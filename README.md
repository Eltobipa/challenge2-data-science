# challenge2-data-science
#  Análisis de Evasión de Clientes (Churn)

## 🔹 Introducción
Este proyecto tiene como objetivo analizar el fenómeno de **evasión de clientes (Churn)** en una empresa de telecomunicaciones.  
La pérdida de clientes afecta directamente los ingresos y la estabilidad del negocio, por lo que identificar patrones asociados a la evasión permite diseñar estrategias de retención más efectivas.

---

## 🔹 Limpieza y Tratamiento de Datos
- Se normalizó la variable **Churn** para asegurar consistencia en los valores ("yes"/"no").
- Se verificaron los tipos de datos en las variables numéricas (`MonthlyCharges`, `Cuentas_Diarias`), confirmando que no contienen valores nulos.
- Se inspeccionó la columna **Cuenta**, identificando las claves disponibles (`Contract`, `PaymentMethod`, `PaperlessBilling`, `Charges`) y descartando aquellas sin datos útiles.
- Se confirmó la cantidad de clientes en cada grupo: aproximadamente **5174 sin evasión** y **1869 con evasión**.

---

## 🔹 Análisis Exploratorio de Datos
Se exploraron las variables numéricas más relevantes:

- **Distribución de MonthlyCharges según Churn**:  
  Los clientes que cancelaron presentan valores más altos de gasto mensual, con mayor dispersión en la distribución.

- **Distribución de Cuentas_Diarias según Churn**:  
  Se observa un patrón similar: los clientes que cancelan tienen mayor gasto diario promedio y una variabilidad más amplia.

- **Histogramas comparativos**:  
  Los clientes que no cancelan se concentran en rangos bajos de gasto, mientras que la evasión se distribuye de manera más uniforme en rangos altos.

---

## 🔹 Conclusiones e Insights
- Existe una **relación directa entre mayor gasto y mayor probabilidad de evasión**.  
- Los clientes con cargos más altos muestran mayor dispersión en su comportamiento, lo que indica sensibilidad al precio y heterogeneidad en la percepción de valor.  
- La ausencia de variables como `Tenure` y `TotalCharges` limita el análisis temporal, pero las métricas disponibles permiten identificar segmentos de riesgo.  
- Los clientes con **MonthlyCharges altos** son los más propensos a cancelar, lo que sugiere que el precio es un factor crítico.

---

## 🔹 Recomendaciones
- **Estrategias de retención en segmentos de alto gasto**: ofrecer beneficios adicionales, descuentos iniciales o paquetes de valor para clientes con cargos elevados.  
- **Alertas tempranas**: implementar un sistema de monitoreo que identifique clientes en los deciles superiores de gasto mensual y diario.  
- **Campañas personalizadas**: diseñar mensajes de fidelización y programas de lealtad para reducir la percepción de costo elevado.  
- **Mejora de datos**: incorporar variables de tiempo de contrato (`Tenure`) y gasto acumulado (`TotalCharges`) para enriquecer futuros modelos predictivos.  
- **Monitoreo continuo**: mantener dashboards con métricas de churn por rango de gasto y realizar análisis de cohortes para evaluar la efectividad de las acciones.

---

## 🔹 Análisis Opcional: Correlaciones
Como paso adicional, se exploraron las **correlaciones** entre variables numéricas del dataset:

- **Relación entre Cuentas_Diarias y evasión**: correlación positiva moderada; clientes con mayor actividad diaria tienden a cancelar más.  
- **Cantidad de servicios contratados y churn**: más servicios no garantizan menor evasión; en algunos casos puede aumentar la probabilidad de cancelación.  

Este análisis adicional aporta insights valiosos para la creación de **modelos predictivos más robustos**.

---

## Conclusión
Este README resume el proceso completo: desde la limpieza de datos hasta la obtención de insights estratégicos, aportando una base sólida para la toma de decisiones orientadas a reducir la evasión de clientes.
