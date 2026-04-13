# SATS-Chile
Sistema de Alerta Temprana de Sismos (SATS-Chile) basado en Inteligencia Artificial y Arquitectura Kappa. Proyecto de investigación con fines educativos para la gestión de riesgos naturales.

# SATS-Chile: Sistema de Alerta Temprana de Sismos

[![Status](https://img.shields.io/badge/Status-Development-orange)](#)
[![Architecture](https://img.shields.io/badge/Architecture-Kappa-blue)](#)

## 📝 Descripción del Proyecto
El **Sistema de Alerta Temprana de Sismos (SATS-Chile)** es una solución basada en Inteligencia Artificial diseñada para la detección inmediata de ondas P. El objetivo es emitir alertas críticas antes de la llegada de las ondas S (destructivas), permitiendo una respuesta automatizada optimizada para la infraestructura televisiva nacional y dispositivos móviles.

## 🏗️ Arquitectura Seleccionada
El sistema implementa una **Arquitectura Kappa**. Este diseño permite el procesamiento de flujos de datos en tiempo real (streaming), garantizando una latencia mínima al eliminar capas de procesamiento por lotes (batch) en el camino crítico de la alerta.

## 🛠️ Requisitos y Configuración del Entorno Técnico
Para el despliegue del sistema se requieren las siguientes herramientas:

*   **Docker & Docker Compose**: Para la contenerización de microservicios, Kafka y bases de datos.
*   **Python 3.10+**: Lenguaje base para el desarrollo del núcleo de IA y servicios de backend.
*   **Apache Kafka**: Message broker encargado del streaming de datos de alta disponibilidad.
*   **PostgreSQL**: Almacenamiento relacional para el historial de eventos y auditoría.
*   **Redis**: Base de datos en memoria para la gestión de estados de alerta con latencia de microsegundos.

## 🚀 Instrucciones de Instalación

Siga estos pasos para configurar el entorno de desarrollo local:

1.  **Clonar el repositorio:**
    ```bash
    git clone [url-del-repositorio-aquí]
    cd sats-chile
    ```

2.  **Levantar la infraestructura (Contenedores):**
    ```bash
    docker-compose up -d
    ```

3.  **Instalar dependencias de Python:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Ejecutar el simulador de sensor sísmico:**
    ```bash
    python scripts/simulate_sensor.py
    ```

## 📂 Estructura del Repositorio

```text
├── data/               # Datasets de ejemplo para pruebas locales
├── docker/             # Archivos de configuración de Docker y redes
├── src/
│   ├── ingestion/      # Scripts de conexión a estaciones y productores Kafka
│   ├── models/         # Modelos de IA (.h5/.pth) y lógica de inferencia
│   └── api/            # Servidor FastAPI y gestión de WebSockets
├── scripts/            # Utilidades de simulación y mantenimiento
└── README.md           # Documentación del proyecto
```

## 📂 Documentación
El diseño técnico detallado de este proyecto se encuentra disponible en formato PDF:
*   [Descargar Informe Técnico (PDF)](docs/Informe_SATS_Chile.pdf)
