# Tensorflow Saver/Restore 图离线方法

`tf.train.saver` 提供了对整个Tensorflow的离线缓存方法，需先生成saver实例后进行保存，读取操作。
建议在session环境范围内部署saver相关代码：
```python
#class tf.train.saver:
  __init__(
    var_list=None, 
    reshape=False,
    #...
    name=None,  # prefix name
    save_relative_paths=False
  )
```
## Saver
保存运行时图结构(可选），从离线文件中恢复时，如果存在图文件(\*.meta)，
可同时将运行图导入，而无需重复定义：
```python3
saver.export_meta_graph(filename)
```
保存变量：
```python3
saver.save(sess, "/tmp/model.ckpt", global_step=g)
```

## Restore
```python3
saver.restore(sess, save_path)
```
一段常用的从最后检查点恢复的方法
```python3
ckpt = tf.train.get_checkpoint_state(checkpoint_dir)  
if ckpt and ckpt.model_checkpoint_path:  
  saver.restore(sess, ckpt.model_checkpoint_path)
```
或者
```python3
states = tf.train.get_checkpoint_stat(your_checkpoint_di)
checkpoint_paths = states.all_model_checkpoint_paths
saver.recover_last_checkpoints(checkpoint_paths)
```
