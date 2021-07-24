# Chat
3er Proyecto


Lo primero que debemos hacer es crear una base de datos con la tabla que utilizaremos.

Las tablas que use para este proyecto fueron:

CREATE TABLE plant1( id INTEGER PRIMARY KEY, name TEXT NOT NULL, division TEXT NOT NULL, color TEXT NOT NULL, phylum TEXT NOT NULL, duration TEXT NOT NULL, type TEXT NOT NULL);
CREATE TABLE plant2( id INTEGER PRIMARY KEY, name TEXT NOT NULL, division TEXT NOT NULL, color TEXT NOT NULL, phylum TEXT NOT NULL, duration TEXT NOT NULL, type TEXT NOT NULL);

Conecte el programa a la base de datos de esta manera : 


![photo_2021-07-23_23-01-37](https://user-images.githubusercontent.com/64318749/126855647-8f18ac24-4b62-48dd-b61f-3894221b8418.jpg)


Para agregar una planta debemos colocar el id de esta planta ( su numero para identificarla ), el nombre de esta, la division o grupo en donde esta pertenece ya sea : Briofita, Pteridofita, Angiosperma o Gimnosperma. Tambien hay que colocar el color de la planta, el filo de esta planta de los cuales hay mas de 20. Posteriormente la clasificacion de esta segun su duracion, donde podemos encontrar:  Anuales, Bianuales y Perennes, y por ultimo hay que seleccionar el tipo de planta.

Podemos modificar una planta colocando el id de la misma y de igual manera podemos eliminar una colocando su id.

Tambien podemos ver todas las plantas del invernadero dandole click al boton de presentar.

En el chat que vamos a observar podemos enviar mensajes al otro usuario sobre el invernadero y podemos limpiar la pantalla del mismo chat. 
Encima del chat podemos observar a quien le estamos enviando este mensaje, y tambien si colocamos la palabra "plant" vamos a poder observar las plantas que tenemos en nuestro invernadero.
