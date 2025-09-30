[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=20745264&assignment_repo_type=AssignmentRepo)
# Lab04: Visualización de Datos en Raspberry Pi con Node-RED 

## Integrantes

- [Michael Handrety Fonseca Arana](https://github.com/MichaelJF50)  
- [Laura Daniela Rincón Pinilla](https://github.com/Laura03rincon)  

## Documentación

<!-- Incluir diagramas y adjuntar al repositorio, en una carpeta src, el flujo que crearon -->

C:\Users\LAURA RINCON\Documents\DECIMO_SEMESTRE\DIGITALES_III\lab04-raspberry-pi-con-node-red-2025-ii-sd3-g01\lab04-raspberry-pi-con-node-red-2025-ii-sd3-g01

## Documentación

En el presente laboratorio se realizó la conexión inalámbrica entre la Raspberry Pi, el equipo de cómputo local mediante SSH y la interfaz web de Node-RED. Para establecer la comunicación remota se utilizó el protocolo SSH, ejecutando en la terminal el siguiente comando:

 `ssh laura@10.56.108.11`

 Después de ingresar la contraseña, se establece la conexión y se puede acceder a la Raspberry Pi de manera remota.

### Marco teorico
**Node-red**: Node-RED es una herramienta de programación visual basada en Node.js que permite conectar dispositivos, APIs y servicios usando «nodos» que arrastras y encadenas en un editor tipo diagrama de flujo. 

Node-RED en una Raspberry Pi funciona como un servidor que corre sobre Node.js y se abre desde un navegador en la dirección (http://localhost:1880). Desde allí puedes usar un editor gráfico basado en bloques llamados nodos. Estos nodos se arrastran y conectan para crear flujos de datos que se ejecutan en tiempo real. Los nodos de entrada permiten leer información (por ejemplo, de los pines GPIO, MQTT o HTTP). Los nodos de proceso sirven para transformar los datos (hacer cálculos o aplicar lógica con funciones en JavaScript). Finalmente, los nodos de salida permiten mostrar o enviar la información, ya sea en un dashboard, a una base de datos o incluso activando otro pin GPIO.

**Nodos de entrada**: Leen datos (GPIO de la Pi, MQTT, HTTP, etc.).

**Nodos de proceso**: transforman o procesan la información (funciones JavaScript, filtros, cálculos).

**Nodos de salida**: envían los resultados a la pantalla, dashboard, GPIO, base de datos, correo, etc.


### Dificultades  

Una de las principales dificultades encontradas fue mantener Node-RED en ejecución al cerrar la terminal SSH. Inicialmente, al correr `node-red-start`, el servicio quedaba activo únicamente mientras la sesión estaba abierta. Esto se solucionó configurando Node-RED como servicio de *systemd*, lo cual permitió que se ejecutara automáticamente en segundo plano.  

Otra complicación fue la instalación de los nodos de dashboard, que en algunos intentos requirió actualizar npm antes de poder añadirlos correctamente desde la pestaña de *Manage Palette*.  

### Términos técnicos aprendidos  

- **SSH (Secure Shell)**: protocolo que permite la conexión remota segura a la Raspberry Pi desde otro equipo. Ejemplo de uso: `ssh usuario@ip`.  
- **Script remoto con curl y bash**: comando que descarga y ejecuta automáticamente la instalación de Node-RED. Ejemplo: `bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)`.  
- **systemctl**: herramienta de Linux para gestionar servicios en segundo plano, como en `sudo systemctl enable nodered.service`.  
- **Dashboard**: conjunto de nodos en Node-RED que permiten generar interfaces gráficas interactivas accesibles desde el navegador.  

## Conclusiones  

El laboratorio permitió comprender cómo establecer una conexión remota con la Raspberry Pi y cómo instalar y configurar Node-RED como servicio en segundo plano. Además, se logró crear un flujo funcional con nodos de entrada, procesamiento y salida, verificando el almacenamiento de datos y su visualización en un dashboard.  

Se concluye que Node-RED es una herramienta poderosa para integrar hardware y software mediante flujos visuales, y que su ejecución en la Raspberry Pi lo convierte en una opción práctica para proyectos de monitoreo y control en tiempo real.  


sx