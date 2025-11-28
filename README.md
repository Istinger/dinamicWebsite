# 🛠️ Sistema Web de Ferretería

Aplicación web para la gestión de productos, usuarios, servicios y compras. Implementada con Java (JSP/Servlets), JDBC y PostgreSQL; preparada para desplegar en Apache Tomcat.

---
## 📌 Características principales

### 👥 Gestión de Usuarios
- Registro e inicio de sesión.
- Perfiles: administrador, vendedor, cliente.
- Cada perfil posee diferentes permisos y vistas.

### 🛒 Carrito de Compras
- Agregar productos.
- Calcular subtotal y total.
- Generar órdenes de compra.
- Historial de compras por usuario.

### 📦 Gestión de Productos
- Crear, editar y eliminar productos.
- Control de stock.
- Categorías dinámicas.
- Ofertas y descuentos.

### 🧰 Servicios
- Mantenimiento.
- Instalación.
- Corte de materiales.
- Gestión de órdenes y detalle de servicios.

### 🔐 Seguridad
- Control por perfiles.
- Restricciones por página.
- Auditoría mediante triggers PostgreSQL.


---

### 🧱 Tecnologías utilizadas
### Backend
- **Java JDK 8+**
- **Servlets**
- **JSP**
- **JDBC** (conexión a PostgreSQL)

### Frontend
- **JSP**
- **HTML5**
- **CSS3**
- **Bootstrap** (si aplica)

### Base de Datos
- **PostgreSQL**
- Tablas como:
  - tb_usuario
  - tb_producto
  - tb_carrito
  - tb_orden
  - tb_servicio
  - tb_pagina
  - tb_perfil
  - tb_auditoria
- Uso de **secuencias**, **llaves foráneas** y triggers.

### Servidor de Aplicaciones
- **Apache Tomcat 9 / 10**
- Despliegue mediante archivo `.war`

---

## ✨ Funcionalidades principales
- Gestión de usuarios: registro, inicio de sesión y control de accesos por rol.  
- Carrito de compras: añadir productos, subtotal/total automático, historial de órdenes.  
- Gestión de productos: CRUD, categorías, control de stock, ofertas.  
- Servicios: catálogo de servicios (instalación, mantenimiento, corte).  
- Seguridad y auditoría: triggers en PostgreSQL para registro de operaciones.

---

## 🚀 Preparar y ejecutar (rápido)
1. Clonar repositorio:
    git clone <URL-del-repo>
2. Crear la base de datos en PostgreSQL y restaurar el backup (backup.sql).
3. Configurar conexión JDBC en src/.../Conexion.java (URL, usuario, contraseña).
4. Construir y desplegar:
    - Desde IDE (Eclipse/NetBeans): exportar WAR y desplegar en Tomcat, o ejecutar desde el servidor integrado.
    - Manual: exportar WAR → copiar a TOMCAT_HOME/webapps/ → iniciar Tomcat.
5. Acceder: http://IP:8080/ferreteria/

---

## 🗂 Estructura del proyecto
ferreteria/  
├─ src/  
│  ├─ com.productos.datos/  
│  ├─ com.productos.negocio/  
│  └─ com.productos.control/  
├─ WebContent/  
│  ├─ JSP/  
│  ├─ css/  
│  ├─ js/  
│  ├─ imagenes/  
│  └─ WEB-INF/  

---

## 🗄 Base de datos
Tablas principales: usuario, productos, carrito, ordenes, servicios, auditoria.  
Se recomiendan índices sobre campos de búsqueda y claves foráneas para integridad.

---

## ⚙️ Notas de configuración
- Java: JDK 8+  
- Ajustar pool de conexiones si es necesario.  
- Verificar rutas de JSP y mappings en web.xml si hay cambios en el despliegue.

---

## 👤 Autor
Proyecto desarrollado por Jossue Proaño. 


