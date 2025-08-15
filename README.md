Mi Primera API FastAPI - Bootcamp

👤 Desarrollador: Camilo Andrés León Roldán
📧 Correo: camilo-leon@users.noreply.github.com
🔒 Privacidad: Email configurado según buenas prácticas de GitHub
📅 Fecha de creación: 2025-08-14 22:15:00
📂 Ubicación del proyecto: /c/Users/Aprendiz/desarrollo-personal/camilo-leon-bootcamp/mi-primera-api-fastapi
💻 Equipo de trabajo: SENA – ADSO Ficha 3147246

🔧 Configuración Local

Este proyecto está preparado para un entorno de desarrollo controlado y colaborativo:

Entorno virtual dedicado: venv-camilo/

Configuración Git aplicada solo a este repositorio

Dependencias aisladas para no interferir con otros proyectos

🚀 Instalación y Ejecución
# 1. Activar entorno virtual
source venv-camilo/bin/activate   # Linux/Mac
venv-camilo\Scripts\activate      # Windows

# 2. Instalar dependencias
pip install -r requirements.txt

# 3. Ejecutar servidor en modo desarrollo
uvicorn main:app --reload --port 8000

📝 Notas del Desarrollador

Git: Configurado únicamente para este proyecto.

Correo: Uso de email privado de GitHub para proteger información personal.

Entorno virtual: Todas las librerías instaladas en venv-camilo/.

Puerto: Por defecto 8000, modificable si existe conflicto.

Estado actual: Semana 2 – API básica con validación y type hints.

🛠️ Resolución de Problemas

No se activa el entorno virtual:

rm -rf venv-camilo && python -m venv venv-camilo


Puerto en uso: Cambiar el valor de --port en el comando de Uvicorn.

Git no responde: Revisar configuración local con:

git config user.name
git config user.email


Cambiar correo en Git: Configurar desde GitHub → Settings → Emails.

📌 ¿Qué hace esta API?

Es una API inicial creada con FastAPI, que incluye validación automática de datos y anotaciones de tipo (type hints) para mayor claridad y robustez.

✨ Funcionalidades implementadas (Semana 2)

✅ Anotaciones de tipo en todos los endpoints
✅ Validación automática con Pydantic
✅ Endpoint POST para agregar datos
✅ Parámetros dinámicos en ruta (/products/{id})
✅ Filtros y búsqueda con parámetros de consulta (query parameters)

▶️ Cómo ejecutar rápidamente
pip install fastapi pydantic uvicorn
uvicorn main:app --reload

 📌 My API with FastAPI & Pydantic

Este proyecto es una API construida con **FastAPI** y **Pydantic**, que demuestra cómo crear y consumir diferentes endpoints, manejar validaciones de datos y estructurar respuestas de forma tipada.

---

## 🚀 Endpoints Disponibles

### **1. Información general**
| Método | Endpoint | Descripción |
|--------|----------|-------------|
| GET | `/` | Mensaje de bienvenida. |
| GET | `/info` | Información sobre la API y su estado. |
| GET | `/greeting/{name}` | Saluda a un usuario por nombre. |
| GET | `/my-profile` | Devuelve un perfil de ejemplo. |

---

### **2. Operaciones básicas**
| Método | Endpoint | Descripción |
|--------|----------|-------------|
| GET | `/calculate/{num1}/{num2}` | Suma dos números. |
| GET | `/fruits` | Lista de frutas. |
| GET | `/numbers` | Lista de números enteros. |
| GET | `/user/{user_id}` | Información de usuario ficticia. |

---

### **3. Gestión de productos**
| Método | Endpoint | Descripción |
|--------|----------|-------------|
| POST | `/products` | Crea un producto (usa Pydantic para validación). |
| GET | `/products` | Lista todos los productos creados. |
| GET | `/products/{product_id}` | Obtiene un producto por su ID. |
| GET | `/categories/{category}/products/{product_id}` | Busca un producto dentro de una categoría. |
| GET | `/search` | Filtra productos por nombre, precio máximo o disponibilidad. |

---

### **4. Gestión de usuarios**
| Método | Endpoint | Descripción |
|--------|----------|-------------|
| POST | `/users` | Crea un usuario con datos completos y validación. |

---

## 🛠 Ejemplo de uso del endpoint POST `/products`

**Request:**
```bash
curl -X POST "http://127.0.0.1:8000/products" \
-H "Content-Type: application/json" \
-d '{
    "name": "Laptop",
    "price": 1500,
    "available": true
}'

## Reflexión
Durante este ejercicio aprendí a implementar modelos con Pydantic para validar datos automáticamente en FastAPI.  
También comprendí cómo usar los *type hints* para mejorar la legibilidad y el mantenimiento del código.  
Esta experiencia me permitió crear una API más robusta, profesional y preparada para funcionalidades más complejas.
