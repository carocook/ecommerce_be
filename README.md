# Ecommerce Backend

Proyecto backend de ecommerce desarrollado con Node.js, Express y MongoDB Atlas.

## 📌 Funcionalidades

- CRUD de productos
- CRUD de carritos
- Sistema de autenticación con Passport
- Login con JWT
- Encriptación de contraseñas con bcrypt
- Validación de usuario autenticado
- Persistencia de datos en MongoDB Atlas
- Motor de plantillas Handlebars
- WebSockets con Socket.IO

---

## 🛠️ Tecnologías utilizadas

- Node.js
- Express
- MongoDB Atlas
- Mongoose
- Passport
- Passport Local
- Passport JWT
- JSON Web Token
- bcrypt
- Handlebars
- Socket.IO

---

## 📂 Estructura del proyecto

```bash
src/
│
├── config/
├── dao/
├── model/
├── public/
├── routers/
├── views/
├── utils/
└── app.js

```

---

## 📂 Instalación

1. Clonar repositorio

```
git clone https://github.com/carocook/ecommerce_be.git
```

2. Instalar dependencias

```
npm install
```

3. Crear archivo .env en la raíz del proyecto

```
PORT=3000

MONGO_URL=TU_URI_DE_MONGODB

JWT_PRIVATE_KEY=CoderSecret
```

4. Ejecutar servidor

```
npm run dev
```

- Servidor

```
http://localhost:3000
```

---

## 🔐 Autenticación

📌 Registro

- Endpoint

```
POST /api/sessions/register
```

- Body

```
{
  "first_name": "****",
  "last_name": "****",
  "email": "***@test.com",
  "age": 25,
  "password": "123456"
}
```

📌 Login

- Endpoint

```
POST /api/sessions/login
```

- Body

```
{
  "email": "***@test.com",
  "password": "123456"
}
```

- Respuesta

```
{
  "status": "success",
  "token": "JWT_TOKEN"
}
```

📌 Usuario Actual

- Endpoint

```
GET /api/sessions/current
```

- Requiere
  Cookie JWT válida.

- Respuesta

```
{
  "status": "success",
  "payload": {
    "id": "ID_USUARIO",
    "email": "***@test.com",
    "role": "user"
  }
}
```

---

## 🔒 Seguridad

- Contraseñas almacenadas con hash utilizando bcrypt.
- Autenticación mediante JWT.
- Cookies httpOnly.
- Estrategias Passport Local y Passport JWT.

---

## 👩‍💻 Autora

Carolina Cook - Desarrolladora Backend
