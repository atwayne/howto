## Description
To delete a recovery partition in Windows.

## Commands

```CMD
> diskpart
DISKPART> list disk
DISKPART> select disk 2
DISKPART> list partition
DISKPART> select partition 
DISKPART> delete partition override
```


## Tags
- disk management
- diskpart
- windows
- recovery partition
