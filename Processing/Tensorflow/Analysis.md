# Tensorboard相关分析文件输出方法

```python3
writer = tf.summary.FileWriter.__init__(
  logdir, graph=None, max_queue=10, flush_secs=120, graph_def=None)
writer.add_summary(summary, global_step=None)
writer.flush()
writer.close()
```

# tf.summary 类别总结

