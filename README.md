# MejoresInversiones
Aplicación web para la evaluación financiera de alternativas de inversión mediante Periodo de Recuperación, VAN y TIR. Permite comparar múltiples proveedores por artículo, calcular flujos de efectivo dinámicos y determinar la mejor opción de inversión.
# Alternativas de Inversión – Evaluación Financiera Web

---

## TAGS
- finanzas
- ingenieria-economica
- van
- tir
- payback
- javascript
- indexeddb
- web-app

---

Aplicación web desarrollada en **HTML, CSS y JavaScript** para evaluar **alternativas de inversión** de una empresa mediante indicadores financieros clásicos:

- **Periodo de Recuperación (Payback)**
- **Valor Actual Neto (VAN)**
- **Tasa Interna de Retorno (TIR)**

La aplicación permite registrar artículos existentes, comparar múltiples proveedores, calcular flujos de efectivo dinámicos y determinar automáticamente la alternativa más conveniente.

---

## Objetivo del proyecto

Brindar una herramienta práctica para el **análisis financiero de inversiones**, enfocada en contextos académicos y empresariales, sin depender de servidores externos ni bases de datos remotas.

Toda la información se almacena localmente en el navegador mediante **IndexedDB**.

---

## Funcionalidades principales

### Gestión de artículos
- Registro de artículos existentes de la empresa
- Edición de datos financieros
- Retiro lógico (no se eliminan registros, solo se desactivan)

### Gestión de proveedores
- Alta y edición de proveedores por artículo
- Asociación de productos y costos
- Retiro lógico de proveedores
- Persistencia de flujos de efectivo por proveedor

### Flujos de efectivo dinámicos
- Generación automática de tablas según la vida útil
- Captura de ventas y costos por año
- Visualización de flujo detallado (utilidades, impuestos, depreciación)

### Cálculos financieros
- Depreciación por **línea recta**
- Cálculo de **diferencia de depreciación** entre activo actual y alternativa
- Cálculo automático de:
  - Periodo de recuperación (años, meses y días)
  - VAN (usando WACC)
  - TIR
- Determinación del proveedor ganador con la regla:
  1. Mayor VAN
  2. Mayor TIR (desempate)
  3. Menor Payback

### Resultados consolidados
- Visualización de resultados por proveedor
- Identificación clara del proveedor ganador
- Tabla comparativa final

---

## Tecnologías utilizadas

- **HTML5** – Estructura
- **CSS3** – Estilos y diseño visual
- **JavaScript (ES Modules)** – Lógica de negocio
- **IndexedDB** – Persistencia local de datos
- **Normalize.css** – Normalización de estilos

No se utilizan frameworks ni librerías externas.

---

## Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/tu-repositorio.git
2. Abre el proyecto:

- **Opción simple**: abrir index.html directamente en el navegador

- **Opción recomendada**: usar un servidor local (por ejemplo Live Server en VS Code)

3. Navega por la aplicación:

- **Inicio** → registra o selecciona un artículo

- **Proveedores** → agrega proveedores y flujos

- **Resultados** → analiza la mejor alternativa de inversión

---

## Persistencia de datos

Los datos se almacenan localmente en el navegador usando IndexedDB

No se envía información a servidores externos

Al limpiar caché/datos del navegador se pierde la información almacenada