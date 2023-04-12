## 28
`db.empleados.find({ contrato: "Indefinido"}).count()`

## 29
`db.empleados.find({ contrato: "Temporal"}, { nome: 1, apelidos: 1, salario: 1}).sort({ salario: 1 })`

## 30
`db.empleados.find({ contrato: "Temporal"}, { nome: 1, apelidos: 1, salario: 1}).sort({ salario: -1, apelidos: 1, nome: 1 })`

## 31
`db.empleados.find({}).sort({ data_nac: 1 }).limit(4)`

## 32
`db.empleados.find({ num_fillos: { $gt: 1 }, dni: /A$/ }, { _id: 0, dni: 1, num_fillos: 1, nome: 1, apelidos: 1}).sort({ apelidos: 1, nombre: 1}).skip(5).limit(2)`

## 33
`db.empleados.updateOne({ nome: 'Osvaldo', apelidos: 'Sánchez Hernández'}, { $set: { num_fillos: 2, telefono: 620691338, fax: 973100100}})`

## 34
`db.empleados.updateOne({ dni: '10000000Z'}, { $inc: {num_fillos: 1}})`

## 35
`db.empleados.updateOne({ dni: '99004348C' }, { $unset: { num_fillos: 0}})`

## 36
`db.empleados.updateMany({ dni: { $in: ['95991061D', '99004348C']}}, { $inc: { num_fillos: 1 }})`

## 37
`db.empleados.updateMany({ dni: { $in: ['95991061D', '99004348C']}}, { $inc: { num_fillos: 1 }})`

## 38
`db.empleados.updateOne({ dni: '12345678Z'}, {$set: {nome: 'Antón', apelidos: 'Pérez Pérez', enderezo: { localidade: 'A Coruña', provincia: 'A Coruña', rua: 'Ronda de Outeiro, 3'}}}, { upsert: true })`

## 39
`db.empleados.updateMany({ contrato: 'Por obra'}, { $set: { contrato: 'Por obra ou servizo'}})`

## 40
`db.empleados.updateMany({ contrato: 'Por obra'}, { $set: { contrato: 'Por obra ou servizo'}})`

## 41
`db.empleados.updateMany({ contrato: 'Por obra'}, { $set: { contrato: 'Por obra ou servizo'}})`

## 42
`db.empleados.updateMany({ num_fillos: { $gt: 0 }, hobbies: 'Coidar da prole'}, { $pull: { hobbies: 'Coidar da prole'}})`

## 43
`db.empleados.updateMany({ salario: { $gt: 10000 }}, { $mul: { salario: 1.07 }})`
