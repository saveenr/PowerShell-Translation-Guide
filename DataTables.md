# Datatables				
---

Create a DataTable				
----------------------------------------

```
C# 3.0			

Python or IronPython			

PowerShell 2.0	
	$data1=New-ObjectSystem.Data.Datatable
```
	
### Define the Datatable Columns		
		
```
C# 3.0			

Python or IronPython			

PowerShell 2.0	

    $data1.Columns.Add("Value",[double])
    $data1.Columns.Add("Category",[string])
```
		
# Populating a datatable				

```
C# 3.0			

Python or IronPython			

PowerShell 2.0	
	$data1.Rows.Add(1,"A")
    $data1.Rows.Add(2,"B")
    $data1.Rows.Add(3,"C")
```		
