				
# Lists				
---


### New List (untyped)	


```
C# 3.0	
	var names = new List<object> { "Foo, "Bar", "Beer" };	

Python or IronPython	
	names = [ "Foo", "Bar", "Beer" ]		

PowerShell 2.0	
	$names =@( "Foo", "Bar", "Beer" )
or
	$names = "Foo", "Bar", "Beer"		
```

### New List (typed)

```
C# 3.0	
	var names = new List<string> { "Foo, "Bar", "Beer" };		

Python or IronPython	
	N/A		

PowerShell 2.0	
	[string[]] $names = @( "Foo", "Bar", "Beer" )
```		
				
### New empty list (untyped)

```
C# 3.0	
	var names = new List<object> { };		

Python or IronPython	
	names = []

PowerShell 2.0	
	$names =@( )		
```

### New empty list (typed)	


```
C# 3.0	
	var names = new List<string> { };		

Python or IronPython	
	N/A
		
PowerShell 2.0	
	[string[]] $names =@( )		
```

### Length of a list	


```
C# 3.0	
	names.Count		

Python or IronPython	
	len(names)		

PowerShell 2.0	
	$names.Length		
```
