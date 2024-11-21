# Proyecto de Monitoreo de Tiempos Muertos con InfluxDB y Grafana

Este proyecto utiliza contenedores Docker para implementar una solución de monitoreo de tiempos muertos basada en InfluxDB y Grafana. Los datos de los sensores se almacenan en una base de datos InfluxDB, y los gráficos se visualizan en Grafana.

## Requisitos Previos

- [Docker](https://www.docker.com/) instalado en el sistema.
- [Docker Compose](https://docs.docker.com/compose/) instalado.

## Configuración del Proyecto

El archivo `docker-compose.yml` configura los siguientes servicios:

### 1. **InfluxDB**
- Base de datos orientada a series temporales.
- Se usa para almacenar los datos recopilados de los sensores.

**Configuración:**
- Base de datos: `tiempos_muertos`
- Usuario administrador: `David`
- Contraseña: `David09-09`

El servicio expone el puerto `8086`.

### 2. **Grafana**
- Herramienta para la visualización de datos y generación de gráficos a partir de los datos de InfluxDB.

**Configuración:**
- Contraseña de administrador: `admin` (se recomienda cambiarla en producción).

El servicio expone el puerto `3000`.

### Volúmenes
Los datos de ambos servicios se persisten en volúmenes de Docker:
- `influxdb_data`: Almacena los datos de InfluxDB.
- `grafana_data`: Almacena las configuraciones de Grafana.
