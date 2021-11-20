# **Problema de asignación 3-dimensional axial y 3-dimensional planar.**
### **Introducción:**

* El problema de asignación, consiste en asignar ciertos recuros disponibles a unas tareas, siendo el objetivo relizar esta asignación al menor coste posible. Hay que tener en cuenta, que cada recuerso es destinado a una sola tarea y que cada tarea será ejecutada por un solo recurso. Se trata de un caso particular del problema de transporte, donde la cantidad a repartir desde el origen es 1 y la demanda en cada destino es 1 también.<br><br>

* Como caso de partida, el modelo matemático para el problema de asignación 2-dimensional es el siguiente:<br><br>    

   * ***Variables:***   

      <center>

        ![](https://drive.google.com/uc?export=view&id=1iRRclx2Oq06Y4IiLbTvrx4Y0Fdh51nwC)
      </center><br>

   * ***Función objetivo:*** 
      <center>

      ![](https://drive.google.com/uc?export=view&id=1iRnQV24gM_yS6hC3jhO9lXtbteTZbila)
      </center><br>

  * ***Restricciones:***
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1iS9S7dTgsUpq9K3K1ooCXkIixeBRFlkW)
      </center><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1iToxL1P38we64VoMPhmkECWQmBnsX5wO)
      </center><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1iUgfD6PqJ-5fTXhmHyxx5JHVe7F172d2)
      </center><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1iUxACOTwRF0zfBSwuaqDZJHnZR-ZiQ9U)
      </center><br><br>

      <center>

      ![](https://drive.google.com/uc?export=view&id=17NFk7Ms3Jwyb0YP16xWEhOM92sJBcpzw)

      </center><br>

* A continuación se procederá a explicar en qué consiste cada uno y se implementará un código para modelizarlos y resolver un ejemplo, utilizando para ello la herramienta ***OR-tools*** de Google.


### **Problema de asignación 3-dimensional axial:**

* El problema de asignación 3-dimensional axial ***(3AP-axial)*** se trata de una una "*extensión*" del problema de asignación 2-dimensional, donde en este caso se trabaja con 3 conjuntos *I, J y K* **(todos con el mismo número de elementos)**, y obviamente, se busca que se asignen todos los recursos a todas las tareas, de manera que el coste sea mínimo.<br><br>

  <center>

  ![](https://drive.google.com/uc?export=view&id=1iV76KAlRL6wqDsnz6VuMx9e_VjhN-6Ex)
  </center><br>


* Como ejemplo ilustrativo para el 3AP-axial, se plantea un conjunto de transportistas ***(I)***, un conjunto de camiones ***(J)*** y un conjunto de rutas ***(K)***, y se busca que el coste de la asignación entre estos tres conjuntos sea mínimo:<br><br>

  <center>

  ![](https://drive.google.com/uc?export=view&id=1iW0ozOF3HtmDUt6qFmylt90Sf1fdebRo)
  </center><br>

   * ***Variables:***   

      <center>

        ![](https://drive.google.com/uc?export=view&id=1iXK-o8RgHphRspZ4ArFYbO1t2IAi-Esu)
      </center><br>

   * ***Función objetivo:*** 
      <center>

      ![](https://drive.google.com/uc?export=view&id=1iXxSWdE6pWp6vo6AvSEewv1NpdTjtwzo)
      </center><br>
  
  * ***Restricciones:***

      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1i_M7Ba1RkX6uTOFlSRUpd1KTwwc4wghq)
      </center><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1ibHVGSsetcoSot82YCgo7iCFwWI4TYcI)
      </center><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1ibOLkAh6Zqwmme_GvzAjwua7ndLZbzBy)
      </center><br>

      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1idKLVxuddFnTiNuy4vgtnth3UBiVVATp)
      </center><br><br>

      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1iYvfDT6-frtspzHQdOfeOtqvPGuA9QiW)
      </center><br><br>
      
    
### **Problema de asignación 3-dimensional planar:**

