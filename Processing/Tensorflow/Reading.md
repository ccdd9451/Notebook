# tf.train 数据预处理相关

```python3
tf.train.shuffle_batch(
    tensors,
    batch_size,
    capacity,
    min_after_dequeue,
    num_threads=1,
    seed=None,
    enqueue_many=False,
    shapes=None,
    allow_smaller_final_batch=False,
    shared_name=None,
    name=None
)
