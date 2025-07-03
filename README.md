mongosh

show dbs =>show database list

use admin => change database

db.createCollection("student") => create database

db.student.insertOne({name:"Yash",age:19}) => insert value in database.

db.student.insertMany([{name:"Yash",age:19},{name:"Romil",age:18},{name:"Harnish"},{name:"Rudra",gender:"MALE"}]) => insert many values using array

db.student.updateOne({name:"Mohit"},{$set:{name:"Yash"}}) =>update one record pan je pela ave te update karshe.

db.student.updateMany({field:"IT"},{$set:{age:21}})

db.student.find({name:"Yash"})

db.student.find({name:"Yash"},{age:1}) => only require field shown

db.student.find({name:"Yash"},{age:1,_id:0}) => only id ma zero valid.

db.student.findOne({age:21})

db.student.find({age:21}).limit(1) =>scan full database and give one value which is first.

# Comparision Operator :
$eq,$gte,$lte,$ne,$gt,$lt,$in,$nin

db.student.find({age:{$gte:20}}) =>greater than or equal.

db.student.find({age:{$in:[21,23]}}) => for range of age using in operator.

# Logical Operator :
$and,$or,$not,$nor

db.student.find({$and:[{age:21},{field:"IT"}]})

db.student.find({$or:[{age:21},{gender:"MALE"},{field:"IT"}]})

# field update operator:
