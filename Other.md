

				
				


### zip				


``` 
C# 3.0	
	var a = new [] { 1, 2, 3};
	var b = new [] { "a", "b", "c" };
	var c = Enumerable.Range(a.Length)
    	.Select( i=> new { v0=a[i], v1=b[i] } )
    	.List();		

Python or IronPython	
	a = [1,2,3]
	b = ["a","b","c"]
	c = zip(a,b)		

PowerShell 2.0	
	$a = @( 1, 2, 3 ) 
	$b = @( "a", "b", "c" ) 
	$c = 0..($a.count - 1) | 
   		% {, ($a[$_], $b[$_])}  
```



				
### Add members				

```
C# 3.0	
	N/A		

Python or IronPython	
	N/A		

PowerShell 2.0	
	$obj1 | Add-Member -type NoteProperty -name PropName -Value "PropValue"		
```			

### Get List Of Property Values				

```
C# 3.0			

Python or IronPython			

PowerShell 2.0	
	get-service alerter | format-list -property *		
```
				
				
# Other
---

### Warn When Using Uninitialized Variables	

```
    Set-StrictMode -Version 2
```

### Stop Script Execution If There Is an Error
```
    $ErrorActionPreference = "Stop"
```

### Windows Features
----------------------------------------

###(IMPORT WINDOWS MODULES FIRST)

    Get-Windows-Feature <featurename>
    Add-Windows-Feature <featurename>

### Windows Special Folders
----------------------------------------

### Location of My Documents
    $mydocs = [Environment]::GetFolderPath("MyDocuments")


### Get Installation Information about a Product

    get-wmiobject -query "select * from win32_product where IdentifyingNumber='{4676603E-5C2E-4FA4-815B-6A27C113A2C0}'"

### Find All the Products with a Specific Name

    get-wmiobject Win32_Product | Where-Object { $_.Name -like "IronPython*" }

# Misc
----------------------------------------


### Recording Your Session
    Start-Transcript -path d:\steps.ps1
    Stop-Transcript

### Unblocking Files Downloaded From the Internet

### For a single file
    Unblock-File foo.dll

### For all the files in a folder
    Dir d:\scopesdk | Unblock-File	

 



# Printing
----------------------------------------

### Add a printer 
    New-Object -ComObject WScript.Network).AddWindowsPrinterConnection("\\printerserver\hplaser3")

# System.Xml.Linq
----------------------------------------

### Loading the Assembly
    [Reflection.Assembly]::LoadWithPartialName("System.Xml.Linq") | Out-Null

### Loading an XML File
    $xml = [System.Xml.Linq.XDocument]::Load( “c:\foo.xml” )


# Event Log
---


    $applog = Get-EventLog -LogName Application

### Counting Events by Source
    $applog | group Source | Sort-Object Count –Descending



