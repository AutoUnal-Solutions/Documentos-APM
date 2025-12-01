# Módulo: Celda de Manufactura Robotizada

Nuestra celda de manufactura robotizada está diseñada para el proceso de "machine tending" durante el rectificado de los engranajes de los motorreductores a producir. Este enfoque optimiza la eficiencia, precisión y seguridad de la producción, ya que el proceso es repetitivo y requiere alta exactitud al ubicar los engranajes en las máquinas CNC programadas para el rectificado. La robotización en nuestro proyecto aporta los siguientes beneficios:

- Automatización de la eficiencia y productividad: al ser una tarea repetitiva, el robot mejora la consistencia y velocidad de la operación.
- Mejora de la seguridad: al eliminar la necesidad de un operador para esta tarea, se reduce el riesgo de accidentes y daño físico relacionado con el uso y manipulación de equipos industriales.
- Mayor precisión y consistencia: El proceso de posicionar los engranajes en las máquinas CNC para su rectificado requiere una precisión muy alta, y la celda robotizada puede asegurar este nivel de exactitud de manera constante.

En resumen, la lógica que sigue la celda robotizada es la siguiente: inicialmente, el manipulador recibe los engranajes a través de cintas transportadoras. Estos engranajes provienen del proceso de dentado. A lo largo de las cintas, se ubican varios sensores que envían señales al controlador del robot, informando sobre el tipo de engranaje que se acerca al manipulador. Al final de la cinta transportadora, se encuentra un sensor de parada que, al detectar un engranaje, detiene las cintas y envía una señal al robot para iniciar el proceso de "machine tending". Dependiendo de la señal recibida, el manipulador coloca el engranaje en la máquina CNC correspondiente. Luego, el robot queda a la espera de posicionar otro engranaje o retirar un engranaje que ya haya sido rectificado.

Para ello, se seleccionó el robot IRB 4600 de ABB, un robot diseñado para celdas de fabricación compactas con un alto volumen de productividad. A pesar de contar con un manipulador relativamente grande, ocupa poco espacio. Este robot fue seleccionado principalmente por su alcance y su carga útil. Específicamente, la referencia seleccionada fue el IRB 4600-20/2.50, que tiene un alcance de 2.51 m, lo cual es perfecto para la distribución diseñada para la celda robotizada, y una carga útil de 20 kg, suficiente para las piezas que se van a posicionar en las máquinas CNC. Esto, considerando que el engranaje más pesado tiene una masa de aproximadamente 6 kilogramos, además del peso del gripper. Al momento de realizar la compra de este robot, se incluye su controlador, el IRC5.


<p align="center">
  
  ![IRB4600](https://github.com/user-attachments/assets/a8e7b257-50c8-476e-b52d-21e461a38c6a)
  
  Manipulador IRB 4600

</p>





<img align="center" width="736" height="415" alt="IRC5_16x9-S" src="https://github.com/user-attachments/assets/85ff936f-4115-4aa0-af64-4c5d73069947" />

Controlador IRC5

| Elemento | Peso (kg) |
| ---- | ---- |
| Engranaje Cónico | 3.73 |
| Engranaje Helicoidal | 3.35 |
| Corona | 5.99 |
| Gripper 3DG25 | 1.6 |

Para manipular adecuadamente los engranajes, se seleccionó el gripper OnRobot 3DG25, ideal para manipular piezas cilíndricas como los engranajes. Además, este gripper está diseñado para funcionar en entornos de fabricación exigentes, especialmente en el manejo de máquinas CNC con piezas de trabajo pesadas. Tiene capacidad para agarrar objetos con un diámetro máximo de 155 mm, pero puede manipular elementos desde orificios internos. Esto significa que, si en algún momento se debe manipular un engranaje que supere los 155 mm de diámetro exterior, puede hacerlo desde su orificio central. Además, es capaz de manipular piezas de hasta 25 kg. Esta pinza es completamente eléctrica y proporciona un control total sobre la sujeción, lo que permite un agarre rápido de las piezas y garantiza un agarre firme y estable, lo que permite una colocación precisa en las máquinas CNC. Su fuerza máxima de agarre es de 450 N.

<p align="center">
<img width="551" height="680" alt="image" src="https://github.com/user-attachments/assets/8db4f2a2-6b00-45af-ab66-ca62255dcea6" />
</p>

Gripper OnRobot 3FG25







</ul>
