# Basics				
---

###True/False				


```
C#
    true
    false

Python
    True
    False		

PowerShell
    $true
    $false		

```

###Null				


```
C#
    null		

Python 
    None		

PowerShell
    $null		
```

### Declare and Assign				


```

C#
    var hello = "world";		

Python 
	hello = "world"		

PowerShell 2.0	
	$hello = "word"		
```

### if				

```
C#	
	if ( true ) { … }
	if ( false ) { … }
		
Python 
 	if ( True ) :
    	# do nothing
	if ( False ) :
    	# do nothing		

PowerShell 2.0	
	if ( $true ) { }
	if ( $false ) { }		
```


### test for null				

```
C# 3.0	
	if ( a == null ) { }		

Python or IronPython	
	if (a == None) :
    	    # do nothing		

PowerShell 2.0	
	if ( $a –eq $null ) { }		
```

### do nothing				

```
C# 3.0			
    N/A


Python or IronPython	
    pass		


PowerShell 2.0			
    N/A
```
