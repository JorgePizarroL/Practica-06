# 📝 Práctica 6 - Fetch API (Gestor de Posts)

Aplicación web que consume la API de JSONPlaceholder para gestionar posts (CRUD), utilizando JavaScript moderno y manipulación del DOM sin usar innerHTML.

---

## 🚀 Funcionalidades

-  Cargar posts desde API (GET)
-  Crear nuevos posts (POST)
-  Editar posts (PUT)
-  Eliminar posts (DELETE)
-  Buscar posts por título o contenido
-  Spinner de carga
-  Manejo de errores
-  Mensajes de éxito

---

## Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript
- Fetch API
- JSONPlaceholder (API pública)

---

## 📸 Evidencias de funcionamiento

### 1. Datos cargados desde la API
![Lista](assets/01-lista.png)  
**Descripción:** Se obtienen 20 registros desde la API JSONPlaceholder mediante una petición GET. Los datos se renderizan dinámicamente en la interfaz mostrando título, contenido e ID de cada post.

---

### 2. Spinner - Estado de carga
![Spinner](assets/02-spinner.png)  
**Descripción:** Se muestra un indicador visual de carga ("Cargando posts...") mientras se realiza la petición a la API, mejorando la experiencia del usuario.

---

### 3. Crear post
![Crear](assets/03-crear.png)  
**Descripción:** Se envía el formulario y se realiza una petición POST. El nuevo post se agrega dinámicamente a la lista con un ID generado (ej. 101).

---

### 4. Editar post
![Editar](assets/04-editar.png)  
**Descripción:** Se selecciona un post y se cargan sus datos en el formulario. Al actualizar, se realiza una petición PUT y los cambios se reflejan en la lista.

---

### 5. Eliminar post
![Eliminar](assets/05-eliminar.png)  
**Descripción:** Se elimina un post mediante una petición DELETE. El elemento desaparece de la interfaz sin recargar la página.

---

### 6. Manejo de errores
![Error](assets/06-error.png)  
**Descripción:** Se muestra un mensaje de error cuando falla una petición HTTP, permitiendo identificar problemas en la comunicación con la API.

---

### 7. DevTools Network
![Network](assets/07-network.png)  
**Descripción:** En la pestaña Network se observan las peticiones HTTP realizadas:
- GET /posts (carga de datos)
- POST /posts (creación)
- PUT /posts/{id} (actualización)
- DELETE /posts/{id} (eliminación)

---

## 💻 Evidencias de código

### 8. API Service (Fetch API)
![API](assets/08-get-create-update-delete.png)  
**Descripción:** Implementación de funciones para consumir la API utilizando Fetch:
- getPosts (GET)
- createPost (POST)
- updatePost (PUT)
- deletePost (DELETE)

---

### 9. Componente PostCard
![PostCard](assets/09-PostCard.png)  
**Descripción:** Componente que construye dinámicamente cada post usando createElement, sin utilizar innerHTML.

---

### 10. Spinner y manejo de errores
![Spinner y Error](assets/10-spinner-mensajeError.png)  
**Descripción:** Componentes visuales para mostrar el estado de carga (Spinner) y errores en la aplicación.

---

### 11. Mensaje de éxito y renderizado
![Mensaje](assets/11-mensajeExito-renderizar.png)  
**Descripción:** Se muestra un mensaje visual de éxito al crear, editar o eliminar un post. Además, se renderiza dinámicamente la lista actualizada.

---

##  Estructura del proyecto

PRACTICA-06/
│── assets/
│── css/
│ └── styles.css
│── js/
│ ├── apiService.js
│ ├── app.js
│ └── components.js
│── index.html

---

## Buenas prácticas implementadas

- Uso de Fetch API con async/await
- Manejo de errores con try/catch
- Manipulación del DOM sin innerHTML
- Uso de createElement, textContent y appendChild
- Separación de lógica (API, UI, lógica principal)

---

## API utilizada

https://jsonplaceholder.typicode.com/

---