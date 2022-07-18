Here in this section we will use grasshopper's data structure called data tree. 

Where we will store collection of points in various branches:

```python
from Grasshopper import DataTree
from Grasshopper.Kernel.Data import GH_Path
from Rhino.Geometry import Point3d

## Data Trees
tree = DataTree[Point3d]()

pathCount = 0
newPath = GH_Path(pathCount)

for num in range(len(points)):
    if num % 20 == 0 and num != 0:
        pathCount+= 1
        newPath = GH_Path(pathCount)
    tree.Add(points[num], newPath)
```