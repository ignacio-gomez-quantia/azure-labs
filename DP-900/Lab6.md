# Lab 6 · Power BI

## Entorno

| Parámetro | Valor |
|-----------|-------|
| Herramienta | Power BI Desktop |
| Datos | `customers.csv`, `products.csv`, `orders.csv` (origen Web) |
| Informe | [`Lab6.pbix`](./files/Lab6.pbix) |

## Pasos

### 1. Importación de datos y modelo

Las tres tablas se importan desde la web y Power BI detecta las relaciones `customers` → `orders` y `products` → `orders`.

![Modelo de datos](../assets/DP-900/lab6-01-data-model.png)

### 2. Formato de moneda para Revenue

![Revenue en formato Currency](../assets/DP-900/lab6-02-revenue-currency.png)

### 3. Jerarquía Categorized Product

Jerarquía en `products` con los niveles `Category` → `ProductName`.

![Jerarquía Categorized Product](../assets/DP-900/lab6-03-hierarchy.png)

### 4. Categoría de datos City

![Data category City](../assets/DP-900/lab6-04-city-category.png)

### 5. Tabla con Categorized Product y Revenue

![Tabla](../assets/DP-900/lab6-05-table.png)

### 6. Gráfico de columnas apiladas por categoría

![Stacked column chart](../assets/DP-900/lab6-06-column-chart.png)

### 7. Drill down a producto

Desglose de la categoría Mountain Bikes por producto usando la jerarquía.

![Drill down](../assets/DP-900/lab6-07-drill-down.png)

### 8. Gráfico circular de cantidades por categoría

![Pie chart](../assets/DP-900/lab6-08-pie-chart.png)

### 9. Mapa de ingresos por ciudad e interacción entre visuales

Al seleccionar una ciudad en el mapa, el resto de visuales del informe se filtran para resaltar sus datos.

![Informe con mapa](../assets/DP-900/lab6-09-map-report.png)
