
## Description
Windows 10 can sometimes hog ports and sockets preventing us from using them with services like docker. 

## Commands
To show reserverd ports
```bat
netsh interface ipv4 show excludedportrange protocol=tcp
```

One of the solution to free the ports is to restart the `winnat` service
```bat
net stop winnat
net start winnat
```

## Source: 
https://superuser.com/questions/1579346/many-excludedportranges-how-to-delete-hyper-v-is-disabled


## Tags
- windows
- network
- port
- netsh
- winnat