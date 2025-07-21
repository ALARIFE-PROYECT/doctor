# 🩺 Doctor - BigByte Framework

**Doctor** es una librería del ecosistema **BigByte** que actúa como un lanzador inteligente de scripts Node.js. Proporciona un entorno de monitoreo en tiempo real sobre el proceso lanzado, facilitando la inspección de rendimiento y actividad del proceso, ideal para desarrolladores backend que trabajan con APIs o servicios Node.

## 🚀 Características

- Ejecuta cualquier script Node.js desde CLI.
- Lanza automáticamente una interfaz web de monitoreo.
- Inspección en tiempo real de:
  - Uso de **CPU** y **memoria**.
  - Estado del **event loop**.
  - Información de **requests** HTTP (para APIs REST).
- Monitorización basada en **PID** del proceso lanzado.
- Puerto de monitoreo configurable (`--port`).

## 📦 Instalación

```bash
npm install -g @bigbyte/doctor
```

## 🛠️ Uso básico

```bash
doctor ./mi-script.js
```

Esto ejecutará `mi-script.js` y levantará una web en `http://localhost:8088` mostrando el estado del proceso.

### Cambiar el puerto del monitor

```bash
doctor ./mi-script.js --port 3000
```

## 📊 Interfaz de monitoreo

Una vez lanzado el proceso, accede a:

```
http://localhost:8088
```

(o al puerto indicado)

### Visualiza:

- Gráficas de CPU y memoria en tiempo real.
- Estado del Event Loop (delay, bloqueos).
- Estadísticas de peticiones (si se trata de una API REST):
  - Número total de requests.
  - Tiempo de respuesta.
  - Rutas y métodos utilizados.

## 📁 Estructura del proyecto

```bash
mi-proyecto/
├── script.js      # Script a ejecutar
└── ...
```

## 🧩 Integración

Doctor es parte del framework **BigByte** y se puede usar como lanzador en entornos de desarrollo, testing o benchmarking.

## 📜 Licencia

Este proyecto está licenciado bajo los términos de la [Apache License 2.0](./LICENSE).
