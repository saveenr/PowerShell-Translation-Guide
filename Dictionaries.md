
				
# Dictionaries				
---

### Empty Dictionary				

```
C#
	using System.Collections.Generic;
	var d = new Dictionary<string,string>;		


Python
	d = { }
	d = dict()
		

PowerShell
	$d = @{ }		
```

### Non-empty dictionary				



```
C# 3.0	
	var d = new Dictionary<string,string> 
   		{ {"foo","bar"} , {"baz","beer"}};		

Python or IronPython	
	d = { "foo" : "bar", "baz":"beer" }		

PowerShell 2.0	
	$d = @{"foo"="bar";"baz"="beer" }		
```

### set values				


```
C# 3.0	
	d[ "foo" ] = "bar2"		

Python or IronPython	
	d[ "foo" ] = "bar2"		

PowerShell 2.0	
	$d[ "foo" ] = "bar2"		
```

### key exists				



```
C#
	if (d.ContainsKey("foo") { … }		

Python
	if ( "foo" in d ) :
    	#do something		

PowerShell	
	if $d.ContainsKey("foo") { }		
```

### get value				



```
C#
	d[ "foo" ]		

Python
	d[ "foo" ]		

PowerShell
	$d.Item("foo")		
```

get all keys				

```
C# 
	d.Keys		

Python	
	d.keys()
or
	[k for k in d.iterkeys()]		

PowerShell 2.0	
	$d.Keys		
```

### get all values				


```
C# 3.0	
	d.Values		

Python	
	d.values()
        # or
	[v for v in d.itervalues()]		

PowerShell
	$d.Values		
```

# unique elements				

```
C#	
	var a = new [] { "a", "b", "c" };
	var b = a.Distinct().ToList();		

Python	
	a = ["a", "a", "b"]
	b = set( a )		

PowerShell	
	$a = @( "a", "a", "b" ) 
	$b = a | sort –unique		
```

