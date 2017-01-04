# Exceptions				
---

### Throwing a specific .NET Exception	

```
C#
	throw new System.IO.DirectoryNotFoundException()		
	throw new System.IO.DirectoryNotFoundException("Could not find file FOO")		

Python
	raise System.IO.System.IO.DirectoryNotFoundException()		
	raise System.IO.System.IO.DirectoryNotFoundException("Could not find file FOO")		

PowerShell
	throw (new-object System.IO.DirectoryNotFoundException)		
	throw (new-object System.IO.DirectoryNotFoundException "Could not find file FOO")		
```

