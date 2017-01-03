# Exceptions				
---

### Throwing a specific .NET Exception	

```
C# 3.0	
	throw new System.IO.DirectoryNotFoundException()		
	throw new System.IO.DirectoryNotFoundException("Could not find file FOO")		

Python or IronPython	
	raise System.IO.System.IO.DirectoryNotFoundException()		
	raise System.IO.System.IO.DirectoryNotFoundException("Could not find file FOO")		

PowerShell 2.0	
	throw (new-object System.IO.DirectoryNotFoundException)		
	throw (new-object System.IO.DirectoryNotFoundException "Could not find file FOO")		
```

