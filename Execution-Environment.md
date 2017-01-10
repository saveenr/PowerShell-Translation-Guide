				
				
# Execution Environment				


###Get current directory				

```
C#
    string d = System.IO.GetCurrentDirectory();

Python
    import os
    d = os.getcwd()

PowerShell
    $d = Get-Location	
    
```

### Get location of current script or exe


```
C#
    string d  = Assembly.GetExecutingAssembly().Location;
    // Note Assembly.GetExecutingAssembly().CodeBase might be better choice in some cases

Python
     os.path.realpath(__file__)

PowerShell
     $d = Split-Path $MyInvocation.MyCommand.Path		
```
	
