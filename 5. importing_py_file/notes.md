In grasshopper we can directly input py files and access the functions and variables in it.

```python
import TreeFunctions as tf
reload(tf) ## To update the changes made in the imported library

tree = tf.treeBranch(points, breakP)
```