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
