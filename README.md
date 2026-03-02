# Resoluci-n-Maquina-Superhero

# Reconocimiento

Iniciamos haciendo un escaneo de puertos utilizando la herramienta nmap
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 220122" src="https://github.com/user-attachments/assets/b53bf4bc-fc97-4032-a81d-495aba3eca1c" />
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 220315" src="https://github.com/user-attachments/assets/ee0b4856-1e64-4011-a2de-42c65d805eef" />

Una vez ya sabemos los puertos y servicios que se encuntran ejecutando en esta maquina procedimos a ingresar a la pagina web y ver si podiamos encontrar algo importante 
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 220413" src="https://github.com/user-attachments/assets/cc07cb3e-f5e1-442e-b7da-faeb0c97c911" />

Tratamos de hacer fuzzing pero no encontramos nada que nos funcionara para ingresar a la maquina
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 221614" src="https://github.com/user-attachments/assets/7594726a-2071-49e2-baac-46d9f0c1bf22" />

Buscamos en internet información sobre las vulnerabilidades que pudieran tener los servicios, y dentro de ellos encontramos la vulnerabilidad en el puerto FTP numeración vftp 2.3.4 el cual contenia una vulnerabilidad la cual permitia ejecutar un backdoor ejecution command el cual habia que luego de un nombre de usuario los caracteres :) y una contraseña cualquiera.
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 222636" src="https://github.com/user-attachments/assets/fe15a593-5c93-4a96-857d-6f0fa8ed6f3c" />

En otra terminal ponemos en escuchael puerto 6200 el cual nos permitira el acceso a la maquina 
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 224213" src="https://github.com/user-attachments/assets/23d43c1d-a66c-405f-ae78-2fa01b0cd1b8" />
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 224202" src="https://github.com/user-attachments/assets/1bf707dd-cfee-4da0-a9dd-b3804dd4b3d5" />

# Resultados
Ya dentro de la maquina procedimos a verificar que usuario somos y en efecto eramos usuario root, asi que buscamos la carpeta de root donde encontramos un archivo llamado flag.txt 
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 224259" src="https://github.com/user-attachments/assets/4fc428ec-b69e-48ff-9361-9872cd23824a" />

Procedimos a abrirlo y a utilizar la flag para terminar la maquina
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 224317" src="https://github.com/user-attachments/assets/9ffdbc99-4678-4fc0-b550-609a46002413" />
<img width="1920" height="1140" alt="Captura de pantalla 2026-03-01 224349" src="https://github.com/user-attachments/assets/3aab49df-9384-4e3b-8867-ba5428d47f28" />

y de esta manera terminamos de explotar esta maquina.
Me gustaria recalcar que esta es una de las consecuencias de tener un servicio sin las ultimas versiones actualizadas, los cuales corrigen vulnerabilidades encontradas y que son muy criticas para sistemas en producción.
