# App de Helados Caseros — Guía de publicación

Archivos:
- index.html ........... la app
- firebase-config.js ... AQUÍ pegás los datos de tu proyecto Firebase (paso 3)
- firestore.rules ...... reglas de seguridad para pegar en Firebase (paso 5)
- manifest.json, sw.js, icon-*.png, icon.svg ... para instalarla como app y que abra sin internet

## 1. Crear el proyecto en Firebase
console.firebase.google.com → "Crear un proyecto" → nombre: helados → desactivá Google Analytics → Crear.

## 2. Activar la base de datos
Menú izquierdo: Compilación → Firestore Database → Crear base de datos → ubicación: nam5 (United States) → "Comenzar en modo de producción" → Crear.

## 3. Registrar la app web y copiar la configuración
⚙️ (junto a "Descripción general") → Configuración del proyecto → abajo en "Tus apps" el ícono </> → apodo: helados → Registrar app.
Copiá lo que está entre las llaves de `const firebaseConfig = { ... }` y pegalo en firebase-config.js (abrilo con el Bloc de notas) reemplazando los "PEGAR_AQUI". Guardá.

## 4. Activar usuario y contraseña y crear tu usuario
Compilación → Authentication → Comenzar → pestaña "Método de acceso" → "Correo electrónico/contraseña" → activá el primer interruptor → Guardar.
Luego pestaña "Usuarios" → "Agregar usuario":
  - Correo: tu usuario + @helados.app  (ej: freyman@helados.app)
  - Contraseña: la que querás (mínimo 6 caracteres)
En la app solo escribís el usuario (freyman) y la contraseña.

## 5. Pegar las reglas de seguridad
Firestore Database → pestaña "Reglas" → borrá todo → pegá el contenido de firestore.rules → si tu usuario no es "freyman", cambiá 'freyman@helados.app' → Publicar.
Para que alguien más use la app: crealo en el paso 4 y agregalo aquí: 'freyman@helados.app', 'ana@helados.app'

## 6. Subir a GitHub
github.com → "New repository" → nombre: helados → Public → Create repository → "uploading an existing file" → arrastrá TODOS los archivos (no la carpeta) → Commit changes.

## 7. Activar GitHub Pages
En el repositorio: Settings → Pages → Source: "Deploy from a branch" → Branch: main, carpeta / (root) → Save. En 1-2 minutos queda en: https://TU_USUARIO.github.io/helados/

Listo: abrí el enlace, entrá con tu usuario y contraseña y agregala a la pantalla de inicio del celular.
