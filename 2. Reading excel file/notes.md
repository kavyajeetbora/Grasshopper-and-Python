## Importing the excel library
1. For importing the excel library, we need to attached the library to our python script:
```python 
import clr
clr.AddReference("Microsoft.Office.Interop.Excel")
```
Note: *here [clr](https://en.wikipedia.org/wiki/Common_Language_Runtime) stands for common language runtime which is responsible for managing the execution of .NET programs.

**Function**: Just-in-time compilation converts the managed code (compiled intermediate language code) into machine instructions which are then executed on the CPU of the computer*

Now we can import the library in our python script and use the functions of it in our code:

```python
import Microsoft.Office.Interop.Excel as excel

## Instantiating an excel class object
ex = excel.ApplicationClass()

## Opening an workbook
workbook = ex.Workbooks.Open("Reading excel file\\03_03.xlsx")

## Read worksheet
ws = workbook.Worksheets[1] ## Note that the index starts at 1

## Extracting the data
pX = []
pY = []
pZ = []


for i in range(ws.UsedRange.rows.Count):

    if i !=0:
        ## get the values 
        x = ws.Range(f"A{i+1}") 
        y = ws.Range(f"B{i+1}")
        z = ws.Range(f"C{i+1}")
        ## add the values
        pX.append(x)
        pY.append(y)
        pZ.append(z)

## Once the data is extracted, close the excel
workbook.Close(False) ## here save file = False
ex.Quit()

## Assign the outputs
a = pX
b = pY
c = pZ


## Using construct point component in grasshopper
```





