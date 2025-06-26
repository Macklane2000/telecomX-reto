# Análisis de Rotación de Clientes de Telecomunicaciones

## Descripción del Proyecto

Este proyecto realiza un análisis exploratorio de datos (EDA) sobre la rotación de clientes (Churn) de una empresa de telecomunicaciones. El objetivo es identificar los factores clave que influyen en la decisión de un cliente de abandonar la compañía y proporcionar información valiosa para desarrollar estrategias de retención de clientes efectivas.

## Origen de los Datos

Los datos utilizados provienen del archivo `TelecomX_Data.json`, el cual contiene información detallada sobre los clientes, incluyendo datos demográficos, servicios contratados y comportamiento de uso, así como el estado de rotación (Churn).

## Metodología

El análisis se llevó a cabo siguiendo los siguientes pasos:

1.  **Extracción y Carga:** Se cargaron los datos desde el archivo JSON a un DataFrame de pandas.
2.  **Transformación y Limpieza de Datos:**
    *   Se normalizaron las columnas anidadas (`customer`, `phone`, `internet`, `account`) para obtener una estructura de datos plana.
    *   Se verificaron y manejaron los valores faltantes en la columna `Charges.Total`, eliminando las filas correspondientes.
    *   Se convirtió el tipo de dato de la columna `Charges.Total` a numérico.
3.  **Análisis Exploratorio de Datos (EDA):**
    *   Se calcularon estadísticas descriptivas para las variables numéricas (`tenure`, `Charges.Monthly`, `Charges.Total`, `SeniorCitizen`).
    *   Se analizó la distribución de la rotación a través de variables categóricas (género, tipo de contrato, método de pago, servicios adicionales, etc.) utilizando gráficos de barras.
    *   Se examinó la distribución de las variables numéricas para clientes que rotaron y los que no, empleando diagramas de caja.
4.  **Informe Final:** Se elaboró un informe detallado resumiendo los hallazgos del análisis y ofreciendo recomendaciones.

## Hallazgos Clave

Los principales factores identificados que influyen en la rotación de clientes incluyen:

*   **Tipo de Contrato:** Los contratos mes a mes están fuertemente asociados con una mayor rotación.
*   **Antigüedad del Cliente:** Los clientes con menor antigüedad son más propensos a rotar.
*   **Servicio de Fibra Óptica:** Los clientes con este servicio presentan una tasa de rotación más alta.
*   **Método de Pago:** El uso de cheque electrónico se relaciona con una mayor propensión a rotar.
*   **Servicios Adicionales:** La ausencia de servicios como seguridad online, backup, protección de dispositivos, soporte técnico y streaming aumenta la probabilidad de rotación.
*   **Información Demográfica:** Clientes sin pareja o dependientes tienden a rotar más.
*   **Cargos Mensuales:** Cargos mensuales más altos, especialmente en los primeros meses, pueden estar asociados con la rotación.

## Recomendaciones

Basado en el análisis, se proponen las siguientes recomendaciones para reducir la rotación:

*   Incentivar la transición a contratos a largo plazo.
*   Implementar programas de retención temprana para nuevos clientes.
*   Mejorar la calidad del servicio y soporte para usuarios de fibra óptica.
*   Evaluar y optimizar la experiencia de pago con cheque electrónico.
*   Promocionar activamente la adopción de servicios adicionales.
*   Desarrollar estrategias de retención personalizadas para clientes sin pareja o dependientes.
*   Monitorear proactivamente a clientes con altos cargos iniciales.

## Cómo Ejecutar el Código

Este análisis se realizó en un entorno de Google Colab. Para ejecutar el código:

1.  Asegúrate de tener el archivo `TelecomX_Data.json` disponible.
2.  Abre el notebook de Colab.
3.  Ejecuta las celdas de código secuencialmente.

## Dependencias

Las principales librerías utilizadas son:

*   pandas
*   matplotlib
*   seaborn
