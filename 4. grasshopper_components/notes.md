- In this tutorial, we will make a nurds curve from list of points.
- We will use the same tree of points from the previous exercise

## Basic Outline
1. iterate over list of points in the grasshopper tree object
2. Then create a curve item from these list of points
3. Then from the list of curves, 

```python
import ghpythonlib.components as ghc

curves = []

## Access each branch one at a time:
for i in range(points.BranchCount):
    points_list = points.Branch(i)
    nCurve = ghc.NurbsCurve(points_list, 3, False)
    curves.append(nCurve.curve)


a = ghc.Loft(curves)
```