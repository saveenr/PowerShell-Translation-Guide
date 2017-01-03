
# Loops				
---

### For	

```
C# 3.0	
	for (int i=0; i<10;i++) { }		


Python or IronPython	
    for i in xrange(10) :
       pass		


PowerShell 2.0	
    foreach ($i in 0..9)  { }		
```

### For Each

```
C# 3.0	
	var a = [1,7,8,10]
	foreach (var i in a) { }		

Python or IronPython	
    a = [1,7,8,10]
    for i in a:
       pass		

PowerShell 2.0	
	$a = @(1,2,3)
	foreach ($i in $a) { }		
```

### While	


```
C# 3.0	
	while (true) { }		

Python or IronPython	
	while (True) :
    	pass		

PowerShell 2.0	
	while ($true) { }
```		