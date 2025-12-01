# Módulo: Celda de Manufactura Robotizada

Nuestra celda de manufactura robotizada está diseñada para el proceso de "machine tending" durante el rectificado de los engranajes de los motorreductores a producir. Este enfoque optimiza la eficiencia, precisión y seguridad de la producción, ya que el proceso es repetitivo y requiere alta exactitud al ubicar los engranajes en las máquinas CNC programadas para el rectificado. La robotización en nuestro proyecto aporta los siguientes beneficios:

- Automatización de la eficiencia y productividad: al ser una tarea repetitiva, el robot mejora la consistencia y velocidad de la operación.
- Mejora de la seguridad: al eliminar la necesidad de un operador para esta tarea, se reduce el riesgo de accidentes y daño físico relacionado con el uso y manipulación de equipos industriales.
- Mayor precisión y consistencia: El proceso de posicionar los engranajes en las máquinas CNC para su rectificado requiere una precisión muy alta, y la celda robotizada puede asegurar este nivel de exactitud de manera constante.

En resumen, la lógica que sigue la celda robotizada es la siguiente: inicialmente, el manipulador recibe los engranajes a través de cintas transportadoras. Estos engranajes provienen del proceso de dentado. A lo largo de las cintas, se ubican varios sensores que envían señales al controlador del robot, informando sobre el tipo de engranaje que se acerca al manipulador. Al final de la cinta transportadora, se encuentra un sensor de parada que, al detectar un engranaje, detiene las cintas y envía una señal al robot para iniciar el proceso de "machine tending". Dependiendo de la señal recibida, el manipulador coloca el engranaje en la máquina CNC correspondiente. Luego, el robot queda a la espera de posicionar otro engranaje o retirar un engranaje que ya haya sido rectificado.

