# Tidy - Gestor de Recibos y Pagos Mensuales

Aplicación web para registrar, organizar y controlar recibos mensuales de servicios como agua, luz, internet y arriendo.

## Integrantes
- Juan Murcia
- Juan Diego Soler
- Sergio Clavijo Lopez
- Alejandro Molina

## Tecnologías
- **Backend:** Java 17, Spring Boot 4, Spring Security, JWT
- **Frontend:** React
- **Base de datos:** MySQL
- **Control de versiones:** Git / GitHub

## Requisitos previos
- Java 17
- Maven
- MySQL 8+
- Node.js 18+
- IntelliJ IDEA

## Instalación y configuración

### 1. Clonar el repositorio
```bash
git clone https://github.com/JuanSoler1/tidy-backend2.git
cd tidy-backend2
```

### 2. Configurar la base de datos
Abrir MySQL y ejecutar:
```sql
CREATE DATABASE tidy_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

### 3. Configurar application.properties
Editar el archivo `src/main/resources/application.properties` y cambiar:
```properties
spring.datasource.password=TU_PASSWORD_AQUI
```

### 4. Correr el backend
Abrir el proyecto en IntelliJ IDEA y ejecutar `TidyBackendApplication.java`

El servidor arranca en `http://localhost:8080`

### 5. Correr el frontend
```bash
cd tidy-frontend
npm install
npm start
```

La aplicación abre en `http://localhost:3000`

## Endpoints principales

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| POST | /api/auth/registro | Registrar usuario |
| POST | /api/auth/login | Iniciar sesión |
| POST | /api/recibos | Crear recibo |
| GET | /api/recibos?mes=4&anio=2026 | Listar recibos por mes |
| PUT | /api/recibos/{id} | Editar recibo |
| DELETE | /api/recibos/{id} | Eliminar recibo |
| PATCH | /api/recibos/{id}/estado | Cambiar estado |

## Pruebas unitarias
El proyecto incluye 7 pruebas unitarias en `src/test/java/com/tidy/service/`:
- **AuthServiceTest** — 3 pruebas de registro y login
- **ReciboServiceTest** — 4 pruebas de CRUD de recibos

Para correrlas en IntelliJ: clic derecho sobre la carpeta `service` en test > Run Tests