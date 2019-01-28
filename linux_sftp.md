# Generaly how to connect

```
sftp username@hostname
```

# Using .pem file 

```
sftp -o IdentityFile=key.pem username@hostname
```

# Copy a file from the remote host 

```
get filename
```

# Copy a file from the local computer to the remote host. 

```
put filename
```
	
# Working with 'loca' file system	
Prepending an l to comman commands applys them to local file system. 

E.G. 
- lls
- lmkdir
- lpwd 

 
