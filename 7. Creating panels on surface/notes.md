Here will divide a given surface geometry into panels by creating panels from 4 points in U,V directions:


```python
import Rhino.Geometry as rg

points = []

## Define the domain
domain = rg.Interval(0,1)
surface.SetDomain(0, domain)
surface.SetDomain(1, domain)

for u in range(uDiv):
    for v in range(vDiv):
        p1 = surface.PointAt(u/uDiv, v/vDiv)
        p2 = surface.PointAt((u+1)/uDiv, v/vDiv)
        p3 = surface.PointAt((u+1)/uDiv, (v+1)/vDiv)
        p4 = surface.PointAt(u/uDiv, (v+1)/vDiv)
        
        ## Create a surface using the 4 points
        panel = rg.NurbsSurface.CreateFromCorners(p1,p2,p3,p4)
        
        points.append(panel)
        
 ```
