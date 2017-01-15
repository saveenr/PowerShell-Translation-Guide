# File system				
---

### Get all files in a folder		

```
C#		
	var all_files = System.IO.Directory.GetFiles("D:\\folder")
	var all_jpgs = System.IO.Directory.GetFiles("D:\\folder","*.jpg")

Python
	import os
	import glob
	all_files = os.listdir("D:\\folder")
	all_jpgs = glob.glob("D:\\folder\\*.jpg")

PowerShell	
	$all_files  = Get-ChildItem d:\folder		
	$all_jpgs = Get-ChildItem d:\folder\*.jpg	
	$all_jpgs = Get-ChildItem d:\folder -Filter .jpg
```



### Get all files in a folder recursively	


``` 
C#

Python

PowerShell 
    $files = Get-ChildItem -Recurse		
```

### Getting the My Documents Folder

```

C#
	string mydocs = System.Environment.GetFolderPath("MyDocuments");
	
Python

	import win32com.shell
	mydocs = win32com.shell.shell.SHGetFolderPath(0, win32com.shell.shellcon.CSIDL_PERSONAL, None, 0)

PowerShell 2.0
	$mydocs = [Environment]::GetFolderPath("MyDocuments")		
				
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
