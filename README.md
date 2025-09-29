[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=20745264&assignment_repo_type=AssignmentRepo)
# Lab04: Visualización de Datos en Raspberry Pi con Node-RED 

## Integrantes

- [Michael Handrety Fonseca Arana](https://github.com/MichaelJF50)  
- [Laura Daniela Rincón](https://github.com/Laura03rincon)  

## Documentación

<!-- Incluir diagramas y adjuntar al repositorio, en una carpeta src, el flujo que crearon -->

En el presente laboratorio, se realizo conexión inhalambrica entre nuestra Raspberry Pi, equipo de computo local, SSH y la interfaz web de Node-RED.

### Marco teorico
**Node-red**: Node-RED es una herramienta de programación visual basada en Node.js que permite conectar dispositivos, APIs y servicios usando «nodos» que arrastras y encadenas en un editor tipo diagrama de flujo. 

Node-RED en una Raspberry Pi funciona como un servidor que corre sobre Node.js y se abre desde un navegador en la dirección (http://localhost:1880). Desde allí puedes usar un editor gráfico basado en bloques llamados nodos. Estos nodos se arrastran y conectan para crear flujos de datos que se ejecutan en tiempo real. Los nodos de entrada permiten leer información (por ejemplo, de los pines GPIO, MQTT o HTTP). Los nodos de proceso sirven para transformar los datos (hacer cálculos o aplicar lógica con funciones en JavaScript). Finalmente, los nodos de salida permiten mostrar o enviar la información, ya sea en un dashboard, a una base de datos o incluso activando otro pin GPIO.

**Nodos de entrada**: Leen datos (GPIO de la Pi, MQTT, HTTP, etc.).

**Nodos de proceso**: transforman o procesan la información (funciones JavaScript, filtros, cálculos).

**Nodos de salida**: envían los resultados a la pantalla, dashboard, GPIO, base de datos, correo, etc.


## Conclusiones
