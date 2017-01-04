# File system				
---

### Get all files in a folder		

```
C#		

Python

PowerShell	
	$files = Get-ChildItem		
```

### Get all files in a folder with a specific extension	


```
C#	

Python

PowerShell
	$files = Get-ChildItem *.dll		
```

### Get all files in a folder recursively	


``` 
C#

Python

PowerShell 
    $files = Get-ChildItem -Recurse		
```

### Get all files in a folder recursivelyand get full pathname	


```
C#			

Python			

PowerShell
	$files = Get-ChildItem –Recurse | Foreach-Object { $_.FullName}		
```

### Getting the My Documents Folder

```

C#

Python

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

PowerShell
	join-path "foo\bar" "beer"		
```			

### Path Exists?	


```
C#
	System.IO.Directory.Exists("d:\\foo")
	System.IO.File.Exists("d:\\foo.txt"))


Python	
	os.path.exists( "d:\\foo.txt" )


PowerShell
    test-path "d:\foo.txt"


```		

### Get Full path			

```
C#	
	System.IO.Path.GetFullPath("foo.txt")	

Python
	os.path.abspath( "foo.txt" )		

PowerShell
	[IO.Path]::GetFullPath("foo.txt")		
```

### Normalize Paths	

``` 
C#

Python


PowerShell
	$d = resolve-path "D:\foo\..\bar\beer"		
```

### Create a Directory				

```
C#

Python

PowerShell
	New-Item -Path d:\folder -ItemType Directory		
```

### Delete Folder and Contents Recursively	

```
C#	

Python

PowerShell 2.0	
	Remove-Item "D:/folder" -Recurse		
				
```
