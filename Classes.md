# Classes				


### Create a new class				

```
C# 3.0	
	public class Record
	{
	   public string Name;
	}		

Python	
	class Record :
	   def __init__(self) :
	        pass
		

PowerShell 2.0	

	add-type @"
	public class Record
	{
	   public string Name;
	}
	"@		
```
				
### Create an instanceof a class			

```
C# 3.0	
	var rec1 = new Record()	
	
Python or IronPython	
	rec1 = Record()		

PowerShell 2.0	
	$rec1 = new-object Record		
```
