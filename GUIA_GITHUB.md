# 📘 GUÍA PASO A PASO: Subir Arte Dental a GitHub

## 🎯 Objetivo
Tener tu sistema Arte Dental accesible desde cualquier lugar mediante una URL pública.

---

## ✅ MÉTODO 1: SUBIR ARCHIVOS DIRECTAMENTE (MÁS FÁCIL)

### Paso 1: Crear cuenta en GitHub (si no tienes)
1. Ve a https://github.com
2. Click en "Sign up" (Registrarse)
3. Completa el formulario con tu email
4. Verifica tu cuenta por email

### Paso 2: Crear un nuevo repositorio
1. Inicia sesión en GitHub
2. Click en el botón verde "New" o el ícono "+" arriba a la derecha → "New repository"
3. Completa los datos:
   - **Repository name**: `arte-dental-cloud`
   - **Description**: "Sistema de gestión odontológica en la nube"
   - **Public** o **Private**: Selecciona según prefieras
     - Public: Cualquiera puede ver el código (pero NO pueden acceder sin login)
     - Private: Solo tú puedes ver el repositorio
   - ✅ NO marques "Add a README file"
4. Click en "Create repository"

### Paso 3: Subir archivos
1. En la página del repositorio recién creado, verás opciones
2. Click en "uploading an existing file"
3. Arrastra estos 3 archivos a la ventana:
   - `index.html`
   - `README.md`
   - `.gitignore`
4. En el cuadro de texto abajo escribe: "Primera versión del sistema"
5. Click en "Commit changes" (el botón verde)

### Paso 4: Activar GitHub Pages
1. En tu repositorio, click en "Settings" (⚙️ Configuración)
2. En el menú de la izquierda, busca y click en "Pages"
3. En la sección "Source":
   - Branch: Selecciona "main"
   - Folder: Deja "/ (root)"
4. Click en "Save"
5. Espera 1-2 minutos
6. Refresca la página
7. Verás un mensaje verde: "Your site is published at https://TU-USUARIO.github.io/arte-dental-cloud/"

### Paso 5: Acceder a tu sistema
1. Copia la URL que apareció: `https://TU-USUARIO.github.io/arte-dental-cloud/`
2. Pégala en tu navegador
3. ¡Listo! Inicia sesión con:
   - Usuario: `Admin`
   - Contraseña: `10680`

---

## 💻 MÉTODO 2: USAR GIT (Para usuarios técnicos)

### Requisitos previos
- Tener Git instalado en tu computadora
- Tener una cuenta de GitHub

### Paso 1: Instalar Git (si no lo tienes)
**Windows:**
- Descarga de: https://git-scm.com/download/win
- Instala con las opciones por defecto

**Mac:**
```bash
# Usando Homebrew
brew install git

# O descarga de: https://git-scm.com/download/mac
```

**Linux:**
```bash
sudo apt-get install git  # Ubuntu/Debian
sudo yum install git      # CentOS/Fedora
```

### Paso 2: Configurar Git (primera vez)
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

### Paso 3: Crear repositorio en GitHub
1. Ve a https://github.com/new
2. Repository name: `arte-dental-cloud`
3. Click en "Create repository"
4. **NO cierres esta página**, necesitarás las instrucciones

### Paso 4: Subir archivos desde terminal
```bash
# 1. Abre la terminal/CMD en la carpeta donde están tus archivos

# 2. Inicializa Git
git init

# 3. Agrega todos los archivos
git add .

# 4. Crea el primer commit
git commit -m "Primera versión del sistema Arte Dental"

# 5. Conecta con GitHub (reemplaza TU-USUARIO)
git remote add origin https://github.com/TU-USUARIO/arte-dental-cloud.git

# 6. Cambia a la rama main
git branch -M main

# 7. Sube los archivos
git push -u origin main
```

### Paso 5: Activar GitHub Pages
(Igual que en el Método 1, Paso 4)

---

## 🔄 Actualizar tu aplicación después

### Si usaste el Método 1 (Subir archivos):
1. Ve a tu repositorio en GitHub
2. Click en el archivo que quieres actualizar (ej: `index.html`)
3. Click en el ícono del lápiz (✏️ Edit)
4. Haz tus cambios
5. Scroll abajo, escribe un mensaje descriptivo
6. Click en "Commit changes"
7. Espera 1-2 minutos y los cambios estarán en línea

### Si usaste el Método 2 (Git):
```bash
# 1. Modifica tus archivos

# 2. Agrega los cambios
git add .

# 3. Crea un commit con descripción
git commit -m "Descripción de los cambios"

# 4. Sube los cambios
git push
```

---

## 📱 Compartir con tu equipo

Una vez configurado, simplemente comparte la URL:
```
https://TU-USUARIO.github.io/arte-dental-cloud/
```

**Credenciales de acceso:**
- Usuario: `Admin`
- Contraseña: `10680`

**Importante:**
- Cada persona debe tener su propio usuario
- Créalos desde: Sistema → Usuarios
- Asigna roles según necesites (Admin, Odontólogo, Usuario)

---

## ❓ Preguntas Frecuentes

### ¿Es seguro tener mi aplicación en GitHub?
- ✅ Sí, porque requiere login para acceder
- ✅ Los datos están en Supabase, no en GitHub
- ✅ GitHub Pages usa HTTPS (conexión segura)
- ⚠️ Si prefieres más privacidad, usa repositorio "Private"

### ¿Cuánto cuesta?
- GitHub: **GRATIS** (con límites generosos)
- GitHub Pages: **GRATIS**
- Supabase: **GRATIS** (hasta 500MB de base de datos)

### ¿Puedo usar mi propio dominio?
Sí, GitHub Pages permite dominios personalizados:
1. Compra un dominio (ej: artedental.com)
2. En Settings → Pages → Custom domain
3. Ingresa tu dominio
4. Configura los DNS según las instrucciones

### ¿Qué pasa si borro algo por error?
GitHub guarda todo el historial. Puedes volver a versiones anteriores:
1. Ve a tu repositorio
2. Click en "Commits"
3. Encuentra la versión anterior
4. Click en "Browse files"
5. Descarga o restaura lo que necesites

### ¿Funciona sin internet?
No, necesitas conexión a internet porque:
- Los datos están en Supabase (nube)
- La aplicación se carga desde GitHub Pages
- Es una aplicación web, no una app instalada

---

## 🆘 Problemas Comunes

### "404 - Not Found"
**Solución:**
- Verifica que GitHub Pages esté activado
- Espera 2-3 minutos después de activarlo
- La URL debe terminar en `/` (ej: `/arte-dental-cloud/`)

### "No puedo subir archivos"
**Solución:**
- Verifica que hayas iniciado sesión en GitHub
- Asegúrate de estar en tu repositorio
- Intenta refrescar la página

### "Los cambios no se ven"
**Solución:**
- Espera 1-2 minutos (GitHub Pages tarda en actualizarse)
- Limpia la caché del navegador (Ctrl + Shift + R)
- Abre en modo incógnito para verificar

---

## 📞 Siguiente Paso

Una vez subido, comparte esta información con tu equipo:

**URL de acceso:**
```
https://TU-USUARIO.github.io/arte-dental-cloud/
```

**Credenciales iniciales:**
- Usuario: Admin
- Contraseña: 10680

**Recomendación:**
1. Ingresa y cambia la contraseña
2. Crea usuarios para cada miembro del equipo
3. Haz un backup de prueba para verificar que todo funciona

---

¡Éxito con tu sistema Arte Dental! 🦷✨
