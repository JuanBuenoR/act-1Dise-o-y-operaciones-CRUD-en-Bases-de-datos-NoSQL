Reglas básicas del torneo de la copa del mundo de la FIFA 2022
1.	El evento tendrá un total de 32 selecciones deportivas clasificadas oficialmente.
2.	Cada selección podrá inscribir un máximo de 26 jugadores. 
3.	Cada selección podrá inscribir un máximo de 11 integrantes del staff deportivo que deben incluir: director técnico, Asistente Técnico 1, Asistente Técnico 2, Entrenador de Porteros, Preparador Físico 1, Preparador Físico 2, Médico, Kinesiólogo, Utilero, nutricionista y masajista.
4.	El sistema de Juego es el siguiente:
-	El tiempo de juego oficial será de 90 minutos divididos en 2 mitades de 45 minutos cada una.
-	Cada encuentro contará con 8 árbitros delimitados así: en el campo de juego habrá un juez central, dos jueces de línea y un juez auxiliar, en el apoyo VAR habrá 4 jueces. 
-	Cada encuentro se jugará en una sede oficial acorde al fixture oficial del evento.
-	El evento tendrá 2 tipos de etapas: etapa 1 , fase de grupos, etapa 2 fase de eliminación directa.
-	Las fases del evento están delimitadas asi: Fase de Grupos (etapa 1), Octavos de Final, cuartos de Final, semifinales y gran final (etapa 2).
-	Se crearán 8 grupos de 4 equipos para la fase de grupos.
-	En cada encuentro de la fase de grupos se pueden encontrar 3 resultados: Por una victoria, el equipo recibe 3 puntos, por un empate, el equipo recibe 1 punto, por una derrota, el equipo no recibe puntos.
-	En cada encuentro de la fase de eliminación directa en caso de no haber un ganador al finalizar el tiempo reglamentario, el partido se extenderá por 2 tiempos de 15 minutos adicionales, si al finalizar estos tiempos adicionales aun no se conoce un ganador, este se definirá con lanzamientos desde el punto penal iniciando con 5 lanzamientos cada uno, pero si se conserva el empate se realizará un lanzamiento por equipo.
Condiciones para las Colecciones:
1.	Selecciones:
-	Id
-	Nombre
-	Colores
-	Palmarés
-	Escalafón
-	PJ
-	PG
-	PE
-	PP
-	GF
-	GC
-	DF
-	PTS

2.	Sedes
-	Id
-	Nombre
-	Ubicación
-	Capacidad

3.	Árbitros
-	Id
-	Nombre
-	Nacionalidad
-	Escalafón

4.	Jugadores
-	Id
-	Nombre
-	Selección id
-	Posición
-	Fecha de nacimiento
-	Club actual
-	Goles

5.	Staff
-	Id
-	Nombre
-	Selección id
-	Rol

6.	Fixture
-	Id
-	Fecha
-	Sede id
-	Fase
-	Equipo Local id
-	Equipo Visitante id
-	Hora
-	Árbitros
 
7.	Resultados 
-	Id
-	Fixture id
-	Goles Local
-	Goles Visitante
-	Goleadores         
Creando la base de datos y las colecciones
use JBFIFAWC2022
db.createCollection("Selecciones")
db.createCollection("Sedes")
db.createCollection("Arbitros")
db.createCollection("Jugadores")
db.createCollection("Staff")
db.createCollection("Fixture")
db.createCollection("Resultados")
 

Insertando datos en las colecciones
1.	Selecciones
db.Selecciones.insertOne({
  "nombre": "Argentina",
  "Colores": "Celeste y blanco",
  "Palmares": "1978, 1986",
  "Escalafon": "1",
  "PJ": 0,
  "PG": 0,
  "PE": 0,
  "PP": 0,
  "GF": 0,
  "DF": 0,
  "PTS": 0,
})
 
 
2.	Sedes
db.Sedes.insertOne({
  "name": "Estadio Al Bayt",
  "ubicacion": "Jor,Qatar",
  "capacidad": "68895 Espectadores",
})  
 
3.	Árbitros
db.Arbitros.insertOne({
  "Nombre": "Abdulrahman Al-Jassim",
  "Nacionalidad": "Catarí",
  "Escalafon FIFA": 36,
})
 
 
4.	Jugadores
db.Jugadores.insertOne({
  "Nombre": "Lionel Messi",
  "Selección": "Argentina",
  "Posición": "Mediocampista",
  "Nacimiento": "24/jun/1987",
  "Club Actual": "PSG - Francia",
  "Goles": 0,
})
 
 
5.	Staff
db.Staff.insertOne({
  "Nombre": "Lionel Scaloni",
  "Seleccion": "Argentina",
  "Rol": "Director Técnico",
})
 
 
6.	Fixture
db.Fixture.insertOne({
  "Fecha": "20/11/2022",
  "Sede": "Estadio Al Bayt, Jor",
  "Fase": "Fase de Grupos",
  "Equipo Local": "Qatar",
  "Equipo Visitante": "Ecuador",
  "Hora": "20:00",
  "Arbitros": "",
})
 
 
7.	Resultados
db.Resultados.insertOne({
  "FixtureID": "",
  "Goles Local": 0,
  "Goles Visitante": 2,
  "Goleadores": "",
})



 