Para ello, se seleccionó el robot IRB 4600 de ABB, un robot diseñado para celdas de fabricación compactas con un alto volumen de productividad. A pesar de contar con un manipulador relativamente grande, ocupa poco espacio. Este robot fue seleccionado principalmente por su alcance y su carga útil. Específicamente, la referencia seleccionada fue el IRB 4600-20/2.50, que tiene un alcance de 2.51 m, lo cual es perfecto para la distribución diseñada para la celda robotizada, y una carga útil de 20 kg, suficiente para las piezas que se van a posicionar en las máquinas CNC. Esto, considerando que el engranaje más pesado tiene una masa de aproximadamente 6 kilogramos, además del peso del gripper. Al momento de realizar la compra de este robot, se incluye su controlador, el IRC5.



  ![IRB4600](https://github.com/user-attachments/assets/96c7e906-2249-4bd4-87f8-4a7dc7bfad3a)
  
  Manipulador IRB 4600 


<br>

<p align="center">
<img width="736" height="415" alt="IRC5_16x9-S" src="https://github.com/user-attachments/assets/85ff936f-4115-4aa0-af64-4c5d73069947" />
</p>

<center> Controlador IRC5 </center>

<br>

| Elemento | Peso (kg) |
| ---- | ---- |
| Engranaje Cónico | 3.73 |
| Engranaje Helicoidal | 3.35 |
| Corona | 5.99 |
| Gripper 3DG25 | 1.6 |

Para manipular adecuadamente los engranajes, se seleccionó el gripper OnRobot 3DG25, ideal para manipular piezas cilíndricas como los engranajes. Además, este gripper está diseñado para funcionar en entornos de fabricación exigentes, especialmente en el manejo de máquinas CNC con piezas de trabajo pesadas. Tiene capacidad para agarrar objetos con un diámetro máximo de 155 mm, pero puede manipular elementos desde orificios internos. Esto significa que, si en algún momento se debe manipular un engranaje que supere los 155 mm de diámetro exterior, puede hacerlo desde su orificio central. Además, es capaz de manipular piezas de hasta 25 kg. Esta pinza es completamente eléctrica y proporciona un control total sobre la sujeción, lo que permite un agarre rápido de las piezas y garantiza un agarre firme y estable, lo que permite una colocación precisa en las máquinas CNC. Su fuerza máxima de agarre es de 450 N.

<p align="center">
<img width="183" height="226" alt="image" src="https://github.com/user-attachments/assets/8db4f2a2-6b00-45af-ab66-ca62255dcea6" />
</p>

<center> Gripper OnRobot 3FG25 </center>

<br>

### Diseño de celda robotizada en RobotStudio y consideraciones de espacio, flujo de producto, interacción con personal, seguridad funcional y agarre del robot.

La celda de manufactura robotizada fue diseñada y distribuida de tal manera que el robot quede en el centro de la celda, con el fin de maximizar su alcance y poder interactuar con la mayor cantidad posible de máquinas CNC. Como se observa en la figura, alrededor del manipulador se encuentran ubicadas tres máquinas CNC, cada una encargada del rectificado de un tipo específico de engranaje.

Los engranajes ingresan a la celda robotizada a través de cintas transportadoras, provenientes de un proceso de dentado realizado al inicio de la celda de manufactura automatizada. Mediante sensores, el manipulador recibe la señal que indica el tipo de engranaje que va hacia la celda robotizada, con el fin de realizar las trayectorias correspondientes y ubicar el engranaje en su máquina CNC asignada.

Un sensor ubicado al final de la cinta transportadora detiene esta y envía una señal para que el manipulador inicie su rutina de "machine tending". En este momento, el manipulador agarra el engranaje y lo posiciona en la máquina CNC. El controlador del robot, a su vez, envía una señal a la máquina CNC para que comience el proceso de rectificado. Luego, el manipulador regresa a su posición inicial y queda a la espera de una nueva señal para realizar otra acción.

Cuando una máquina CNC termina el proceso de rectificado, envía una señal al controlador del robot indicando que el proceso ha finalizado. En este momento, el manipulador agarra el engranaje rectificado y lo coloca en la banda transportadora de salida.

Es importante aclarar que los engranajes deben llegar al final de la banda transportadora en una posición adecuada para que el manipulador pueda agarrarlos sin problemas. Para ello, se utilizó una canaleta que garantiza que los engranajes siempre lleguen a la misma posición. Debido a que los engranajes tienen diferentes diámetros, se programaron las trayectorias del manipulador para que éste realice el movimiento correspondiente para agarrar el tipo de engranaje que proviene del proceso de dentado. Además, gracias al sensor que detiene la cinta transportadora, los engranajes siempre se detendrán en la misma posición.

### Identificación de peligros y gestión del riesgo.

Con el fin de minimizar los riesgos en la planta, la celda robotizada está protegida por un cercado para evitar que algún operario ingrese a ella. Para acceder, se ha instalado una puerta trasera, la cual cuenta con un sensor RFID, garantizando que solo el personal autorizado pueda ingresar a la celda. Cuando el sensor recibe la señal, el robot se detiene por completo, bloqueando el acceso hasta que la persona autorizada salga de la celda y presione el botón de reset ubicado cerca del sensor RFID.

Además, la celda está equipada con una baliza que indica el estado del sistema:
- Color rojo: cuando el sistema está apagado.
- Color verde: cuando el sistema está encendido.
- Colores verde y amarillo: cuando el manipulador está en movimiento.

La celda también cuenta con varias paradas de emergencia: dos ubicadas en el exterior, cerca de las bandas transportadoras, y una en el pulsador del controlador IRC5.

La celda robotizada está diseñada para operar sin la presencia de un operario dentro de la celda durante su funcionamiento normal. Si es necesario realizar mantenimiento en algún componente, se puede ingresar a la celda apagando automáticamente el robot para garantizar la seguridad.

### Simulación en Robotstudio

Se puede acceder al video en el siguiente [Enlace](https://youtu.be/wzx8rY8hKtg).


</ul>
