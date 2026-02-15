# 🆕 ACTUALIZACIÓN v1.2.0 - Edición y Borrado de Socios

## Nuevos Cambios

### 1. Cambio de Nombre 🏫
La aplicación ahora se llama oficialmente:
**AMPA Hermanos Alvarez Quintero**

Este nombre aparecerá:
- En el título de la página
- En la pantalla de inicio cuando se instale en el móvil
- En todos los encabezados de la aplicación

---

### 2. Editar Socios ✏️

Ahora puedes **modificar la información de socios ya registrados** sin perder su número de socio.

#### Cómo editar un socio:

1. Ve a la sección **"Generar Códigos QR"**
2. Haz clic en el botón **"Ver Lista"** para mostrar todos los socios
3. Busca el socio que quieres editar
4. Haz clic en el **icono de lápiz azul** (✏️) junto al socio
5. Se cargará el formulario con los datos actuales del socio
6. Modifica lo que necesites:
   - ✅ Nombre del titular
   - ✅ Nombres de los hijos
   - ✅ Cursos de los hijos
   - ✅ Añadir o eliminar hijos
   - ❌ **NO se puede cambiar el DNI** (para mantener la integridad)
7. Haz clic en **"Actualizar Socio y Generar Nuevo QR"**
8. Se generará un **nuevo código QR** con la información actualizada
9. **IMPORTANTE**: Descarga el nuevo código QR - el anterior quedará obsoleto

#### Características de la edición:

✅ **Mantiene el número de socio** - El socio conserva su número original
✅ **Genera nuevo QR** - Automáticamente crea un código QR actualizado
✅ **Historial** - Registra la fecha de edición en el historial del socio
✅ **DNI protegido** - No se puede modificar el DNI para evitar duplicados
✅ **Validación completa** - Verifica que todos los campos estén completos
✅ **Cancelación segura** - Puedes cancelar en cualquier momento sin guardar cambios

#### Ejemplo de uso:

**Situación**: El hijo de un socio ha cambiado de curso
1. Editas el socio
2. Cambias "2º Primaria" a "3º Primaria"
3. Actualizas y descargas el nuevo QR
4. Entregas el nuevo QR al socio
5. El antiguo QR ya no funcionará

---

### 3. Eliminar Socios 🗑️

Ahora puedes **borrar socios** de forma permanente.

#### Cómo eliminar un socio:

1. Ve a la sección **"Generar Códigos QR"**
2. Haz clic en el botón **"Ver Lista"** 
3. Busca el socio que quieres eliminar
4. Haz clic en el **icono de papelera rojo** (🗑️)
5. Confirma la eliminación en el diálogo
6. El socio se eliminará permanentemente

#### ⚠️ Importante sobre la eliminación:

- ❌ **No se puede deshacer** - Una vez eliminado, no hay vuelta atrás
- ❌ **Elimina todo** - Se borra toda la información del socio
- ❌ **El QR dejará de funcionar** - El código QR del socio eliminado ya no será válido
- 💾 **Recomendación**: Exporta un CSV antes de eliminar socios importantes

#### Casos de uso para eliminar:

- **Baja del colegio**: El hijo se ha cambiado de colegio
- **Duplicados**: Se creó un socio por error
- **Información incorrecta**: Es más fácil borrar y crear de nuevo
- **Fin de ciclo**: Los hijos han terminado en el colegio

---

## 🎨 Mejoras en la Interfaz

### Indicadores visuales en modo edición:

Cuando editas un socio verás:
- **Título diferente**: "Editar Socio #XX" en lugar de "Generar Código QR"
- **Botón de cancelar**: X en rojo arriba a la derecha
- **Banner informativo**: Mensaje azul indicando que estás en modo edición
- **DNI deshabilitado**: Campo gris que no se puede editar
- **Botón actualizado**: "Actualizar Socio..." en lugar de "Generar Código QR"

### Botones en la lista de socios:

Cada socio tiene ahora **dos iconos**:
1. **✏️ Lápiz azul** - Editar socio
2. **🗑️ Papelera roja** - Eliminar socio

---

## 📊 Flujo de Trabajo Recomendado

### Para actualizar información:

```
1. Clic en "Ver Lista"
2. Clic en ✏️ (lápiz azul)
3. Modificar datos
4. Clic en "Actualizar Socio y Generar Nuevo QR"
5. Descargar nuevo QR
6. Entregar nuevo QR al socio
```

