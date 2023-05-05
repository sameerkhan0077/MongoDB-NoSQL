 # MongoDb
 
 ### create database 
 ```
 use wecodeacademy
 ```
 ### CreateCollection 
 ```mongo
 db.createCollection("students);
 ```
### insert-data
```
 db.student.insertMany([{
 "name":"khalil",
 "fatherName":"k.khan",
 "address":"merta",
 "mobile":123456789,
 "emailid":"khalil@gmail.com",
 "admissiondate":("2023-01-01"),
 "dob":("2001-10-15")},

 {"name":"aarif",
 "fatherName":"a.khan",
 "address":"merta",
 "mobile":2020152012,
 "emailid":"aarif@gmail.com",
 "admissiondate":("2023-04-01"),
 "dob":("2000-03-25")},

 {"name":"shera",
 "fatherName":"s.khan",
 "address":"merta",
 "mobile":7866877895,
 "emailid":"shera@gmail.com",
 "admissiondate":("2023-02-01"),
 "dob":("2002-05-12")},
 
 {"name":"irfan",
 "fatherName":"i.khan",
 "address":"merta",
 "mobile":6547896541,
 "emailid":"irfan@gmail.com",
 "admissiondate":("2023-01-01"),
 "dob":("2003-08-10")},

 {"name":"sameer",
 "fatherName":"b.khan",
 "address":"nagour",
 "mobile":7014101046,
 "emailid":"samk@gmail.com",
 "admissiondate":("2023-01-01"),
 "dob":("2001-09-15")},
 
 {"name":"rafik",
 "fatherName":"r.khan",
 "address":"merta",
 "mobile":3413033413,
 "emailid":"rafik@gmail.com",
 "admissiondate":("2023-03-01"),
 "dob":("2003-05-01")},
 
 {"name":"mazeed",
 "fatherName":"m.khan",
 "address":"jaipur",
 "mobile":1212121212,
 "emailid":"mazeed@gmail.com",
 "admissiondate":("2023-04-01"),
 "dob":("1999-04-27")}]);
 ```
