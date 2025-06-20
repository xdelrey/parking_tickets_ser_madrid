# Predicción de Ocupación del Estacionamiento Regulado (SER) en Madrid

## 1. Propósito del proyecto
Predecir con **60 minutos de antelación** el porcentaje de ocupación de las plazas SER
en cada barrio de Madrid durante 2024.  
La predicción permitirá:

* Lanzar alertas de saturación a conductores y Policía Municipal.  
* Ajustar tarifas dinámicas para reducir congestión y emisiones.  
* Evaluar escenarios “qué pasaría si” ante lluvia intensa o grandes eventos.

### Variable objetivo  

Tickets de aparcamiento / Plazas totales en el barrio


## 2. Fase I – Análisis exploratorio de datos (EDA)

| Paso | Resultado clave |
|------|-----------------|
| **Carga de datos** (Python + pandas) | • 4 M tickets (10 % muestreo aleatorio de 40 M)  \n• Precipitación diaria 2024 (AEMET)  \n• Calendario de grandes eventos IFEMA + agenda municipal |
| **Limpieza** | Normalización de fechas, conversión de ‘prec’ con coma decimal → punto, tratamiento de ‘Ip’ (lluvia inapreciable)... |
| **EDA** | Distribuciones, estacionalidad semanal, correlación lluvia ↔ ocupación, picos durante ferias IFEMA. |

---

## 3. Datasets

| Dataset | Fuente | Granularidad | Campos clave |
|---------|--------|--------------|--------------|
| **Tickets SER 2024** | Open Data Madrid | Parquímetro (id) | Inicio, fin, tipo zona |
| **Plazas SER** | Open Data Madrid | Calle → barrio | Plazas totales |
| **Precipitación diaria** | AEMET (3195, Retiro) | Día | `prec` (mm) |
| **Eventos IFEMA** | `/agenda/v1/events` | Evento | Nombre, fechas, recinto |
| **Agenda “grandes eventos”** | Portal datos Madrid | Evento | Categoría, barrio |

---

## 4. Estructura de carpetas (provisional)


---

## 5. Quick‑start reproducible

```
