# Python

* Accessing LAN Folder with Python  

```text
import win32api
import win32net
import win32netcon,win32wnet
import os
 
username=""
password=""
 
try:
    win32wnet.WNetAddConnection2(win32netcon.RESOURCETYPE_DISK, 'Z:','\\\\public\\public', None, username,password, 0)
    print ("connection established successfully")
    cwd = os.getcwd()
    print(cwd)
except:
    print  ("connection not established")
    
    
```

