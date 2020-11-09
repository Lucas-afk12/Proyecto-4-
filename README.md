# Proyecto-4-

Resultados de las consultas:

-db.cultivo.find({$and:[{cbd:{$in:["none","bajo"]},"genetica.tipo":{$eq:"sativa"}}]});

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f32"), "planta" : "Chem Berry D", "precio" : 25.5, "thc" : 32, "genetica" : { "tipo" : "sativa", "Predominancia" : "dominante" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f33"), "planta" : "Bruce Banner BX 2.0", "precio" : 23, "thc" : 30, "genetica" : { "tipo" : "sativa", "Predominancia" : "dominante" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f34"), "planta" : "HulkBerry", "precio" : 18.5, "thc" : 27, "genetica" : { "tipo" : "sativa", "Predominancia" 
: "semi" }, "cbd" : "bajo" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f38"), "planta" : "Romulan Haze", "precio" : 13, "thc" : 20, "genetica" : { "tipo" : "sativa", "Predominancia" : "dominante" }, "cbd" : "bajo" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f39"), "planta" : "Where's My Bike", "precio" : 10, "thc" : 17, "genetica" : { "tipo" : "sativa", "Predominancia" : "semi" }, "cbd" : "bajo" }

-db.cultivo.find({'genetica.tipo':{$eq:"indica"},$or:[{"genetica.Predominancia":{$eq:"semi"}},{thc:{$gt:29}}]});

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f35"), "planta" : "Original Glue", "precio" : 17, "thc" : 30, "genetica" : { "tipo" : "indica", "Predominancia" : "dominante" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f36"), "planta" : "Girl Scout Cookies", "precio" : 16.5, "thc" : 28, "genetica" : { "tipo" : "indica", "Predominancia" : "semi" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f37"), "planta" : "Green Gelato", "precio" : 15, "thc" : 27, "genetica" : { "tipo" : "indica", "Predominancia" : "semi" }, "cbd" : "bajo" }

-db.cultivo.find({$and:[{precio:{$lt:17}},{thc:{$gte:23}}]});

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f36"), "planta" : "Girl Scout Cookies", "precio" : 16.5, "thc" : 28, "genetica" : { "tipo" : "indica", "Predominancia" : "semi" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f37"), "planta" : "Green Gelato", "precio" : 15, "thc" : 27, "genetica" : { "tipo" : "indica", "Predominancia" : "semi" }, "cbd" : "bajo" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f3a"), "planta" : "Island Sweet Skunk", "precio" : 13, "thc" : 23, "genetica" : { "tipo" : "sativa", "Predominancia" : "semi" }, "cbd" : "alto" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f3b"), "planta" : "Gorilla Zkittlez", "precio" : 8, "thc" : 29, "genetica" : { "tipo" : "indica", "Predominancia" : "dominante" }, "cbd" : "none" }

-db.cultivo.find({$and:[{"genetica.tipo":{$ne:"indica"}},{cbd:{$nin:["bajo"]}}]});

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f32"), "planta" : "Chem Berry D", "precio" : 25.5, "thc" : 32, "genetica" : { "tipo" : "sativa", "Predominancia" : "dominante" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f33"), "planta" : "Bruce Banner BX 2.0", "precio" : 23, "thc" : 30, "genetica" : { "tipo" : "sativa", "Predominancia" : "dominante" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f3a"), "planta" : "Island Sweet Skunk", "precio" : 13, "thc" : 23, "genetica" : { "tipo" : "sativa", "Predominancia" : "semi" }, "cbd" : "alto" }

-db.cultivo.find({$and:[{planta:{$not:{$regex:"^G.*"}}},{$nor:[{precio:{$lte:15}},{"genetica.Predominancia":{$eq:"semi"}}]}]})

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f32"), "planta" : "Chem Berry D", "precio" : 25.5, "thc" : 32, "genetica" : { "tipo" : "sativa", "Predominancia" : "dominante" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f33"), "planta" : "Bruce Banner BX 2.0", "precio" : 23, "thc" : 30, "genetica" : { "tipo" : "sativa", "Predominancia" : "dominante" }, "cbd" : "none" }

{ "_id" : ObjectId("5fa88bd7e087afcd45fd0f35"), "planta" : "Original Glue", "precio" : 17, "thc" : 30, "genetica" : { "tipo" : "indica", "Predominancia" : "dominante" }, "cbd" : "none" }
