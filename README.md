# Flow4_NodeRed
Este repositorio contiene el ejercicio del flow 4 de NodeRed, basandose en el contenido de Internet de las cosas de [Codigo IoT](http://edu.codigoiot.com "Codigo IoT")

## Introducción
Este flow consisten en un tablero que representa en forma de gráficos,  la información de temperatura y humedad locales. Para ello se recibe información por MQTT con un broker local.
## Material necesario
- Ubuntu 20.04
- NodeJS
 - NPM
 - NodeRed
 - Nodos de Dashboard
- Mosquito MQTT

## Referencias
Enlaces de apoyo para las configuraciones:
- [Instalación de Virtual Box y Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=812 "nstalación de Virtual Box y Ubuntu 20.04")
- [Instalación de NodeRed](https://edu.codigoiot.com/course/view.php?id=817 "Instalación de NodeRed")
- [Introducción de NodeRed](https://edu.codigoiot.com/course/view.php?id=278 "Introducción de NodeRed")
- [Introducción a Mosquitto](https://edu.codigoiot.com/course/view.php?id=851 "Introducción a Mosquitto")

## Instrucciones
### Requisitos previos
1. **Instalación de NodeJS. **Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM
2. **Instalación de NodeRed.**La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2
3. **Instalación de nodos node-red-dashboard**. Para ello, dirigete a la opcion "Manage Palet" de NodeRed y en la pestaña Install busca node-red-dashboard. Finalmente haz clic en instalar.
4. Instalación de Broker local Mosquitto MQTT.

### Intrucciones de preparación del entorno
1. Arrancar NodeRed con el comando `node-red`
2. Importar el flow desde el repositorio
3. Hacer clic en el boton Deploy

### Intrucciones de operación
- Para observar el resultado del flow, es necesario abrir un navegador  y dirigirse a localhost:1880/ui
- Enviar por MQTT un mensaje que contenga JSON con variables ID, Temp, Hum.

### Notas
- El flow se suscribe al tema codigoIoT/Mor/mqtt/flow4
- El mensaje mqtt usando para este flow es: `mosquitto_pub -h localhost -t codigoIoT/Mor/mqtt/flow4 -m '{"ID":"Hugo Vargas","temp":18,"hum":78}'`
- Para que la gráfica muestre un progreso, es recomendable enviar al menos 2 mensajes
### Resultados y Evidencias
**Nodos del flow**
![](https://github.com/HilarioBarcenas/flow4_NodeRed/blob/main/NodosFlow4.png?raw=true)

**Tablero resulado del flow**
![](https://github.com/HilarioBarcenas/flow4_NodeRed/blob/main/Dashboard.png?raw=true)

### Créditos
**Desarrollado por** `Hilario Barcenas`
