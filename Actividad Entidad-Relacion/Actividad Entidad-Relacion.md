







## 1 - Seleccionar una PK para cada entidad
- Compañia(#nomCom)
- Vuelo(#numVuelo, fecha, hora, capacitat)
- Aeropuerto(nomAeropuerto,#idAeropuerto)
- Reserva(fecha, plazas,#idReserva)
- Pasajero(nombre,#DNI)
- Ciudad(nombreCiudad,#idCiudad)
- Pais(#nombrePais)

## 2 - Cada entidad pasa a ser una tabla en el modelo relacional.

## 3 - Cada relación pasa a ser una tabla en el modelo relacional.
- R_Compañia_Pais(nomCom, nomPais)
- R_Compañia_Vuelo(nomCom, numVuelo)
- R_Vuelo_Pasajero(numVuelo, DNI)
- R_Vuelo_Aeropuerto_Origen(numVuelo, idAeropuerto)
- R_Vuelo_Destino(numVuelo, idAeropuerto)
- R_Aeropuerto_Ciudad(idAeropuerto, idCiudad)
- R_Ciudad_Pais(idCiudad, nombrePais)

## 4 - Seleccionar una PK para cada relación entre entidades.
- R_Compañia_Pais(#nomCom, nomPais)
- R_Compañia_Vuelo(nomCom,#numVuelo)
- R_Vuelo_Pasajero(#numVuelo,#DNI)
- R_Vuelo_Aeropuerto_Origen(#numVuelo, idAeropuerto)
- R_Vuelo_Destino(#numVuelo, idAeropuerto)
- R_Aeropuerto_Ciudad(#idAeropuerto, idCiudad)
- R_Ciudad_Pais(#idCiudad, nombrePais)


## 5 - Fusionar, si es posible diferentes tablas del modelo relacional.
- Compañia(#nomCom, nomPais)
- Vuelo(#numVuelo, fecha, hora, capacitat,nomCom,idAeropuertoOrigen, idAeropuertoDestino)
- Aeropuerto(nomAeropuerto,#idAeropuerto,idCiudad)
- Reserva(fecha, plazas,#idReserva, DNI,numVuelo)
- Pasajero(nombre,#DNI)
- Ciudad(nombreCiudad,#idCiudad, nombrePais)
- Pais(#nombrePais)