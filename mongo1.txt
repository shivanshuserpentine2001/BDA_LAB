bmdb.student1.insert({_id:1,StudName:"Ravi",USN:"1BM19CS127", Hobbies:"surfing"});CCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCC
[1]+  Stopped                 mongo
bmsce@bmsce-Precision-T1700:~$ mongo
MongoDB shell version v3.6.8
connecting to: mongodb://127.0.0.1:27017
Implicit session: session { "id" : UUID("3b03378e-bc7b-4aa4-abda-c01bdec00a5f") }
MongoDB server version: 3.6.8
Server has startup warnings: 
2022-05-10T09:01:19.700+0530 I STORAGE  [initandlisten] 
2022-05-10T09:01:19.700+0530 I STORAGE  [initandlisten] ** WARNING: Using the XFS filesystem is strongly recommended with the WiredTiger storage engine
2022-05-10T09:01:19.700+0530 I STORAGE  [initandlisten] **          See http://dochub.mongodb.org/core/prodnotes-filesystem
2022-05-10T09:01:26.110+0530 I CONTROL  [initandlisten] 
2022-05-10T09:01:26.110+0530 I CONTROL  [initandlisten] ** WARNING: Access control is not enabled for the database.
2022-05-10T09:01:26.110+0530 I CONTROL  [initandlisten] **          Read and write access to data and configuration is unrestricted.
2022-05-10T09:01:26.110+0530 I CONTROL  [initandlisten] 
> SHOW DBS
2022-05-10T09:29:07.080+0530 E QUERY    [thread1] SyntaxError: missing ; before statement @(shell):1:5
> show dbs
Stud      0.000GB
admin     0.000GB
config    0.000GB
local     0.000GB
mitdb     0.000GB
myDB      0.000GB
mybdalab  0.000GB
studdb    0.000GB
student   0.000GB
students  0.000GB
test      0.000GB
> use myDB
switched to db myDB
> db.student1.insert({_id:1,nAME:"Ravi", USN:"1BM19CS127",Sem:6,Dept_name:"CSE",CGPA:8.34,Hobbies:["Skating"]});
WriteResult({ "nInserted" : 1 })
> db.student1.insert({_id:2,nAME:"Balaji", USN:"1BM19CS134",Sem:6,Dept_name:"CSE",CGPA:8.5,Hobbies:["TT"]});
WriteResult({ "nInserted" : 1 })
> db.student1.insert({_id:3,nAME:"Skanda", USN:"1BM19CS137",Sem:6,Dept_name:"CSE",CGPA:8.85,Hobbies:["skating"]});
WriteResult({ "nInserted" : 1 })
> db.student1.find()
{ "_id" : 1, "nAME" : "Ravi", "USN" : "1BM19CS127", "Sem" : 6, "Dept_name" : "CSE", "CGPA" : 8.34, "Hobbies" : [ "Skating" ] }
{ "_id" : 2, "nAME" : "Balaji", "USN" : "1BM19CS134", "Sem" : 6, "Dept_name" : "CSE", "CGPA" : 8.5, "Hobbies" : [ "TT" ] }
{ "_id" : 3, "nAME" : "Skanda", "USN" : "1BM19CS137", "Sem" : 6, "Dept_name" : "CSE", "CGPA" : 8.85, "Hobbies" : [ "skating" ] }

> db.student1.insert({_id:4,nAME:"Niteesh", USN:"1BM19EC082",Sem:6,Dept_name:"ECE",CGPA:8.2,Hobbies:["drawing"]});
WriteResult({ "nInserted" : 1 })

> db.student1.aggregate({$match:{Dept_name:"CSE"}},{$group:{_id:"$Sem",Avg_CGPA:{$avg:"$CGPA"}}},{$match:{Avg_CGPA:{$gt:7.5}}});
{ "_id" : 6, "Avg_CGPA" : 8.563333333333333 }


bmsce@bmsce-Precision-T1700:~$ mongoexport --host=localhost  --db=myDB --collection=student1 -o stud.json;
2022-05-10T10:27:17.638+0530	connected to: localhost
2022-05-10T10:27:17.638+0530	exported 4 records


