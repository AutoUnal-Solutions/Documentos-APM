# Módulo: Gestión y evaluación de la producción automatizada

El proyecto partió de los datos recolectados durante la visita a la planta de Industrias RAMFE, ubicada en la Cra 69 #17a-96 en Bogotá, Colombia. Esta visita permitió comprender de primera mano el funcionamiento general de la planta, la disposición de su maquinaria, los flujos de trabajo y las tareas realizadas por los colaboradores en cada etapa del proceso productivo. A partir de esta información se llevó a cabo un análisis preliminar que permitió identificar las áreas con mayor potencial de mejora. Para efectos del estudio se seleccionó como caso principal el proceso de fabricación del motorreductor Sin-Fin Corona, del cual se estimo una producción de 75 unidades al mes. Su elección permitió obtener una visión clara del comportamiento actual de la línea, así como de las oportunidades para implementar automatización y optimización operativa. Los hallazgos obtenidos se organizaron y sintetizaron en una serie de esquemas diagnósticos que sirven como base para la propuesta de mejora:
Diagrama de Spaguetti
Diagrama Pre-VSM
Estos documentos, presentados a continuación, permiten visualizar el estado actual del proceso, comprender sus flujos y detectar las principales ineficiencias, sirviendo como punto de partida para el diseño de soluciones orientadas a la modernización y aumento de productividad dentro de la planta.



<ul>

  <li> Diagrama de Espagueti Pre-Automatización  </li>

  ![DIAGRAMAS APM](https://github.com/user-attachments/assets/1741c60b-89c4-4184-818a-9fcdaeb3eb67)
  ![DIAGRAMAS APM (1)](https://github.com/user-attachments/assets/a41859e6-c0ec-4741-b895-dcd9bc7c2464)

  <li> Diagrama Pre-VSM </li>
  
  ![DiagramasPreAutomatizacion-Pre-VSM (2)](https://github.com/user-attachments/assets/57d8b1de-00aa-44f9-bf8e-06029a1e7d7f)

El diagrama Pre-VSM permitió identificar un tiempo de operación especialmente elevado en la etapa de rectificado, lo que sugería una posible restricción dentro del flujo de producción. Para validar esta hipótesis, se realizó una simulación del proceso utilizando Plant Simulation, confirmando la presencia de un cuello de botella en esta fase.

La gráfica obtenida muestra que el rectificador de ejes permanece ocupado durante la mayor parte del tiempo disponible. En contraste, las demás máquinas presentan una baja tasa de utilización, ya que pasan largos periodos en modo de espera o bloqueadas debido a la acumulación de piezas antes del rectificado. Este desbalance evidencia que la etapa de rectificado limita la capacidad global del sistema y afecta directamente los tiempos de ciclo y la eficiencia total de la línea. Este hallazgo resultó fundamental para orientar las decisiones del proyecto, ya que coincidía con la necesidad de incorporar automatización y diseñar la celda robótica propuesta.

Antes de avanzar hacia la solución planteada, se presenta a continuación la simulación del proceso actual de la planta junto con los indicadores resultantes, los cuales sirven como línea base para evaluar el impacto de las mejoras posteriores.

  <li> Simulación Pre-Automatización Plant Simulation Sin Fin - Corona </li>
  
  [Video pre-automatización](https://www.youtube.com/watch?v=Qo0eKrPZasQ)

Los indicadores obtenidos evidencian una falencia importante en la disponibilidad de las máquinas, ya que la mayoría de estaciones presentan tiempos prolongados de bloqueo o espera. Esta condición reduce significativamente el OEE y limita la capacidad real de producción de la planta.

  <img width="1940" height="393" alt="image" src="https://github.com/user-attachments/assets/fd3df7dc-34e3-41e1-9fcf-b22de2a6e8d0" />

  Con base en el análisis previo y proyectando una demanda mensual de 500 motorreductores distribuidos en tres tipos de producto, se llevó a cabo la planificación de un nuevo layout industrial. Este rediseño incluye la adquisición de maquinaria adicional, la desincorporación de equipos con bajo desempeño y, en general, una reorganización completa de la línea para alcanzar los niveles de producción requeridos.

Las mejoras propuestas contemplan un aumento en la capacidad productiva por etapa, así como la incorporación de un sistema de automatización mediante una celda robótica y un sistema SCADA elementos clave para garantizar continuidad operativa, trazabilidad y eficiencia.

El nuevo diagrama de Spaguetti evidencia una secuencia más ordenada en el flujo del proceso, reduciendo desplazamientos innecesarios y optimizando el uso del espacio. Por su parte, el nuevo diagrama VSM resalta mejoras significativas en los tiempos, especialmente en la etapa de rectificado, además de un ajuste favorable en el takt time general.
  
  <li> Diagrama de Spaguetti Post-Automatización. </li>
  
  <img width="8950" height="4584" alt="image" src="https://github.com/user-attachments/assets/7f4e3826-6744-4273-8d28-3509450f6631" />


  <li> Diagrama Post-VSM. </li>
  
  <img width="3468" height="3192" alt="image" src="https://github.com/user-attachments/assets/a4bad5a7-9498-497d-8f94-d103eae637a7" />

  Finalmente, se llevó a cabo una nueva simulación del proceso en Plant Simulation, cuyos resultados y gráficas se presentan a continuación y permiten evaluar el OEE.Si bien este incremento refleja una mejora significativa en la disponibilidad, consecuencia directa de la reorganización del layout y de la reducción de bloqueos y tiempos de espera, también se observó una disminución en los indicadores de desempeño y calidad. Esto indica que, aunque el rediseño permitió aliviar el cuello de botella principal y aumentar la capacidad productiva, aún existen oportunidades importantes de optimización dentro del proceso. Para alcanzar niveles de eficiencia superiores será necesario avanzar hacia una mayor automatización, incorporar nueva maquinaria especializada y considerar una ampliación de la planta que permita distribuir mejor las operaciones.

  <img width="3880" height="786" alt="image" src="https://github.com/user-attachments/assets/4143b80d-acb2-4a71-b988-106651765f57" />


  <li> Simulación Post-Automatización Plant Simulation
    
  Se puede acceder al video en el siguiente [Enlace](https://www.youtube.com/watch?v=CJXzM05k0is) 
    
  
  <li> Diagrama de operaciones de proceso. </li>
  
  ![DIAGRAMAS APM](https://github.com/user-attachments/assets/e3d41216-7699-4aba-9d1c-d40f800368bb)

  ![DIAGRAMAS APM (1)](https://github.com/user-attachments/assets/5292fd2b-3139-4029-a4e9-02d2594de62c)

  <li> Diagrama de análisis de proceso.</li>

  Los diagramas de análisis de proceso se pueden visualizar en el [siguiente enlace.](https://docs.google.com/document/d/1aUp_YgVJHbEZInIFsLJUMVwwGUu5Rn2-zNvv4G0EORY/edit?usp=sharing)


  
  


  
</ul>
