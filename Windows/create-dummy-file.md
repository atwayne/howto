## Description
To create a dummy file in seconds.

> Creates a file of the specified name and size, with content that consists of zeroes.


## Commands
### Syntax
```
fsutil file createnew <filename> <length>
```

### Examples
- Create a file with size of 1MB  
```
fsutil file createnew 1MB 1048576
```
- Create a file with size of 1GB  
```
fsutil file createnew 1GB 1073741824
```
- Create a file with size of 10GB  
```
fsutil file createnew 10GB 10737418240
```
- Create a file with size of 50MB  
```
fsutil file createnew 50GB 53687091200
```


## Source: 
https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/fsutil-file

## Tags
- disk
- windows
