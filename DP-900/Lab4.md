# Lab 4 · Microsoft Fabric

## Entorno

| Parámetro | Valor |
|-----------|-------|
| Plataforma | Microsoft Fabric (Tajamar) |
| Workspace | `Lab4-Workspace` |
| Lakehouse | `taxi_lakehouse` |
| Copy job | `Ingest_Sample_Data` |

## Pasos

### 1. Creación del workspace

![Workspace](../assets/DP-900/lab4-01-workspace.png)

### 2. Creación del lakehouse

![Lakehouse](../assets/DP-900/lab4-02-lakehouse.png)

### 3. Configuración del copy job

Origen: sample data NYC Taxi - Green (Parquet). Destino: tabla `dbo.taxi_rides` del lakehouse, con copia completa.

![Copy job](../assets/DP-900/lab4-03-copy-job-review.png)

### 4. Ejecución del copy job

37 861 891 filas copiadas en 46 min.

![Ejecución del copy job](../assets/DP-900/lab4-04-copy-job-run.png)

### 5. Vista previa de la tabla taxi_rides

![Tabla taxi_rides](../assets/DP-900/lab4-05-taxi-rides.png)

### 6. Consulta desde el SQL analytics endpoint

Distancia media de los trayectos por día de la semana:

```sql
SELECT DATENAME(dw, lpepPickupDatetime) AS Day,
       AVG(tripDistance) AS AvgDistance
FROM taxi_rides
GROUP BY DATENAME(dw, lpepPickupDatetime)
```

![Consulta SQL](../assets/DP-900/lab4-06-sql-query.png)

### 7. Eliminación del workspace

![Eliminación del workspace](../assets/DP-900/lab4-07-delete-workspace.png)
