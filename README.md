# Pregunta 1: Definition of System Requirements

| **System Requirement**              | **Especificación de Requisitos**                                                                                                                                                                |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Capacidades de suministro de energía** | **RFID Bands:** Usan etiquetas pasivas sin batería, alimentadas por el lector. <br>**Smart Food Dispensers y Smart Coffee Makers:** Alimentados con fuente estándar de 220V. <br>**Estación de control del evento:** Requiere energía para el servidor de datos y los equipos de red WiFi. |
| **Restricciones de time-delay**         | **RFID Bands:** Ingreso y pagos sin contacto con tiempos de respuesta mínimos. <br>**Smart Dispensers/Coffee Makers:** Procesamiento en tiempo real del uso de RFID. <br>**Check-In Platform:** Validación QR ágil para 60 usuarios por estación. <br>**Conectividad:** Sincronización en tiempo real con la nube de Eventify. <br>**Food y Maintenance Platforms:** Reporte de estado e inventario en tiempo real. |


# Pregunta 2: Definition of Physical Layer Requirements

| **Physical Layer Requirement**     | **Especificación de Requisitos**                                                                                                                                                                                                                                                                                  |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Número y tipos de nodos sensores y actuators** | **RFID Bands:** 500 a 1000 por evento.<br>**Smart Food Dispensers:** 1 por cada 50 registrados, con RFID RC522, 4 sensores DHT-22, 20 Micro Servos y 1 LCD 1602.<br>**Smart Coffee Makers:** Igual que dispensadores.<br>**Estaciones de control:** 1 por cada 60 registrados, con lector QR. |
| **Target uncertainty**            | **DHT-22:** Humedad 0-100% RH, Temperatura -40°C a 80°C.<br>**RFID RC522:** Frecuencia 13.56 MHz para lectura de etiquetas pasivas.                                                                                                                                                                                |
| **Target accuracy and precision** | **Micro Servo Motors:** Rango de rotación 180°, velocidad 10 sec/60° a 4.8V, temperatura de operación -30 a 60°C.<br>**LCD 1602:** Pantalla 16x2 con interfaz I2C, contraste ajustable.                                                                                                                            |
| **Processing Power**              | **ESP32:** WiFi 802.11n, Bluetooth 4.2, doble núcleo Xtensa LX6 a 240 MHz, 520 KB SRAM, 448 KB ROM, 34 GPIO, sensores táctiles, PWM LED. <br>Capaz de: lectura de sensores, control de servos, interfaz RFID/LCD, comunicación WiFi, lógica de negocio y notificaciones.                                            |


# Pregunta 3: Definition of Information Layer Requirements


| **Information Layer Requirement**  | **Especificación de Requisitos**                                                                                                                                                                                                                                                  |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Definición de usuarios finales** | **Asistentes al evento:** Registrados, usan app y RFID Band.<br>**Organizadores:** Gestionan configuración y datos del evento.<br>**Check-In Staff:** Validan QR y asignan RFID.<br>**Food Partner Users:** Abastecen dispensadores.<br>**Device Maintenance:** Soporte técnico y mantenimiento. |
| **Servicios para cada usuario**    | **Asistentes:** Registro, QR, check-in, pagos sin efectivo, dispensación.<br>**Organizadores:** Configuración, análisis, carga de datos.<br>**Check-In Staff:** Validación de QR, asignación RFID.<br>**Food Partners:** Monitoreo y abastecimiento.<br>**Maintenance:** Estado y gestión de mantenimiento. |
| **Necesidades de información integrada** | **Registro:** Datos personales y del evento.<br>**Check-In:** Validación QR y asignación RFID.<br>**Pagos:** Saldo vinculado al RFID, integración con facturación.<br>**Mantenimiento:** Estado en tiempo real, historial, programación y gestión correctiva de dispositivos.                                          |


