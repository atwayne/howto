## Description
To update the main photo/face of the person recognized by the Photo app of Windows 11.

## Steps
1. Locate the SQLite database which contains all the face data here, make a backup first.
```
%UserProfile%\Local\Packages\Microsoft.Windows.Photos_8wekyb3d8bbwe\LocalState\MediaDb.v1.sqlite
```
2. Use your faviour SQLite query tool to query and update the sqlite file from previous step.
3. Locate the filename of your faviour photo. Let's assume it is `20181204_075849950_iOS.jpg`
4. Find the `Item_Id` from `Item` table with the filename as a filter.
```sql
SELECT Item_Id, * FROM Item WHERE Item_Filename LIKE '%20181204_075849950_iOS.jpg%'
```
Let's assume the `Item_Id` is `3970`.  
5. Find the `Face_Id` from `Face` table with `Item_Id` from previous step.
```sql
SELECT Face_Id, * FROM Face WHERE Face_ItemId = 3970 -- 1425
```
Let's assume the `Face_Id` is `1425`
6. Locate the person you want to update the bese face from `Person` table.
```sql
SELECT * FROM Person
```
7. Update it with
```sql
UPDATE Person SET Person_BestFaceId=1425, Person_SafeBestFaceId=1425 WHERE Person_Id=XXX
```

## Tags
- windows 11
- windows photo app
- best face
