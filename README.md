
# ComPay - Aplicación Web Multicontenedor 🏦💻

Este proyecto contiene la aplicación **ComPay**, una aplicación web desarrollada en Java junto con una base de datos PostgreSQL. Ambos servicios están listos para ejecutarse en contenedores Docker, y se han configurado para facilitar su despliegue con Docker Compose.

## 📋 Contenidos

- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Ejecutar la aplicación](#ejecutar-la-aplicación)
- [Detener la aplicación](#detener-la-aplicación)
- [Detalles de configuración](#detalles-de-configuración)
- [Notas](#notas)

## ✅ Requisitos

- **Docker**: [Instalar Docker](https://docs.docker.com/get-docker/)

## 🚀 Instalación

**Clona este repositorio** en tu máquina local:

   ```bash
   git clone https://github.com/raulblancoo/tswApp.git
   cd tswApp
   ```

## ▶️ Ejecutar la aplicación

   ```bash
   docker-compose up
   ```
Este comando descargará las imágenes necesarias y levantará la aplicación junto con la base de datos PostgreSQL.

Accede a la aplicación en tu navegador web: http://localhost:8080

## ⏹️ Detener la aplicación
Para detener los contenedores y liberar los recursos, ejecuta:

   ```bash
   docker-compose down
   ```

## ⚙️ Detalles de configuración

* **compay_app:** La imagen de tu aplicación web, alojada en Docker Hub.
* **compay_db:** La imagen oficial de PostgreSQL (versión 17).
* **Redirección de puertos:**
   * 8080:8080 para la aplicación web.
   * 5432:5432 para la base de datos (solo para acceso local).

Para más detalles, revisa el archivo docker-compose.yml.

## 📌 Notas
* **Persistencia de datos:** La configuración de Docker Compose está diseñada para crear un volumen temporal para la base de datos, por lo que los datos no persisten entre ejecuciones.
* **Actualización de la aplicación:** Para obtener la última versión de la imagen en Docker Hub, ejecuta docker-compose pull antes de iniciar la aplicación con docker-compose up.
