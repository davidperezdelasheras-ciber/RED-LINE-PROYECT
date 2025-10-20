# 🚆 Proyecto Línea Roja

## 🧩 Descripción general
**Línea Roja** es un entorno de simulación ferroviaria diseñado para integrar **ciberseguridad, automatización y formación técnica** en un mismo laboratorio.  

El proyecto recrea un sistema de control ferroviario (HMI/SCADA) mediante **Node-RED** y comunicaciones **MQTT**, permitiendo visualizar y gestionar un tren virtual con parámetros de velocidad, posición, estado de puertas, alertas y semáforos.  

A la vez, sirve como plataforma educativa para pruebas de **Blue Team**, detección de anomalías y ejercicios de respuesta ante incidentes.

---

## ⚙️ Características principales

### 🚉 Simulación ferroviaria interactiva
- Panel HMI (conductor) creado con **Node-RED Dashboard**.  
- Controles: **Acelerar**, **Frenar**, **Abrir/Cerrar puertas**, **Desacoplar vagones**.  
- Visualización en mapa (trayecto *Madrid → Toledo* con posición dinámica del tren).  
- Indicadores de **velocidad**, **estado de semáforos** y **alertas de seguridad**.

### 🔗 Infraestructura de comunicación
- Broker **Mosquitto MQTT** para el intercambio de mensajes entre módulos.  
- Tópicos utilizados:
  - `train/telemetry` → información enviada desde el tren (velocidad, posición, estado).
  - `train/control` → órdenes desde el puesto de mando (acelerar, frenar, etc.).  
- Integración con sensores virtuales y scripts de automatización.

### 🛡️ Entorno de laboratorio ciberseguro
- Despliegue en entorno **virtualizado con VirtualBox**:
  - **Ubuntu Server / Node-RED** → lado del tren (control SCADA/HMI).
  - **Kali Linux** → lado atacante (pentesting y simulación de amenazas).
- Escenarios orientados a **Blue Team**:
  - Simulación de ataques DoS / DDoS y Fuerza bruta sobre contarseñas de usuarios.
  - Manipulación de telemetría.
  - Fuerza bruta sobre canales de control.
- Integración prevista con herramientas **SIEM** y **SIRP**.

### 🎨 Visualización y diseño
- Interfaz web minimalista y funcional.  
- Estilo visual inspirado en **señalización ferroviaria** (fondo blanco, bordes rojos, iconografía clara).  
- Personalización completa con el branding **CIBERBOOT SLU** (azul eléctrico).

---

## 🎯 Objetivos del proyecto

1. Crear un entorno educativo para comprender **ataques y defensas en sistemas industriales** (ICS/SCADA).  
2. Fomentar el aprendizaje de **Node-RED**, **MQTT** y **seguridad IoT e IoP**.  
3. Entrenar **respuestas ante incidentes** en entornos simulados.  
4. Desarrollar un prototipo visual de **sistema ferroviario conectado y ciberprotegido**.  

---

## 📁 Estructura del proyecto
/linea-roja
│
├── node-red/ # Flujos, UI y scripts del simulador
├── mqtt/ # Configuración del broker Mosquitto
├── docs/ # Documentación y diccionarios 
└── README.txt # Este archivo


---

## Tecnologías utilizadas

- **Node-RED** (v3+)
- **Eclipse Mosquitto MQTT**
- **Ubuntu Server 24.04 LTS**
- **VirtualBox**
- **Kali Linux (entorno atacante)**
- **HTML / CSS / JavaScript** para UI
- **CIBERBOOT Branding** (logos, colores, tipografía)

---

## 👤 Autor

**David Pérez**  
Analista OSINT | Ciberinteligencia y Seguridad Digital  
Proyecto desarrollado bajo la marca **CIBERBOOT SLU**  
© 2025 — Todos los derechos reservados  
---

## Licencia
Este proyecto se distribuye para fines **educativos y demostrativos**.  
Queda prohibido su uso en entornos productivos o con fines ilícitos.


