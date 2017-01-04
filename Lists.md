				
# Lists				
---


### New List (untyped)	


```
C#
	var names = new List<object> { "Foo, "Bar", "Beer" };	

Python
	names = [ "Foo", "Bar", "Beer" ]		

PowerShell
	$names =@( "Foo", "Bar", "Beer" )
        #or
	$names = "Foo", "Bar", "Beer"		
```

### New List (typed)

```
C#
	var names = new List<string> { "Foo, "Bar", "Beer" };		

Python
	N/A		

PowerShell
	[string[]] $names = @( "Foo", "Bar", "Beer" )
```		
				
### New empty list (untyped)

```
C#
	var names = new List<object> { };		

Python
	names = []

PowerShell
	$names =@( )		
```

### New empty list (typed)	


```
C#
	var names = new List<string> { };		

Python 
	N/A
		
PowerShell
	[string[]] $names =@( )		
```

### Length of a list	


```
C#
	names.Count		

Python
	len(names)		

PowerShell 
	$names.Length		
```
