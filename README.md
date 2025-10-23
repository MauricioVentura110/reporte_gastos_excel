# reporte_gastos_excel

Generación automática de gastos (reestructuración de datos) a partir de la balanza contable.

---

## Descripción del notebook "reestructuracion_excel_vf"

Este notebook reestructura automáticamente una balanza contable de un mes particular y recupera los siguientes campos:

- **Cuenta:** número que caracteriza las áreas de la empresa que presentan un gasto.  
- **Nombre:** concepto del cargo.  
- **Cargos:** monto en pesos.

Con estos campos, se genera una tabla en Excel con la siguiente estructura:

- **Columnas:** áreas de la empresa.  
- **Filas:** nombres de los conceptos.  
- **Contenido:** monto de los cargos.

A partir de esta nueva tabla se calculan:

- Gasto total por área y porcentaje de cada concepto respecto al gasto del área.  
- Gasto total por concepto y porcentaje respecto al gasto total del mes.  
- Gasto total del mes.

Cada mes se agrega como **una nueva hoja de cálculo** en el Excel principal.

---

## Descripción del notebook "acumulacion_gastos_vf"

Este notebook toma el archivo de gastos de cada mes y genera un **nuevo archivo Excel** con la acumulación de los gastos hasta el último mes registrado.

La estructura es la misma que la de los gastos mensuales:  
- Columnas -> áreas de la empresa.  
- Filas -> conceptos.  

Se calculan los mismos montos y porcentajes para conocer la evolución de los gastos acumulados.

---

## Tecnologías utilizadas

* **Lenguaje:** Python 3.11.5  
* **Librerías:**
  - `pandas` (2.0.3)  
  - `numpy` (1.24.3)  
  - `openpyxl` (3.0.10)  
  - `os`

---

## Ejecución

**Aviso importante:**  
Los datos de la balanza contable contienen información sensible de la empresa para la cual se diseñó este código.  
Actualmente se está trabajando en **anonimizar los datos** para poder mostrar ejemplos y resultados de manera segura.

**Recomendación para ejecutar el notebook:**  
- Usar datos de ejemplo o sintéticos (no datos reales).  
- Abrir el notebook en Jupyter:
  ```bash
  jupyter notebook reestructuracion_excel_vf.ipynb
