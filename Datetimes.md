				
# Dates And Times				
---

### Get current Date and Time				

```
C# 3.0	
	var now = System.DateTime.Now		

Python or IronPython	
	import datetime
	now = datetime.datetime.now()		

PowerShell 2.0	
	$now = get-date		
```

### Create a Specific Date and Time				

```
C# 3.0	
	var t0 = new System.DateTime(1979,3,31)
	var t1 = new System.DateTime(1979,3,31,1,31,45)		

Python or IronPython	
	t0 = datetime.datetime(1979,3,31)
	t1 = datetime.datetime (1979,3,31,1,31,45)		

PowerShell 2.0	
	$t0 = Get-Date -Year 1979 -Month 3 -Day 31 
	$t1 = Get-Date -Year 1979 -Month 3 -Day 31 -Hour 1 -Minute 31 -Second 45
```
		
### parse a date time string				

```
C#
    var d = System.DateTime.parse( "1979/3/31" )
    
Python			

PowerShell 2.0	
    $t0 = get-date "1979/3/31"
    $t1 = get-date "1979/3/31 1:31:45am"		
```				
