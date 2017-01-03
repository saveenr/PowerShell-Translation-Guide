# File system				
---

### Get all files in a folder		

```
C# 3.0		
	Python or IronPython			

PowerShell 2.0	
	$files = Get-ChildItem		
```

### Get all files in a folder with a specific extension	


```
C# 3.0		

Python or IronPython			

PowerShell 2.0	
	$files = Get-ChildItem *.dll		
```

### Get all files in a folder recursively	


``` 
Python or IronPython			

PowerShell 
	2.0	$files = Get-ChildItem -Recurse		
```

### Get all files in a folder recursivelyand get full pathname	


```
C# 3.0			

Python or IronPython			

PowerShell 2.0	
	$files = Get-ChildItem –Recurse | Foreach-Object { $_.FullName}		
```

### Getting the My Documents Folder	C# 3.0			

```
Python or IronPython			

PowerShell 2.0
	[Environment]::GetFolderPath("MyDocuments")		
				
```				
				
# Paths				
---

### Splitting Paths	C# 

```
C# 3.0	
	var a = System.IO.Path.GetDirectoryName("foo\\bar\\beer")
	var b = System.IO.Path.GetFileName("foo\\bar\\beer")		
	

Python or IronPython	
	a , b = os.path.split ("foo\\bar\\beer" )		


PowerShell 2.0	$a = split-path "\foo\bar\beer"
	$b = split-path "\foo\bar\beer" -leaf
```

###	Joining Paths	

```
C# 3.0	
	System.IO.Path.Combine("foo\\bar" , "beer" )		

Python or IronPython	
	os.path.join( "foo\\bar" , "beer" )		

PowerShell 2.0	
	join-path "foo\bar" "beer"		
```			

### Path Exists?	


```
C# 3.0	
	if (System.IO.Directory.Exists("d:\\foo")) { }
	if (System.IO.File.Exists("d:\\foo.txt")) { }


Python or IronPython	
	if (os.path.exists( "d:\\foo.txt" )) :
    	# do something


PowerShell 2.0	
    if ( test-path "d:\foo.txt" ) { }
	if ( ! (test-path "D:\\x") ) { }

```		

### Get Full path			

```
C# 3.0	
	System.IO.Path.GetFullPath("foo.txt")	

Python or IronPython	
	os.path.abspath( "foo.txt" )		

PowerShell 2.0	
	[IO.Path]::GetFullPath("foo.txt")		
```

### Normalize Paths	

``` 
Python or IronPython			


PowerShell 2.0	
	$d = resolve-path "D:\foo\..\bar\beer"		
```

### Create a Directory				

```
PowerShell 2.0	
	New-Item -Path d:\folder -ItemType Directory		
```

### Delete Folder and Contents Recursively	

```
C# 3.0			


Python or IronPython			

PowerShell 2.0	
	Remove-Item $folder -Recurse		
				
```
