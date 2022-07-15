# Notes on importing modules and Libraries

## How rhino and grasshopper works behind the scenes:
1. Grasshopper python version is IronPython
2. IronPython is same as python v2 but it is developed to work within dot net framework
3. modules of rhino - rhinoscriptsyntax and RhinoCommon
4. Rhino modules are not python file but are DLL files (Dynamic Linked Library)
5. DLL files are pre-compiled files and written in another language such as c#
6. IronPython provides the interface to execute this code in python syntax.