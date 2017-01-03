# LINQ				
--

```
		var a = new [] { "a", "b", "c" };		
		a = ["a", "b", "c" ]		
		$a = @( "a", "b", "c" )		
```

### SELECT				

```
C# 3.0	
	var a1 = a.Select( x=>x.Length ).ToArray();		

Python or IronPython	
	a1 = [len(x) for x in a]		

PowerShell 2.0	
	$a1 = $a | ForEach-Object{ $_.Length }		
```

### WHERE				

```
C# 3.0	
	var a2 = a.Where( x=>x == "a" ).ToArray();		

Python or IronPython	
	a2 = [x for x in a if x=="a"]		

PowerShell 2.0	
	$a2 = $a | Where-Object { $a –eq "a" }		
```

### DISTINCT				

```
C# 3.0	
	var a3 = a.Distinct().ToArray();		

Python or IronPython	
	a3 = list( set( a ) )		

PowerShell 2.0	
	$a3 = $a | sort -unique		

```

### SUM on a property				

```
C# 3.0	
	int  s = a.Select( x=>x.Length).Sum();		

Python or IronPython	
	s = sum(len(x) for x in a)
or
	s = reduce( lambda x,y: x+y , a1)		

PowerShell 2.0	
	// incomplete		
```



### Selecting properties and Anonymous Types				

```
C# 3.0	
	var items2 = items.Select( item => new { a=item.Length, b=item.Name } );		

Python or IronPython	
	// incomplete		

PowerShell 2.0	
	$items2 = $items | Select-Object Length,Name 		
				