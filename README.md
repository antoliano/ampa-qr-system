# AMPA QR System - Sistema de Gestión de Socios

Sistema PWA (Progressive Web App) para gestionar socios de AMPA con códigos QR seguros y control de asistencia a reuniones.

## 🚀 Características

- ✅ **Generación de Códigos QR** con seguridad HMAC
- ✅ **Escaneo de QR** con cámara del dispositivo (usando jsQR)
- ✅ **Validación automática** de caducidad y autenticidad
- ✅ **Detección de duplicados** en reuniones
- ✅ **Almacenamiento persistente** local
- ✅ **Funciona offline** (PWA)
- ✅ **Instalable** en móviles iOS y Android

## 📱 Instalación en GitHub Pages

### Paso 1: Crear repositorio en GitHub

1. Ve a [GitHub](https://github.com) e inicia sesión con tu cuenta (antoliano@gmail.com)
2. Haz clic en el botón verde **"New"** (o "Nuevo repositorio")
3. Configura el repositorio:
   - **Repository name**: `ampa-qr-system` (o el nombre que prefieras)
   - **Description**: "Sistema de gestión de socios AMPA con códigos QR"
   - Marca como **Public** (público)
   - **NO** marques "Initialize with README"
4. Haz clic en **"Create repository"**

### Paso 2: Subir los archivos

Tienes dos opciones:

#### Opción A: Interfaz web de GitHub (más fácil)

1. En la página del repositorio recién creado, haz clic en **"uploading an existing file"**
2. Arrastra y suelta TODOS estos archivos:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
   - `README.md`
3. Escribe un mensaje de commit: "Subida inicial de AMPA QR System"
4. Haz clic en **"Commit changes"**

#### Opción B: Usar Git desde línea de comandos

```bash
# Clonar el repositorio
git clone https://github.com/TU_USUARIO/ampa-qr-system.git
cd ampa-qr-system

# Copiar los archivos al repositorio
# (copia index.html, manifest.json, sw.js, icon-192.png, icon-512.png, README.md)

# Añadir y subir archivos
git add .
git commit -m "Subida inicial de AMPA QR System"
git push origin main
```

### Paso 3: Activar GitHub Pages

1. En tu repositorio, ve a **Settings** (Configuración)
2. En el menú lateral izquierdo, haz clic en **Pages**
3. En **Source**, selecciona:
   - Branch: **main**
   - Folder: **/ (root)**
4. Haz clic en **Save**
5. Espera 1-2 minutos

### Paso 4: Acceder a tu aplicación

Tu aplicación estará disponible en:
```
https://TU_USUARIO.github.io/ampa-qr-system/
```

Por ejemplo, si tu usuario es `antoliano`:
```
https://antoliano.github.io/ampa-qr-system/
```

## 📲 Instalar en tu móvil

### En Android (Chrome/Samsung Internet):

1. Abre la URL en Chrome: `https://TU_USUARIO.github.io/ampa-qr-system/`
2. Toca el menú (⋮) en la esquina superior derecha
3. Selecciona **"Añadir a pantalla de inicio"** o **"Instalar app"**
4. Confirma la instalación
5. ¡Listo! Aparecerá un icono morado en tu pantalla de inicio

### En iOS (Safari):

1. Abre la URL en Safari: `https://TU_USUARIO.github.io/ampa-qr-system/`
2. Toca el botón de compartir (cuadrado con flecha hacia arriba)
3. Desplázate y selecciona **"Añadir a pantalla de inicio"**
4. Personaliza el nombre si quieres
5. Toca **"Añadir"**
6. ¡Listo! Aparecerá el icono en tu pantalla de inicio

## 🎯 Cómo usar la aplicación

### 1. Generar Códigos QR

1. Abre la aplicación
2. Toca **"Generar Códigos QR"**
3. Introduce:
   - DNI del padre/madre
   - Nombre completo
   - Nombres de los hijos
4. Toca **"Generar Código QR"**
5. Descarga el código QR generado
6. El socio puede guardar o imprimir su código QR

**Importante**: Si el DNI ya existe, el sistema reutilizará el mismo número de socio.

### 2. Crear una Reunión

1. Ve a **"Gestionar Reuniones"**
2. Toca el botón **"+ Nueva"**
3. Introduce:
   - Nombre de la reunión
   - Fecha
   - Hora
   - Lugar (opcional)
4. Toca **"Crear"**
5. Todos los socios se añadirán automáticamente a la lista

### 3. Escanear QR en una Reunión

1. Selecciona la reunión de la lista
2. Toca **"Activar Cámara"**
3. Apunta la cámara al código QR del socio
4. El sistema validará automáticamente:
   - ✅ **Verde**: Código válido, entrada registrada
   - ⛔ **Rojo**: Código caducado o falsificado
   - 🚨 **Amarillo**: Código ya escaneado (duplicado)
5. La lista se actualizará mostrando quién ha asistido

## 🔒 Seguridad

- Cada código QR incluye una **firma HMAC** única
- Los códigos **caducan automáticamente** el 30 de junio del año siguiente
- **Detección de duplicados** en tiempo real
- **Imposible falsificar** sin la clave secreta

## 💾 Almacenamiento de Datos

- Todos los datos se guardan **localmente** en tu dispositivo
- **No hay servidor** externo
- Los datos **persisten** entre sesiones
- Funciona **offline** después de la primera carga

## 🛠️ Soporte Técnico

### La cámara no funciona

1. Verifica que has dado permisos de cámara al navegador
2. En Android: Settings → Apps → Chrome → Permissions → Camera
3. En iOS: Settings → Safari → Camera → Allow

### Los datos no se guardan

1. Verifica que no estás en modo incógnito/privado
2. Asegúrate de tener espacio suficiente en el dispositivo
3. Comprueba que las cookies/almacenamiento local están activadas

### El escaneo QR no funciona

1. Asegúrate de que hay buena iluminación
2. Mantén el código QR centrado en el marco morado
3. Evita movimientos bruscos
4. Si el código está impreso, asegúrate de que no está arrugado o manchado

## 📝 Notas importantes

- **Fecha de caducidad**: Los códigos QR caducan el 30 de junio del año siguiente a su generación
- **Renovaciones**: Si renuevas un socio con el mismo DNI, mantendrá su número de socio
- **Backup**: Recomendamos hacer capturas de pantalla de los códigos QR importantes
- **Compatibilidad**: Funciona en todos los navegadores modernos (Chrome, Safari, Firefox, Edge)

## 🔄 Actualizar la aplicación

Para actualizar la aplicación con nuevas versiones:

1. Sube los nuevos archivos a tu repositorio GitHub
2. GitHub Pages se actualizará automáticamente en 1-2 minutos
3. Los usuarios verán la nueva versión al recargar la página

## 📧 Contacto

Para soporte o sugerencias, contacta con el administrador del AMPA.

---

**Versión**: 1.0.0  
**Desarrollado para**: AMPA  
**Tecnología**: PWA (HTML5, JavaScript, React)
