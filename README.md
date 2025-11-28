# 🛠️ Sistema Web de Ferretería  
Aplicación web desarrollada en **Java (JDK 8+)**, **JSP**, **HTML/CSS**, y **PostgreSQL** para la gestión de productos, usuarios, pedidos, servicios y funcionalidades administrativas.  
Diseñada para ejecutarse en **Apache Tomcat**.

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

## 🧱 Tecnologías utilizadas

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

## 📂 Estructura del proyecto

ferreteria/
│── src/
│ ├── com.productos.datos/ # Conexión a la BD (PostgreSQL)
│ ├── com.productos.negocio/ # Lógica de negocio
│ └── com.productos.control/ # Servlets
│
│── WebContent/
│ ├── pages JSP
│ ├── css/
│ ├── js/
│ ├── imagenes/
│ └── WEB-INF/
│ ├── web.xml
│ └── lib/ (drivers JDBC)