* El problema de asignación 3-dimensional planar ***(3AP-planar)*** se trata también de una "*extensión*" del problema de asignación 2-dimensional, donde al igual que en caso axial, también se trabaja con 3 conjuntos *I, J y K* **(todos con el mismo número de elementos)**, y obviamente, se busca que se asignen todos los recursos a todas las tareas, de manera que el coste sea mínimo.<br><br>


* Como ejemplo ilustrativo para el 3AP-planar, se plantea buscar la asignación de transportistas, camiones y rutas, de manera que el coste de la asignación total entre estos tres conjuntos sea mínimo. El modo de empleo sería ofrecer a cada transportista las opciones (camión-ruta) con menor coste que se le han asignado, dado que lo que interesa en este problema es minimizar el coste global, no "el personal", de modo que, no pueden haber transportistas que tengan asignado un mismo camión-ruta.<br><br>

<center>

  ![](https://drive.google.com/uc?export=view&id=1e_ktI1TK8XB6Y_dZjiLlbjKUcpgW2Hpd)
  </center><br>

* Cabe mencionar que para cada transportista se tiene que asignar n camiones y n rutas, existiendo tantas asignaciones como elementos tengan los tres conjuntos, que será n = |I| = |J| = |K|. A continuación se muestra un ejemplo donde el número de elemetos es 4, por lo que habrán 4 conductores (4 matrices), y para cada uno se le asignará 4 pares camión/ruta, de manera que las asignaciones se han realizado minimizando los costes globales: <br><br>

  <center>

  ![](https://drive.google.com/uc?export=view&id=10CvwKAv10PmbkddrQRbVo9FGcnv4Tqgu)
  </center><br>
  <center>

  ![](https://drive.google.com/uc?export=view&id=1m0X7sulUj_rWl2EXqyjot7345ac5iIlG)
  </center><br>
  <center>

  ![](https://drive.google.com/uc?export=view&id=1AlM7BF7nccOLRjbztjf7Lu__xWo31rjU)
  </center><br>
  <center>

  ![](https://drive.google.com/uc?export=view&id=12PMTe_264O8z0syLlyy6U7u8F1TWYOXm)
  </center><br>

* Como se puede observar, las soluciones que se escogen para el problema 3AP-planar corresponden a un **cuadrado latino**, un caso particular (matriz n x n) del **retángulo latino**, que consiste en una matriz n x m donde para cada fila y columna el elemento ij es distinto. Para el caso de las soluciones del problema, la elección que se hace para cada matriz es única en filas y columnas, es decir, no puede haber como solución un mismo elemento en las filas y columnas del conjunto de matrices. El cuadrado latino con las soluciones para el caso de muestra, es el siguiente: <br><br>

  <center>

  ![](https://drive.google.com/uc?export=view&id=12p_bUqYerczyGGCmN0HW9-aVBUxzGTq7)
  </center><br>
  <center>

  ![](https://drive.google.com/uc?export=view&id=1jXSg6F0YSQ383C1H7d42CeJbU3Zu-O3c)
  </center><br>

   * ***Variables:***   

      <center>

      </center><br>

   * ***Función objetivo:*** 
      <center>

      ![](https://drive.google.com/uc?export=view&id=1iXxSWdE6pWp6vo6AvSEewv1NpdTjtwzo)
      </center><br>
  
  * ***Restricciones:***

      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1_5-n1wloxQlAXvgqW4i2x213F47RQ5QG)
      </center><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1Ltw3DytoDSP0omRXdK1iTeHfCv2EaLo_)
      </center><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1_0VU9lsCfXSYGmlEx_jtuSbKk55t50In)
      </center><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1idKLVxuddFnTiNuy4vgtnth3UBiVVATp)
      </center><br><br>
      <center>
      
      ![](https://drive.google.com/uc?export=view&id=1iYvfDT6-frtspzHQdOfeOtqvPGuA9QiW)
      </center><br><br>
