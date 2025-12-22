# ERPNext Print Formats

Este repositorio contiene formatos de impresión (Print Formats) personalizados para **ERPNext** y **Frappe Framework**, diseñados para adaptarse a necesidades específicas (como localizaciones, visualización de productos, etc.) utilizando **Jinja** y **CSS**.

## Formatos Disponibles

### 1. Cotización - Chile (`quotation/`)

Un formato de impresión optimizado para el mercado chileno.

- **Archivos**:
  - `quotation-chile.html`: Plantilla Jinja/HTML.
  - `quotation-chile.css`: Estilos CSS dedicados.
- **Características**:
  - **Localización**: Muestra el **RUT** de la empresa y del cliente (campo `tax_id`).
  - **Moneda**: Formato especial para **CLP** (Pesos Chilenos) sin decimales.
  - **Visual**: Incluye imágenes de los productos en las líneas de detalle.
  - **PDF**: Optimizado para `wkhtmltopdf` (el motor de generación de PDF estándar de ERPNext v14/v15).
  - **Detalles**: Secciones claras para condiciones comerciales, vendedor, entrega, términos y notas.

## Cómo Utilizar

1. **Crear Print Format en ERPNext**:

   - Ir a `Print Format List` > `New Print Format`.
   - **DocType**: Seleccionar `Quotation` (para el formato de Chile) u otro según corresponda.
   - **Name**: Ej. "Cotización Chile".
   - **Module**: Seleccionar un módulo apropiado (ej. Selling).
   - **Standard**: `No`.
   - **Custom Format**: `Yes`.
   - **Print Format Type**: `Jinja`.

2. **Copiar Código**:

   - Copiar el contenido de archivo `.html` en la sección **HTML**.
   - Copiar el contenido de archivo `.css` en la sección **CSS**.

3. **Guardar y Probar**:
   - Guardar el documento.
   - Ir a una Cotización existente y probar el botón de imprimir seleccionando el nuevo formato.

## Requisitos/Compatibilidad

- **ERPNext**: Probado en versiones v14/v15.
- **Campos Personalizados**: Si su instancia usa campos propios para el RUT u otros datos, asegúrese de ajustar las variables Jinja al inicio del archivo HTML.

---

_Autor: Generado automáticamente._
