# Exceptions				
---

### Throwing an Exception	

```
C#
	throw new System.IO.DirectoryNotFoundException()		
	throw new System.IO.DirectoryNotFoundException("Could not find directory FOO")		

Python
	raise SomeException('Smom error')
	
IronPython
	raise System.IO.System.IO.DirectoryNotFoundException()		
	raise System.IO.System.IO.DirectoryNotFoundException("Could not find directory FOO")		

PowerShell
	throw [System.IO.DirectoryNotFoundException]
	throw [System.IO.DirectoryNotFoundException] "Could not find directory FOO"
	
	# or to directly control the exception object
	
	$exc = new-object System.IO.DirectoryNotFoundException "Could not find directory FOO"		
	throw $exc		
```

### Catching an Exception	

```
C#
	try
	{
		// do something
	}
	catch (SomeException error)
	{
	}
	
Python
	try:
		raise SomeException('some message')
	except SomeException as error:
		print('caught this error: ' + repr(error))


PowerShell
	try
	{
		# do something
	}
	catch [System.IO.DirectoryNotFoundException]
	{
		# handle exception
	}

```


### Rethrowing an a caught Exception	

```
C#
	try
	{
		// do something
	}
	catch (SomeException error)
	{
		throw;		
	}
	
Python
	try:
		# do something
	except SomeException as error:
		raise 

PowerShell
	try
	{
		# do something
	}
	catch [System.IO.DirectoryNotFoundException]
	{
		throw
	}

```
