# 🦷 Arte Dental - Sistema de Gestión Odontológica en la Nube

Sistema completo de gestión dental con base de datos en la nube (Supabase), diseñado para clínicas odontológicas modernas.

## ✨ Características

- 📅 **Agenda de Citas** - Gestión completa de citas y tratamientos
- 👥 **Gestión de Pacientes** - Registro detallado de información del paciente
- 🏥 **Fichas Médicas** - Historia clínica completa con alergias, medicamentos y antecedentes
- 📋 **Historia Clínica** - Registro de consultas, tratamientos y diagnósticos
- 📸 **Gestión de Imágenes** - Carga y visualización de radiografías y fotos
- 💾 **Backup/Restore** - Exportación e importación de datos
- 👤 **Multi-usuario** - Sistema de roles (Admin, Odontólogo, Usuario)
- 🌐 **100% en la Nube** - Datos sincronizados en tiempo real
- 📱 **Responsive** - Funciona en desktop, tablet y móvil
- 🔒 **Seguro** - Autenticación de usuarios

## 🚀 Acceso Rápido

**URL de la aplicación:** `https://TU-USUARIO.github.io/arte-dental-cloud/`

> ⚠️ Reemplaza `TU-USUARIO` con tu nombre de usuario de GitHub después de configurar GitHub Pages

## 👤 Credenciales por Defecto

- **Usuario:** `Admin`
- **Contraseña:** `10680`

> 🔐 **Importante:** Cambia la contraseña después del primer inicio de sesión

## 📦 Instalación y Despliegue

### Opción 1: GitHub Pages (Recomendado)

1. **Crea un nuevo repositorio en GitHub:**
   - Ve a https://github.com/new
   - Nombre del repositorio: `arte-dental-cloud`
   - Descripción: "Sistema de gestión odontológica"
   - Selecciona "Public" o "Private" según prefieras
   - Click en "Create repository"

2. **Sube los archivos:**
   ```bash
   # Si tienes Git instalado
   git clone https://github.com/TU-USUARIO/arte-dental-cloud.git
   cd arte-dental-cloud
   
   # Copia el archivo index.html al repositorio
   # Luego:
   git add .
   git commit -m "Versión inicial Arte Dental"
   git push origin main
   ```

3. **Activa GitHub Pages:**
   - Ve a tu repositorio en GitHub
   - Click en "Settings" (Configuración)
   - En el menú lateral, click en "Pages"
   - En "Source", selecciona "main" branch
   - Click en "Save"
   - ¡Listo! Tu app estará disponible en: `https://TU-USUARIO.github.io/arte-dental-cloud/`

### Opción 2: Subir archivos directamente (Más fácil)

1. **Crea el repositorio** como en el paso 1 anterior
2. **Sube archivos manualmente:**
   - En tu repositorio, click en "Add file" → "Upload files"
   - Arrastra el archivo `index.html`
   - Escribe un mensaje: "Versión inicial"
   - Click en "Commit changes"
3. **Activa GitHub Pages** como en el paso 3 anterior

## 🗄️ Base de Datos

La aplicación usa **Supabase** como base de datos en la nube. Ya está configurado y listo para usar.

### Tablas de la Base de Datos:
- `users` - Usuarios del sistema
- `patients` - Información de pacientes
- `appointments` - Citas y agenda
- `history` - Historial de consultas
- `images` - Imágenes y radiografías
- `medical_records` - Fichas médicas

### Estructura de Datos

**Users (Usuarios)**
```json
{
  "id": 1,
  "username": "Admin",
  "password": "10680",
  "name": "Administrador",
  "role": "admin"
}
```

**Patients (Pacientes)**
```json
{
  "id": 1,
  "nombre": "Juan Pérez",
  "telefono": "099123456",
  "email": "juan@email.com",
  "direccion": "Calle Principal 123",
  "fecha_nac": "1985-05-15",
  "notas": "Paciente regular",
  "deleted": false
}
```

