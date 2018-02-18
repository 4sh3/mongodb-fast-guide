## Install mongoDB
> sudo apt-get install mongodb

## Execute mongo on shell
> mongo
* if give an error use: 
> sudo service mongodb restart

## Consultas en MongoDB fast spanish guide
db.<collection>.insert({JSON-Document}) Permite agregar una o varias colecciones a una base de datos.
db.<collection>.insertOne({JSON-Document}) A diferencia del insert({JSON-Document}), este método solo inserta una colección.
db.<collection>.insertMany([{JSON-Document}, {Other-JSON-Document}, {...}]) Este método es similar a insert({JSON-Document}), sin embargo, este método fue incluido en la versión 3 de MongoDB por ende debe comenzar a usarse y evitar insert({JSON-Document}).

db.<collection>.find() Imprime los primeros 20 documentos que encuentre.
db.<collection>.findOne() Imprime solo el primer documentos que encuentre.
db.<collection>.find({"clave" : {$gte: "cantidad"}},{clave: 0, clave : 1}).limit(2).pretty() Find global que muestra el valor de la clave el cual sea mayor o igual que la cantidad mencionada ($gt/$gte/$lt/$lte)

db.<collection>.save({JSON-Document)} Modifica un campo si se encuentra en una colección, si no se agrega.
db.<collection>.update({JSON-Document)} Actualiza el documento por completo, es decir, elimina todos los campos y agrega los nuevos dejando así solo el _id.
db.<collection>.updateOne({filtro}, {"clave": "valor"}) Se actualizará el primer documento que coincida con el filtro.
db.<collection>.updateMany({filtro}, {"clave": "valor"}) Se actualizará todos los documentos que coincida con el filtro.

db.<collection>.deleteOne({"filter")} Elimina el primer documento encontrado según el filtro.
db.<collection>.deleteMany({"filter")} Elimina todos los documentos encontrados según el filtro.
db.<collection>.remove({"filter")} Elimina un campo según el filtro, es decir, si coincide uno o muchos documentos con el filtro serán eliminados de la base de datos.
db.<collection>.drop() Elimina todos los documentos de una colección.

## Complete guide
https://joaquinaraujo.github.io/mongodb-redis/
