 # MongoDb
 
 ### create database 
 ```sql
 use wecodeacademy
 ```
 ### CreateCollection 
 ```sql
 db.createCollection("students);
 ```
### insert-data students
```sql
 db.student.insertMany([{
 "name":"khalil",
 "fatherName":"k.khan",
 "address":"merta",
 "mobile":123456789,
 "emailid":"khalil@gmail.com",
 "admissiondate":("2023-01-01"),
 "dob":("2001-10-15")},
 ```
```sql
 {"name":"aarif",
 "fatherName":"a.khan",
 "address":"merta",
 "mobile":2020152012,
 "emailid":"aarif@gmail.com",
 "admissiondate":("2023-04-01"),
 "dob":("2000-03-25")},
```
```sql
 {"name":"shera",
 "fatherName":"s.khan",
 "address":"merta",
 "mobile":7866877895,
 "emailid":"shera@gmail.com",
 "admissiondate":("2023-02-01"),
 "dob":("2002-05-12")},
 ```
 ```sql
 {"name":"irfan",
 "fatherName":"i.khan",
 "address":"merta",
 "mobile":6547896541,
 "emailid":"irfan@gmail.com",
 "admissiondate":("2023-01-01"),
 "dob":("2003-08-10")},
```
```sql
 {"name":"sameer",
 "fatherName":"b.khan",
 "address":"nagour",
 "mobile":7014101046,
 "emailid":"samk@gmail.com",
 "admissiondate":("2023-01-01"),
 "dob":("2001-09-15")},
 ```
 ```sql
 {"name":"rafik",
 "fatherName":"r.khan",
 "address":"merta",
 "mobile":3413033413,
 "emailid":"rafik@gmail.com",
 "admissiondate":("2023-03-01"),
 "dob":("2003-05-01")},
 ```
 ```sql
 {"name":"mazeed",
 "fatherName":"m.khan",
 "address":"jaipur",
 "mobile":1212121212,
 "emailid":"mazeed@gmail.com",
 "admissiondate":("2023-04-01"),
 "dob":("1999-04-27")}]);
 ```
  ### CreateCollection
 ```sql
 db.createCollections('Batch');
 ```
 ### insert-data batch 
 ```sql
 db.batch.insert({
 "coursename" : "websiteDesign",
 "startdate" :"2023-01-15",
 "enddate" : "2023-06-20"});
 ```
  ```sql
db.batch.insert({
  "coursename" : "Nodejs",
  "startdate" :"2023-02-15",
  "enddate" : "2023-06-20"});
 ```
 ```sql
  db.batch.insert({
  "coursename" : "mysql",
  "startdate" :"2023-03-15",
  "enddate" : "2023-04-20"});
```
```sql
db.batch.insert({
 "coursename" : "javascript",
 "startdate" :"2023-01-10",
"enddate" : "2023-05-30"});
```
# Mongodb Query

 ### 1. Vo sare students ki list btao jinka email ni hai 
 ```sql
 db.student.find({emailid: {$exists: false}});
 ```
### 2. Vo sare students ki list btao jinka mobile number same hai 
```sql
db.student.find({mobile:{$eq:7014101046}});
```
### 3. Sare students ka only email and mobile return krvao
```sql
db.student.find({},{emailid:1,mobile:1});
```
### 4. students record ki name se sorting krni hai 
```sql
 db.student.find({}).sort({name : 1});
 ```
### 5. vo sare students ki list return kro jinka admission last 3 months me hua hai 
```sql
```
### 6. vo sare students ka only naam btao jinka admission current month me hua hai 
``sql
```
### 7. vo sare students ka naam btao jinki dob year same hai  
```sql
wecodeacademy> db.student.find( { "dob": { $eq: "2001-09-15" } } );
```
### 8. vo sare students ka naam btao jinka address jaipur, nagaur ya karauli ho ;
```sql
db.student.find({ address: { $in: [ "jaipur", "nagaur","karauli" ] } },{ name: 1 });
```
### 9. vo sare students ka naam btao jo Sikar, Jhunjhun se ni hai 
```sql
db.student.find({ address: { $nin: [ "Jhunjhun", "sikar" ] } },{ name: 1});
```

### 10. vo sare students ka naam btao jinka Address Sikar hai and fathername Rahim hai 
```sql
db.student.find({$and: [{ address: "Sikar" },{ fatherName: "fathername.khan" }]}, { name: 1});
```
### 11. vo sare students ka naam btao jinka fathername Khalil ho or email id rahim@gmail.com ho 
```sql
db.student.find({$or: [{ emailid: "rahim@gmail.com " },{ fatherName: "m.Khalil" }]}, { name: 1});
```
### 12. question 11 ko nor se kro 
### 13. Vo sare students ka naam btao jinka father name Ahmed ni hai 
```sql
db.student.find({fatherName : {$nin : ["b.khan"]}}, {name : 1});
```
### 14. Vo sare students ka naam btao jinka mobile 945345435 ni hai
```sql
 db.student.find({"mobile" : {$nin : [123456789]}}, {"name" : 1})
 ```