**Medical Records (Ficha Médica)**
```json
{
  "id": 1,
  "paciente_id": 1,
  "alergias": ["Polen"],
  "alergias_medicamentos": ["Penicilina"],
  "medicacion_actual": ["Omeprazol"],
  "antecedentes_personales": {
    "diabetes": false,
    "hipertension": true,
    "cardiopatia": false
  }
}
```

## 📱 Uso del Sistema

### 1. Login
- Ingresa con usuario: `Admin` y contraseña: `10680`
- Cambia tu contraseña haciendo click en el ícono de llave 🔑

### 2. Agenda
- Crea nuevas citas seleccionando fecha, hora y paciente
- Busca citas por paciente o tratamiento
- Las citas del día actual se destacan en azul

### 3. Pacientes
- Registra nuevos pacientes con toda su información
- Busca por nombre o teléfono
- Accede rápido a Ficha Médica e Historia Clínica
- Los pacientes con condiciones médicas se marcan con ⚠️

### 4. Ficha Médica
- Registra alergias y medicamentos
- Antecedentes personales y odontológicos
- Hábitos del paciente
- Observaciones importantes

### 5. Historia Clínica
- Registra cada consulta con tratamiento, diagnóstico y precio
- Sube imágenes (radiografías, fotos)
- Imprime la historia completa
- Todo queda registrado con fecha y usuario

### 6. Sistema
- **Usuarios**: Crea usuarios con diferentes roles
- **Backup**: Exporta/Importa todos los datos en formato JSON
- **Info**: Estado de conexión a la base de datos

## 🔧 Roles de Usuario

| Rol | Permisos |
|-----|----------|
| **Admin** | Acceso total + gestión de usuarios |
| **Odontólogo** | Acceso completo a pacientes e historias |
| **Usuario** | Acceso básico (agenda y pacientes) |

## 💾 Backup y Restauración

### Exportar Datos
1. Ve a "Sistema" → "Backup"
2. Click en "Descargar"
3. Se descarga un archivo JSON con todos los datos

### Importar Datos
1. Ve a "Sistema" → "Backup"
2. Click en "Cargar"
3. Selecciona el archivo JSON previamente exportado

## 🔒 Seguridad

- ✅ Autenticación obligatoria
- ✅ Roles y permisos diferenciados
- ✅ Datos encriptados en tránsito (HTTPS)
- ✅ Base de datos segura en Supabase
- ✅ No se pueden eliminar usuarios admin principales

## 📊 Tecnologías Utilizadas

- **Frontend**: React 18 + Tailwind CSS
- **Base de Datos**: Supabase (PostgreSQL)
- **Hosting**: GitHub Pages
- **Icons**: Lucide React
- **Build**: Babel Standalone (sin necesidad de compilación)

## 🌐 Acceso desde Diferentes Dispositivos

Una vez desplegado en GitHub Pages, puedes acceder desde:
- 💻 Computadora de escritorio
- 📱 Teléfono móvil
- 📱 Tablet
- 🌍 Cualquier navegador moderno

Solo necesitas la URL: `https://TU-USUARIO.github.io/arte-dental-cloud/`

## 🐛 Solución de Problemas

### "No se conecta a la base de datos"
- Verifica tu conexión a internet
- El indicador en la esquina superior derecha debe estar verde (🟢)
- Si está rojo (🔴), espera unos segundos y recarga la página

### "No puedo iniciar sesión"
- Verifica que estés usando las credenciales correctas
- Usuario: `Admin` (con A mayúscula)
- Contraseña: `10680`

### "Las imágenes no se cargan"
- Verifica que el archivo no sea muy pesado (máx. 5MB recomendado)
- Usa formatos JPG, PNG o WEBP

## 📞 Soporte

Si tienes problemas o preguntas:
1. Revisa esta documentación
2. Verifica que GitHub Pages esté activo
3. Comprueba la conexión a internet

## 📄 Licencia

Este proyecto es de uso privado para Arte Dental.

---

**Desarrollado con ❤️ para Arte Dental**
**Versión 2.0 - 2025**
