# Lab 2 · Azure Storage

## Entorno

| Parámetro | Valor |
|-----------|-------|
| Suscripción | Azure for Students |
| Grupo de recursos | `Lab2` |
| Storage account | `lab2tajamarstorage` |
| Región | Spain Central |
| Rendimiento | Standard |
| Redundancia | LRS |

## Pasos

### 1. Despliegue del storage account

![Despliegue](../assets/DP-900/lab2-01-deployment-in-progress.png)

### 2. Subida de product1.json al contenedor data

![Subida de product1.json](../assets/DP-900/lab2-02-upload-product1.png)

### 3. Upgrade a Data Lake Storage Gen2

Antes de validar fue necesario desactivar el soft delete de contenedores (`containerDeleteRetentionPolicy`) en Data protection.

![Upgrade a Data Lake Gen2](../assets/DP-900/lab2-03-datalake-upgrade.png)

### 4. Subida de product2.json

![Subida de product2.json](../assets/DP-900/lab2-04-upload-product2.png)

### 5. Creación del file share

![File share files](../assets/DP-900/lab2-05-file-share.png)

### 6. Eliminación del grupo de recursos

![Eliminación del grupo de recursos](../assets/DP-900/lab2-06-delete-resource-group.png)
