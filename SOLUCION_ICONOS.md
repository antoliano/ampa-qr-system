# 🔧 SOLUCIÓN: Iconos no se ven correctamente

## Problema
Los iconos del logo de la AMPA no aparecen en el móvil después de instalar la aplicación.

## Causa
El manifest.json tiene las rutas relativas de los iconos, pero GitHub Pages necesita rutas específicas según tu configuración.

---

## ✅ SOLUCIÓN RÁPIDA

### Opción 1: Cambiar rutas en manifest.json (RECOMENDADO)

Actualiza el `manifest.json` con las rutas absolutas según tu repositorio:

**Si tu repositorio se llama `ampa-qr-system`:**

```json
{
  "name": "AMPA Hermanos Alvarez Quintero",
  "short_name": "AMPA HAQ",
  "description": "Sistema de gestión de socios y control de asistencia para AMPA Hermanos Alvarez Quintero",
  "start_url": "/ampa-qr-system/",
  "display": "standalone",
  "background_color": "#7c3aed",
  "theme_color": "#7c3aed",
  "orientation": "portrait",
  "icons": [
    {
      "src": "/ampa-qr-system/icon-192.png",
      "sizes": "192x192",
      "type": "image/png",
      "purpose": "any maskable"
    },
    {
      "src": "/ampa-qr-system/icon-512.png",
      "sizes": "512x512",
      "type": "image/png",
      "purpose": "any maskable"
    }
  ]
}
```

**Si tu repositorio tiene otro nombre, cambia `ampa-qr-system` por el nombre de tu repo.**

**IMPORTANTE:** También actualiza la referencia al manifest en el `index.html`:
```html
<link rel="manifest" href="/ampa-qr-system/manifest.json">
```

---

### Opción 2: Usar rutas relativas (más simple)

Si los archivos están en la raíz del repositorio, usa rutas relativas simples:

```json
{
  "name": "AMPA Hermanos Alvarez Quintero",
  "short_name": "AMPA HAQ",
  "description": "Sistema de gestión de socios y control de asistencia para AMPA Hermanos Alvarez Quintero",
  "start_url": "./",
  "display": "standalone",
  "background_color": "#7c3aed",
  "theme_color": "#7c3aed",
  "orientation": "portrait",
  "icons": [
    {
      "src": "./icon-192.png",
      "sizes": "192x192",
      "type": "image/png",
      "purpose": "any maskable"
    },
    {
      "src": "./icon-512.png",
      "sizes": "512x512",
      "type": "image/png",
      "purpose": "any maskable"
    }
  ]
}
```

---

## 📋 Pasos para aplicar la solución:

1. **Elige una de las opciones de arriba** (recomiendo Opción 1)

2. **Reemplaza tu `manifest.json`** en GitHub con el código correspondiente

3. **Verifica que los 3 archivos están en GitHub:**
   - ✅ `icon-192.png` (logo de la AMPA)
   - ✅ `icon-512.png` (logo de la AMPA)
   - ✅ `manifest.json` (actualizado)

4. **Si usaste Opción 1, también actualiza `index.html`:**
   Busca la línea:
   ```html
   <link rel="manifest" href="manifest.json">
   ```
   Y cámbiala por:
   ```html
   <link rel="manifest" href="/ampa-qr-system/manifest.json">
   ```
   (o el nombre de tu repositorio)

5. **Espera 2-3 minutos** para que GitHub Pages actualice

6. **En tu móvil:**
   - Desinstala la app antigua
   - Borra caché del navegador
   - Vuelve a abrir la URL
   - Reinstala la app

7. **¡Ahora debería aparecer el logo correcto!** 🎉

---

## 🔍 Cómo verificar que funciona:

Antes de instalar en el móvil, abre en el navegador del móvil:

```
https://TU_USUARIO.github.io/NOMBRE_REPO/manifest.json
```

Deberías ver el contenido del manifest. Si da error 404, las rutas están mal.

---

## 💡 Tip adicional:

Si nada funciona, prueba esto:

1. **Sube todos los archivos a la RAÍZ del repositorio:**
   ```
   /
   ├── index.html
   ├── manifest.json
   ├── sw.js
   ├── icon-192.png
   ├── icon-512.png
   └── README.md
   ```

2. **Usa rutas simples en manifest.json:**
   ```json
   "start_url": "./",
   "src": "./icon-192.png",
   "src": "./icon-512.png"
   ```

3. **En index.html usa:**
   ```html
   <link rel="manifest" href="./manifest.json">
   ```

Esta es la configuración más sencilla y suele funcionar sin problemas.

---

## 🆘 Si sigue sin funcionar:

Mándame:
1. La URL completa de tu aplicación
2. El nombre exacto de tu repositorio en GitHub
3. Te generaré el manifest.json con las rutas correctas

---

**Archivo creado:** manifest.json actualizado está en tus outputs ✅
