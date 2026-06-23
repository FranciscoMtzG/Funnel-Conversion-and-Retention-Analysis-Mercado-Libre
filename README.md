# 📊 Análisis de Embudo y Retención para MercadoLibre

## 🎯 Objetivo
Analizar el comportamiento de los usuarios en el proceso de compra de **MercadoLibre** para identificar **puntos de fuga** en el embudo de conversión y evaluar la **retención de usuarios por cohortes**.  
El propósito es proponer **mejoras accionables** que optimicen la conversión y la retención a lo largo del tiempo.

---

## 📁 Dataset

### **mercadolibre_funnel**
Registra eventos de usuarios durante el proceso de compra.

- **Columnas principales:**
  - `user_id`: Identificador único del usuario.  
  - `session_id`: Identificador de sesión.  
  - `event_name`: Tipo de evento (`add_to_cart`, `purchase`, etc.).  
  - `event_times`: Marca temporal en formato Unix.  
  - `country`: País del evento.  
  - `device_category`: Tipo de dispositivo (`mobile`, `desktop`, `tablet`).  
  - `platform`: Plataforma (`android`, `iOS`, `web`).  
  - `product_cat`: Categoría del producto.  
  - `price`: Precio del producto.  
  - `currency`: Moneda.  
  - `referral_source`: Fuente de tráfico (`organic`, `paid_search`, `social`).  
  - `event_date`: Fecha legible del evento.  
  - `year`: Año del evento.

---

### **mercadolibre_retention**
Mide la actividad recurrente por usuario y periodo.

- **Columnas principales:**
  - `user_id`: Identificador único del usuario.  
  - `signup_date`: Fecha de registro.  
  - `signup_datetime`: Fecha y hora exactas del registro.  
  - `country`: País del usuario.  
  - `device_category`: Tipo de dispositivo.  
  - `platform`: Plataforma utilizada.  
  - `day_after_signup`: Días transcurridos desde el registro.  
  - `activity_date`: Fecha de actividad.  
  - `active`: Indicador binario (1 = activo, 0 = inactivo).  
  - `prob_active`: Probabilidad estimada de actividad.

---

## 🛠️ Herramientas Utilizadas
- **SQL** (CTEs, agregaciones, cohortes, cálculos de conversión)  
- **Google Sheets / Excel** (visualizaciones y resumen ejecutivo)  
- **MercadoLibre Funnel & Retention Dataset**

---

## 🔍 Metodología
1. Exploración del esquema y revisión de datos base.  
2. Construcción del embudo de conversión con CTEs.  
3. Cálculo de tasas de conversión y detección de caídas.  
4. Análisis de retención por cohortes (D7, D14, D21, D28).  
5. Segmentación por país, dispositivo y fuente de tráfico.  
6. Simulación de mejoras en etapas críticas.  
7. Redacción del informe ejecutivo (C → F → I).

---

## 📈 Métricas Clave
- **Tasa de conversión por etapa**  
- **Caída porcentual entre pasos del embudo**  
- **Retención por cohorte (D7, D14, D21, D28)**  
- **Segmentación por país, dispositivo y fuente de tráfico**

---

## 🧠 Hallazgos Clave
- Mayor pérdida de usuarios entre las etapas **add_to_cart → begin_checkout**.  
- Países con mejor conversión: **Argentina y México**.  
- Usuarios móviles presentan mayor retención en D7 y D14.  
- Cohortes recientes muestran una mejora progresiva en retención.  
- Las fuentes **orgánicas** tienen mejor conversión que las **pagadas**.

---

## 💡 Conclusiones
El análisis revela oportunidades para **optimizar el embudo de conversión** y **mejorar la retención** mediante:
- Simplificación del proceso de checkout.  
- Incentivos personalizados para usuarios que abandonan el carrito.  
- Estrategias de remarketing enfocadas en cohortes con baja retención.  
- Ajustes en campañas de adquisición según fuente y dispositivo.

---
