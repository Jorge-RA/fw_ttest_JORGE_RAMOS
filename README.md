# fw_ttest_JORGE_RAMOS

Instrucciones para ejecutar el proyecto:

- Tener lista la ESP32 para ser programada con Micropython
- Descargar los archivos .py del repositorio. (main.py, ntp_server.py, wifi_connection.py, measures.py)
- Subir los archivos descargados a la memoria de la ESP32. Subidos con el Editor Mu en mi caso, pero puede ser el de su preferencia.
- Correr el programa

Los datos son enviados al siguiente broker: 
- broker.emqx.io 
- https://www.emqx.com/en/mqtt/mqtt-websocket-toolkit
- Credenciales: user="enerbit", password="enerbit"

TOPICS:
- esp/measure/foundry
- esp/measure/pneumatic
- esp/measure/molding
- esp/measure/warehouse
- esp/measure/alert

El MQTTClient de la ESP32 está suscrito al topic "pc", no realiza ninguna función si se le envía un mensaje, pero sí lo imprime por el terminal.

DIAGRAMA DE CONEXIÓN MODBUS ESP32-SIEMENS PAC3200 adjunto.
