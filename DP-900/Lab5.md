# Lab 5 · Real-time analytics en Microsoft Fabric

## Entorno

| Parámetro | Valor |
|-----------|-------|
| Plataforma | Microsoft Fabric (Tajamar) |
| Workspace | `Lab5-Workspace` |
| Eventstream | `taxi_data` |
| Origen | `sample-yellowtaxi` (Yellow taxi) |
| Eventhouse | `Taxi Eventhouse` |
| Tabla KQL | `yellow-taxi` |

## Pasos

### 1. Conexión del origen Yellow taxi al eventstream

Desde el Real-Time hub, origen de ejemplo Yellow taxi hacia el eventstream `taxi_data` del workspace `Lab5-Workspace`.

![Conexión del origen](../assets/DP-900/lab5-01-eventstream-connect.png)

### 2. Eventstream en vivo

![Eventstream en vivo](../assets/DP-900/lab5-02-eventstream-live.png)

### 3. Eventhouse como destino del stream

![Destino Eventhouse](../assets/DP-900/lab5-03-eventhouse-destination.png)

### 4. Base de datos KQL con la tabla yellow-taxi

![Base de datos KQL](../assets/DP-900/lab5-04-kql-database.png)

### 5. Consulta KQL: primeras 100 filas

```kql
['yellow-taxi']
| take 100
```

![KQL take 100](../assets/DP-900/lab5-05-kql-take.png)

### 6. Consulta KQL: recogidas por hora

```kql
['yellow-taxi']
| summarize PickupCount = count() by bin(todatetime(tpep_pickup_datetime), 1h)
```

![KQL summarize por hora](../assets/DP-900/lab5-06-kql-summarize.png)

### 7. Gráfico de columnas de recogidas por hora

![Column chart](../assets/DP-900/lab5-07-column-chart.png)

### 8. Eliminación del workspace

![Eliminación del workspace](../assets/DP-900/lab5-08-delete-workspace.png)
