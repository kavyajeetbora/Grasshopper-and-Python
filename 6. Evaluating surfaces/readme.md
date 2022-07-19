## Creating points on a surface


```python
import Rhino.Geometry as rg

points = []

## Define the domain
domain = rg.Interval(0,1)
surface.SetDomain(0, domain)
surface.SetDomain(1, domain)

for u in range(uDiv+1):
    for v in range(vDiv+1):
        point = surface.PointAt(u/uDiv, v/vDiv)
        points.append(point)
```