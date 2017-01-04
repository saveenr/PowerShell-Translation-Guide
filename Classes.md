# Classes				


### Create a new class				

```
C#	
	public class Record
	{
	   public string Name;
	}		

Python	
	class Record :
	   def __init__(self) :
	        pass
		

PowerShell	

	add-type @"
	public class Record
	{
	   public string Name;
	}
	"@		
```
				
### Create an instanceof a class			

```
C
	var rec1 = new Record()	
	
Python
	rec1 = Record()		

PowerShell
	$rec1 = new-object Record		
```
