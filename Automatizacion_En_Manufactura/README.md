# Módulo: Introducción a la automatización en Manufactura

En esta sección se puede encontrar
<ul>
  <li> Pirámide de automatizacion o ISA-95 </li>

  <img width="3325" height="2111" alt="Blank diagram" src="https://github.com/user-attachments/assets/3f452458-c187-47b5-b6c8-15c62884ffe5" />


  <li> Arquitectura de comunicaciones y descripción de las comunicaciones utilizadas, identificando protocolos, canales, niveles de la pirámide de automatización donde son utilizadas.</li>

  ![Arquitectura de Conexiones](https://github.com/user-attachments/assets/7c316fe6-835d-43db-8a35-845b30165aa5)

Dentro de la red LAN se organiza toda la operación centralizada del proceso, conectando de forma directa los sistemas de control, simulación y supervisión. En esta capa, el PC1 funciona como el punto neurálgico: allí se ejecuta Ignition en su versión local, que actúa como plataforma SCADA principal para visualizar variables en tiempo real, gestionar historiales y coordinar la comunicación entre módulos. Este servidor recibe datos provenientes de dos servidores OPC diferentes: por un lado, el servidor OPC-UA nativo de Ignition, y por otro, el servidor OPC-DA administrado por RSLinx Gateway.
En esa misma máquina también corre Logix Emulate Studio 5000, que simula el comportamiento del PLC y envía sus tags hacia Ignition y hacia cualquier cliente OPC conectado. Studio 5000 Designer opera sobre la misma arquitectura, permitiendo modificar la lógica del controlador de manera integrada con las herramientas de simulación y supervisión.

El PC2 complementa esta estructura actuando como cliente OPC-UA dedicado, conectado de forma continua a Ignition para extraer datos de proceso que luego alimentan Siemens NX. Esta conexión habilita la sincronización entre el estado real o simulado del sistema y los modelos digitales, soportando flujos de trabajo como verificación dinámica, validaciones de manufactura y análisis basados en el gemelo digital.

Ambas estaciones interactúan entre sí mediante la red interna, permitiendo que la supervisión local, la simulación del controlador y la ingeniería digital funcionen como un único ecosistema. Dentro de esta misma red, una tableta con acceso WiFi puede operar como interfaz SCADA local, ofreciendo movilidad y acceso inmediato a los indicadores del proceso sin necesidad de hardware adicional.

En paralelo, la solución se extiende hacia el exterior gracias a una integración MQTT con Azure. Módulos locales de transmisión y enrutamiento publican datos operativos hacia la nube, donde un sistema SCADA remoto puede supervisar el proceso desde un dispositivo externo con conectividad 4G. Esta doble capa de supervisión ofrece tanto control en planta, accesible desde tabletas conectadas a la red WiFi, como visibilidad remota para análisis avanzado, mantenimiento predictivo y toma de decisiones desde cualquier ubicación. 
El resultado es una arquitectura híbrida, escalable y preparada para Industria 4.0, capaz de unir simulación, operación real y analítica en un único ecosistema conectado.

  <li>Diagramas de instrumentación</li>
  
![PI D (1)](https://github.com/user-attachments/assets/4f74e406-c3d9-42d7-b788-184d9844d666)

  
</ul>
