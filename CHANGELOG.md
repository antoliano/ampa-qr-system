# 🆕 CAMBIOS Y NUEVAS FUNCIONALIDADES

## Versión 1.1.0 - Febrero 2024

### ✨ Nuevas Funcionalidades

#### 1. Campo de Curso Escolar por Hijo

**Descripción**: Ahora puedes indicar el curso escolar de cada hijo al generar un código QR.

**Cómo usar**:
1. Al añadir cada hijo, verás dos campos:
   - **Nombre del hijo**: Nombre completo
   - **Curso**: Ejemplo de formatos válidos:
     - `3º Primaria`
     - `1º ESO`
     - `Infantil 5 años`
     - `2º Bachillerato`

**Ejemplo visual**:
```
Hijo 1:
  Nombre: Juan García López
  Curso: 3º Primaria

Hijo 2:
  Nombre: María García López
  Curso: 1º ESO
```

**Importante**: 
- El campo curso es obligatorio
- Esta información se guarda en el código QR
- Se mostrará en el listado de socios y en las reuniones

---

#### 2. Exportación y Visualización de Listado de Socios

**Descripción**: Nuevos botones para gestionar y exportar el listado completo de socios.

**Botones disponibles**:

##### 📥 Botón "CSV"
- **Función**: Descarga un archivo Excel/CSV con todos los socios
- **Contenido del archivo**:
  - Número de Socio
  - DNI
  - Nombre del Titular
  - Nombres de los Hijos (separados por punto y coma)
  - Cursos (separados por punto y coma)
  - Fecha de Alta
  - Fecha de Caducidad
- **Nombre del archivo**: `AMPA_Listado_Socios_2024-02-15.csv`
- **Uso**: Perfecto para importar a Excel, Google Sheets o cualquier programa de hojas de cálculo

##### 📄 Botón "Imprimir"
- **Función**: Abre una ventana con el listado formateado para imprimir
- **Características**:
  - Diseño profesional con encabezado
  - Tabla organizada con todos los datos
  - Fecha de generación del listado
  - Total de socios
  - Botón de imprimir integrado
- **Uso**: Ideal para tener una copia física del listado o generar un PDF

##### 👁️ Botón "Ver Lista" / "Ocultar"
- **Función**: Muestra u oculta la lista completa de socios en pantalla
- **Ventajas**:
  - No sobrecarga la interfaz cuando hay muchos socios
  - Acceso rápido a la información cuando lo necesitas
  - Scroll automático si hay muchos socios
- **Información mostrada**:
  - Número de socio
  - DNI
  - Nombre del titular
  - Lista de hijos con sus cursos

---

### 🔄 Compatibilidad con Códigos QR Antiguos

**Importante**: La aplicación es compatible con códigos QR generados antes de esta actualización.

- ✅ Los códigos antiguos (sin campo curso) funcionarán correctamente
- ✅ Los códigos nuevos (con campo curso) incluyen la información adicional
- ✅ No es necesario regenerar códigos QR existentes
- ⚠️ Si quieres añadir información de cursos a socios existentes, deberás regenerar su código QR

---

### 📊 Ejemplo de CSV Generado

```csv
Número Socio,DNI,Nombre Titular,Hijos,Cursos,Fecha Alta,Válido Hasta
1,"12345678A","María García López","Juan García; Ana García","3º Primaria; 1º ESO","2024-02-15","2026-06-30"
2,"87654321B","Pedro Martínez Ruiz","Carlos Martínez","Infantil 5 años","2024-02-15","2026-06-30"
```

**Cómo abrir el CSV**:
1. Haz doble clic en el archivo descargado
2. Se abrirá en Excel, Google Sheets o tu programa predeterminado
3. Los datos estarán organizados en columnas automáticamente

---

### 📋 Ejemplo de Listado Impreso

El listado impreso incluye:

```
╔══════════════════════════════════════════════════════════╗
║           LISTADO DE SOCIOS AMPA                         ║
║                                          Generado: 15/02/2024 ║
╚══════════════════════════════════════════════════════════╝

Total de socios: 25

┌────┬───────────┬──────────────────┬────────────────┬────────────────┬──────────────┐
│ Nº │    DNI    │     Titular      │     Hijos      │     Cursos     │ Válido hasta │
├────┼───────────┼──────────────────┼────────────────┼────────────────┼──────────────┤
│ #1 │ 12345678A │ María García L.  │ Juan García    │ 3º Primaria    │ 30/06/2026   │
│    │           │                  │ Ana García     │ 1º ESO         │              │
├────┼───────────┼──────────────────┼────────────────┼────────────────┼──────────────┤
│ #2 │ 87654321B │ Pedro Martínez R.│ Carlos M.      │ Infantil 5 años│ 30/06/2026   │
└────┴───────────┴──────────────────┴────────────────┴────────────────┴──────────────┘
```

