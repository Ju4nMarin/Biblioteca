# 📚 BiblioISA Virtual - Sistema de Gestión de Biblioteca Digital

<div align="center">

![BiblioISA Virtual](https://img.shields.io/badge/BiblioISA-Virtual-orange?style=for-the-badge&logo=book&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

*Una solución simmple, moderna y elegante para la gestión de bibliotecas personales*

</div>

## 🎥 Vista Previa de la Aplicación
![image](https://github.com/user-attachments/assets/55e5e32d-f7a1-441d-ae91-8bf95c1398ad)


### 📱 Interfaz Principal
La página de inicio presenta un dashboard intuitivo con estadísticas en tiempo real y acceso rápido a las funcionalidades principales.

### 📖 Gestión de Libros
- **Vista de Biblioteca**: Tabla completa con todos los libros registrados
- **Búsqueda Inteligente**: Sistema de búsqueda en tiempo real por título, autor y editorial
- **Formularios Dinámicos**: Interfaz moderna para agregar y modificar libros
- **Navegación Fluida**: Diseño responsive con modales y transiciones suaves

### 🎨 Características Visuales
- **Diseño Moderno**: Interfaz limpia con gradientes y efectos visuales
- **Iconografía FontAwesome**: Iconos profesionales en toda la aplicación
- **Responsive Design**: Adaptable a dispositivos móviles y desktop
- **Feedback Visual**: Alertas y notificaciones para mejor UX

---

## 🚀 Características Principales

### ✨ Funcionalidades Core
- **📚 Gestión Completa de Libros**: Crear, leer, actualizar y eliminar registros
- **🔍 Búsqueda Avanzada**: Buscar por título, autor o editorial con resaltado de resultados
- **📊 Dashboard Estadístico**: Visualización de métricas de la biblioteca
- **🎯 Interfaz Intuitiva**: Diseño centrado en la experiencia del usuario
- **📱 Responsive Design**: Compatible con dispositivos móviles y tablets

### 🛠️ Características Técnicas
- **⚡ Rendimiento Optimizado**: Consultas eficientes a la base de datos
- **🔒 Validación de Datos**: Validación tanto en frontend como backend
- **🎨 UI/UX Moderna**: Diseño contemporáneo con animaciones suaves
- **♿ Accesibilidad**: Implementación de mejores prácticas de accesibilidad web
- **🔧 Código Mantenible**: Estructura clara y documentada

---

## 🛠️ Stack Tecnológico

### Backend
- **Flask 3.0.3**: Framework web ligero y flexible
- **PyMySQL 1.1.1**: Conector Python para MySQL
- **Jinja2**: Motor de plantillas para renderizado dinámico

### Frontend
- **HTML5**: Estructura semántica moderna
- **CSS3**: Estilos avanzados con Flexbox y Grid
- **JavaScript ES6+**: Interactividad y validaciones del lado cliente
- **FontAwesome 6.4.0**: Biblioteca de iconos profesionales

### Base de Datos
- **MySQL**: Sistema de gestión de base de datos relacional

---

## 📋 Requisitos del Sistema

### Prerrequisitos
- **Python 3.8+**
- **MySQL 5.7+** o **MariaDB 10.3+**
- **pip** (gestor de paquetes de Python)

### Dependencias Python
```
Flask==3.0.3
PyMySQL==1.1.1
mysqlclient==2.2.5
```

---

## ⚙️ Instalación y Configuración

### 1. Clonar el Repositorio
```bash
git clone https://github.com/tu-usuario/biblioteca-virtual.git
cd biblioteca-virtual
```

### 2. Crear Entorno Virtual
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

### 3. Instalar Dependencias
```bash
pip install -r requirements.txt
```

### 4. Configurar Base de Datos
```sql
-- Crear la base de datos
CREATE DATABASE biblioteca CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;

-- Usar la base de datos
USE biblioteca;

-- Crear la tabla de libros
CREATE TABLE libros (
    id INT AUTO_INCREMENT PRIMARY KEY,
    titulo VARCHAR(255) NOT NULL,
    autor VARCHAR(255) NOT NULL,
    editorial VARCHAR(255) NOT NULL,
    numero_paginas INT NOT NULL,
    edicion VARCHAR(50) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
```

### 5. Configurar Variables de Entorno
Edita el archivo `app.py` con tus credenciales de MySQL:
```python
app.config['MYSQL_HOST'] = 'localhost'
app.config['MYSQL_USER'] = 'tu_usuario'
app.config['MYSQL_PASSWORD'] = 'tu_contraseña'
app.config['MYSQL_DB'] = 'biblioteca'
app.config['MYSQL_PORT'] = 3306
```

### 6. Ejecutar la Aplicación
```bash
python app.py
```

La aplicación estará disponible en: `http://localhost:5000`

---

## 🏗️ Estructura del Proyecto

```
biblioteca-virtual/
├── 📁 static/
│   ├── estilos.css          # Estilos principales
│   └── estilos2.css         # Estilos específicos
├── 📁 templates/
│   ├── index.html           # Página principal
│   ├── alta.html            # Formulario agregar libro
│   ├── modificar.html       # Formulario editar libro
│   ├── almacenamiento.html  # Vista biblioteca completa
│   └── resultados.html      # Resultados de búsqueda
├── app.py                   # Aplicación Flask principal
├── requirements.txt         # Dependencias Python
└── README.md               # Documentación
```

---

## 🔗 Rutas de la Aplicación

| Ruta | Método | Descripción |
|------|--------|-------------|
| `/` | GET | Página principal con dashboard |
| `/alta` | GET | Formulario para agregar libro |
| `/add_libro` | POST | Procesar nuevo libro |
| `/almacenamiento` | GET | Vista completa de la biblioteca |
| `/modificar/<id>` | GET/POST | Editar libro específico |
| `/eliminar_libro/<id>` | GET | Eliminar libro |
| `/buscar` | POST | Buscar libros |

---

## 🎯 Uso de la Aplicación

### Agregar un Nuevo Libro
1. Navega a la sección "Agregar Libro"
2. Completa todos los campos requeridos
3. Haz clic en "Guardar Libro"

### Buscar Libros
1. Utiliza la barra de búsqueda en la navegación
2. Ingresa título, autor o editorial
3. Los resultados se mostrarán con términos resaltados

### Editar un Libro
1. Ve a "Mi Biblioteca"
2. Haz clic en "Editar" junto al libro deseado
3. Modifica los campos necesarios
4. Guarda los cambios

### Eliminar un Libro
1. En "Mi Biblioteca", haz clic en "Eliminar"
2. Confirma la acción en el diálogo

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Para contribuir:

1. **Fork** el proyecto
2. Crea una **rama** para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. **Commit** tus cambios (`git commit -m 'Agregar nueva funcionalidad'`)
4. **Push** a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un **Pull Request**

---

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

---

## 🙏 Agradecimientos

- Flask por el excelente framework web
- FontAwesome por los iconos profesionales
- La comunidad de código abierto por su apoyo continuo

---

<div align="center">

**⭐ Si este proyecto te resultó útil, ¡considera darle una estrella! ⭐**

</div>
