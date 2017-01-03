
				
# Dictionaries				
---

### Empty Dictionary				

```
C# 3.0	
	using System.Collections.Generic;
	var d = new Dictionary<string,string>;		


Python or IronPython	
	d = { }
	d = dict()
		

PowerShell 2.0	
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
C# 3.0	
	if (d.ContainsKey("foo") { … }		

Python or IronPython	
	if ( "foo" in d ) :
    	#do something		

PowerShell 2.0	
	if $d.ContainsKey("foo") { }		
```

### get value				



```
C# 3.0	
	d[ "foo" ]		

Python or IronPython	
	d[ "foo" ]		

PowerShell 2.0	
	$d.Item("foo")		
```

get all keys				

```
C# 
	3.0	d.Keys		

Python or IronPython	
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

Python or IronPython	
	d.values()
or
	[v for v in d.itervalues()]		

PowerShell 2.0	
	$d.Values		
```

# unique elements				

```
C# 3.0	
	var a = new [] { "a", "b", "c" };
	var b = a.Distinct().ToList();		

Python or IronPython	
	a = ["a", "a", "b"]
	b = set( a )		

PowerShell 2.0	
	$a = @( "a", "a", "b" ) 
	$b = a | sort –unique		
```

