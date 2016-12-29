# tensorflow-snippets
```
import tensorflow as tf

import os
cwd = os.getcwd()
print(cwd)

with tf.gfile.FastGFile("../tensorflow/tf_files/retrained_graph.pb", 'rb') as f:
    graph_def = tf.GraphDef()
    graph_def.ParseFromString(f.read())
    graph = tf.import_graph_def(graph_def, name='')

# print(graph)
[n.name for n in tf.get_default_graph().as_graph_def().node]
```