### Para dar de baja:

```
1. Exportar CSV (backup)
2. Clic en "Ver Lista"
3. Clic en 🗑️ (papelera roja)
4. Confirmar eliminación
5. Listo
```

### Para corregir un error:

**Opción A - Editar** (si el error es menor):
- Usa el lápiz para modificar
- Genera nuevo QR

**Opción B - Eliminar y recrear** (si el error es grave):
- Elimina el socio incorrecto
- Crea uno nuevo desde cero

---

## 🔐 Seguridad y Compatibilidad

### Sobre los códigos QR editados:

- Cada vez que editas un socio, se genera un **nuevo código QR con nueva firma HMAC**
- El código QR **antiguo dejará de funcionar** automáticamente
- Esto es una medida de seguridad para evitar que circulen códigos desactualizados
- El sistema detectará códigos antiguos y los rechazará

### Compatibilidad con reuniones:

- Las reuniones existentes **seguirán funcionando** normalmente
- Si un socio editado ya estaba en una reunión, **permanecerá** en la lista
- Sus datos en la reunión se actualizarán la próxima vez que escanees su nuevo QR
- Si eliminas un socio, seguirá apareciendo en reuniones antiguas (historial)

---

## ❓ Preguntas Frecuentes

### ¿Puedo editar el DNI de un socio?
❌ No. El DNI es el identificador único y no se puede cambiar. Si necesitas cambiar el DNI, debes eliminar el socio y crear uno nuevo.

### ¿Qué pasa con el número de socio al editar?
✅ Se mantiene. El socio conserva su número original.

### ¿El código QR antiguo sigue funcionando después de editar?
❌ No. Cuando editas, se genera un nuevo código QR y el antiguo deja de ser válido por seguridad.

### ¿Puedo recuperar un socio eliminado?
❌ No. La eliminación es permanente. Por eso recomendamos exportar un CSV antes de eliminar.

### ¿Cuándo debo usar "Editar" vs "Eliminar y recrear"?
- **Editar**: Para cambios simples (nombre, curso) y mantener el número de socio
- **Eliminar y recrear**: Para errores graves o si quieres un número de socio nuevo

### ¿Se pueden editar varios socios a la vez?
❌ No. Debes editar cada socio individualmente.

### ¿La edición afecta al historial del socio?
✅ Sí. Cada edición se registra en el historial con fecha y hora.

---

## 🔄 Cómo actualizar tu aplicación

Para obtener estas nuevas funcionalidades:

1. **Descarga** el nuevo archivo `index.html` y `manifest.json`
2. **Ve a tu repositorio** en GitHub
3. **Reemplaza** ambos archivos con las nuevas versiones
4. **Espera 1-2 minutos** para que GitHub Pages se actualice
5. **Abre la app en tu móvil** y recarga (puede necesitar forzar recarga: Ctrl+Shift+R o borrar caché)
6. **Verifica** que el nombre ha cambiado a "AMPA Hermanos Alvarez Quintero"
7. **Prueba** editar un socio de prueba para verificar que funciona

---

## 📝 Resumen de Cambios

| Funcionalidad | Estado | Descripción |
|---------------|--------|-------------|
| Cambio de nombre | ✅ Listo | Ahora se llama "AMPA Hermanos Alvarez Quintero" |
| Editar socios | ✅ Listo | Modifica información manteniendo número de socio |
| Eliminar socios | ✅ Listo | Borra socios permanentemente |
| DNI protegido | ✅ Listo | No se puede editar el DNI |
| Nuevo QR al editar | ✅ Listo | Genera automáticamente código actualizado |
| Confirmación al borrar | ✅ Listo | Pide confirmación antes de eliminar |
| Botón cancelar | ✅ Listo | Cancela edición sin guardar cambios |
| Indicadores visuales | ✅ Listo | Muestra claramente cuando estás editando |

---

## 🎉 ¡Disfruta de las nuevas funcionalidades!

Ahora tienes control total sobre tu base de datos de socios. Puedes mantenerla actualizada fácilmente sin perder información importante como los números de socio.

¿Tienes alguna sugerencia o encuentras algún problema? No dudes en reportarlo.

**AMPA Hermanos Alvarez Quintero - v1.2.0** 🏫
