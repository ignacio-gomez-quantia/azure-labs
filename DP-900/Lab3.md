# Lab 3 · Azure Cosmos DB

## Entorno

| Parámetro | Valor |
|-----------|-------|
| Suscripción | Azure for Students |
| Grupo de recursos | `Lab3` |
| Cuenta de Cosmos DB | `lab3accountcosmo` |

## Pasos

### 1. Despliegue de la cuenta de Cosmos DB

![Despliegue](../assets/DP-900/lab3-01-deployment-in-progress.png)

### 2. Creación del contenedor de ejemplo

Desde Data Explorer, base de datos `SampleDB` y contenedor `SampleContainer` con partition key `/categoryId`.

![Contenedor de ejemplo](../assets/DP-900/lab3-02-sample-container.png)

### 3. Exploración de los items

![Items de SampleContainer](../assets/DP-900/lab3-03-items.png)

### 4. Nuevo item y filtro

Creación del item `Road Helmet,45` y filtrado de los items cuyo nombre contiene "Helmet":

```sql
SELECT * FROM c WHERE CONTAINS(c.name, "Helmet")
```

![Nuevo item y filtro](../assets/DP-900/lab3-04-new-item-filter.png)
