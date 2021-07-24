# Chat
3er Proyecto


Lo primero que debemos hacer es crear una base de datos con la tabla que utilizaremos.

Las tablas que use para este proyecto fueron:

CREATE TABLE plant1( id INTEGER PRIMARY KEY, name TEXT NOT NULL, division TEXT NOT NULL, color TEXT NOT NULL, phylum TEXT NOT NULL, duration TEXT NOT NULL, type TEXT NOT NULL);


CREATE TABLE plant2( id INTEGER PRIMARY KEY, name TEXT NOT NULL, division TEXT NOT NULL, color TEXT NOT NULL, phylum TEXT NOT NULL, duration TEXT NOT NULL, type TEXT NOT NULL);



Conecte el programa a la base de datos de esta manera : 

Vamos a Window > Perspective 
![photo_2021-07-23_23-01-37](https://user-images.githubusercontent.com/64318749/126855647-8f18ac24-4b62-48dd-b61f-3894221b8418.jpg)




En Open Perspective le damos click  Other...
![photo_2021-07-23_23-01-40](https://user-images.githubusercontent.com/64318749/126855664-f40fe79a-4c37-4ac5-85c5-b596b19af012.jpg)




En la ventana que nos aparece, le damos click a Database Development que es lo que queremos
![photo_2021-07-23_23-01-42](https://user-images.githubusercontent.com/64318749/126855674-295e11d4-54bd-4aba-9d22-616d47dd803f.jpg)




Buscamos PostgreSQL y le damos a Next
![photo_2021-07-23_23-01-44](https://user-images.githubusercontent.com/64318749/126855687-2c2d4422-5c0b-47d5-8e18-e1ab48e2ad5a.jpg)



Nos aparecera una ventana con el nombre de nuestra base de datos y contraseña, hay que revisar estas dos y luego darle a Test Connection.
Debe aparecerte Ping Suceeded!
![photo_2021-07-23_23-01-46](https://user-images.githubusercontent.com/64318749/126855697-36426e3a-d79d-49d5-89f9-44cce2012d95.jpg)



De esta forma nos conectamos a la base de datos
![photo_2021-07-23_23-01-48](https://user-images.githubusercontent.com/64318749/126855721-003f2c3b-fddf-4293-acc5-2740e7f8f502.jpg)


Al darle a Run nos aparecera primero una ventana donde debemos colocar los nombres de los dos usuarios que se encontraran para identificarlos ene el Chat.

Para agregar una planta debemos colocar el id de esta planta ( su numero para identificarla ), el nombre de esta, la division o grupo en donde esta pertenece ya sea : Briofita, Pteridofita, Angiosperma o Gimnosperma. Tambien hay que colocar el color de la planta, el filo de esta planta de los cuales hay mas de 20. Posteriormente la clasificacion de esta segun su duracion, donde podemos encontrar:  Anuales, Bianuales y Perennes, y por ultimo hay que seleccionar el tipo de planta.

Podemos modificar una planta colocando el id de la misma y de igual manera podemos eliminar una colocando su id.

Tambien podemos ver todas las plantas del invernadero dandole click al boton de presentar.

En el chat que vamos a observar podemos enviar mensajes al otro usuario sobre el invernadero y podemos limpiar la pantalla del mismo chat. 
Encima del chat podemos observar a quien le estamos enviando este mensaje, y tambien si colocamos la palabra "plant" vamos a poder observar las plantas que tenemos en nuestro invernadero.