---

### 🎯 Casos de Uso

#### Caso 1: Generar Listado para una Reunión
1. Ve a "Generar Códigos QR"
2. Desplázate hasta la sección "Socios"
3. Haz clic en "Imprimir"
4. Imprime o guarda como PDF
5. Lleva el listado a la reunión para verificación manual si es necesario

#### Caso 2: Enviar Listado a la Dirección del Colegio
1. Ve a "Generar Códigos QR"
2. Desplázate hasta la sección "Socios"
3. Haz clic en "CSV"
4. Envía el archivo descargado por email

#### Caso 3: Analizar Distribución por Cursos
1. Descarga el CSV
2. Abre en Excel/Google Sheets
3. Usa filtros o tablas dinámicas para agrupar por curso
4. Crea gráficos o estadísticas

---

### 🔧 Notas Técnicas

#### Formato del Campo Curso
- Texto libre (sin restricciones)
- Se recomienda usar formato consistente para facilitar análisis
- Ejemplos recomendados:
  - Para Infantil: `Infantil 3 años`, `Infantil 4 años`, `Infantil 5 años`
  - Para Primaria: `1º Primaria`, `2º Primaria`, ... `6º Primaria`
  - Para ESO: `1º ESO`, `2º ESO`, `3º ESO`, `4º ESO`
  - Para Bachillerato: `1º Bachillerato`, `2º Bachillerato`

#### Codificación del CSV
- UTF-8 con BOM (para compatibilidad con Excel)
- Separador: coma (,)
- Los campos de texto están entre comillas para proteger caracteres especiales

#### Almacenamiento de Datos
- Los datos del curso se guardan localmente en tu dispositivo
- Se incluyen en el código QR cifrado
- Persisten entre sesiones de la aplicación

---

### ⚙️ Actualización de la Aplicación

Para actualizar tu aplicación desplegada en GitHub Pages:

1. Descarga el nuevo archivo `index.html`
2. Ve a tu repositorio en GitHub
3. Haz clic en el archivo `index.html` existente
4. Haz clic en el icono de lápiz (editar)
5. Borra todo el contenido
6. Copia y pega el contenido del nuevo `index.html`
7. Haz clic en "Commit changes"
8. Espera 1-2 minutos
9. Recarga la aplicación en tu móvil (puede que necesites limpiar caché)

**Alternativa rápida**: Borra y vuelve a subir el archivo `index.html` completo

---

### 🐛 Posibles Problemas y Soluciones

#### Problema: No veo los botones de exportación
**Solución**: Necesitas tener al menos un socio registrado

#### Problema: El CSV no se abre correctamente en Excel
**Solución**: 
1. Abre Excel
2. Ve a Datos → Importar desde texto
3. Selecciona el archivo CSV
4. Marca "Delimitado" y "Coma" como separador

#### Problema: Los cursos no se muestran en códigos antiguos
**Solución**: Los códigos antiguos no tienen información de curso. Debes regenerarlos si quieres añadir esta información.

#### Problema: El listado impreso está cortado
**Solución**: En la ventana de impresión, selecciona orientación "Horizontal" o ajusta el zoom

---

### 📝 Changelog Técnico

**Cambios en la estructura de datos**:
```javascript
// Formato antiguo
hijos: ["Juan García", "Ana García"]

// Formato nuevo
hijos: [
  { nombre: "Juan García", curso: "3º Primaria" },
  { nombre: "Ana García", curso: "1º ESO" }
]
```

**Nuevas funciones añadidas**:
- `exportarListadoCSV()` - Genera y descarga archivo CSV
- `imprimirListado()` - Abre ventana de impresión con formato
- `actualizarHijo(index, campo, valor)` - Actualiza nombre o curso
- Estado `mostrarListado` - Controla visibilidad de la lista

**Compatibilidad hacia atrás**: ✅ Mantenida
- Los códigos QR antiguos siguen siendo válidos
- La aplicación detecta automáticamente el formato y lo procesa correctamente

---

## 📞 Soporte

Si tienes alguna pregunta sobre las nuevas funcionalidades o encuentras algún problema, no dudes en contactar con el administrador del sistema.

**¡Gracias por usar AMPA QR System!** 🎉
