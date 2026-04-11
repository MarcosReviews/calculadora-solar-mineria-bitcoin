# ₿ Calculadora Solar para Minería Bitcoin 24/7

**Herramienta gratuita e interactiva para calcular si merece la pena instalar energía solar para minar Bitcoin.**

👉 [Ver la calculadora en vivo] https://dynamic-starship-cd670a.netlify.app/

---

## ¿Qué hace?

Responde en tiempo real a las preguntas que todo minero se hace antes de instalar solar:

- ¿Cuántos **paneles solares** necesito para alimentar mi ASIC 24/7?
- ¿Cuántas **baterías** hacen falta para cubrir la noche?
- ¿Cuánto **cuesta** toda la instalación?
- ¿En cuánto tiempo se **amortiza**?
- ¿Me sale a cuenta añadir **batería** o es mejor tirar de la red por las noches?
- Si ya tengo solar, ¿**qué me falta** para añadir el minero?

## ✨ Características

- **Sin instalación** — un solo archivo `.html`, se abre directamente en el navegador
- **Sin servidor** — todos los cálculos corren en local, sin enviar datos a ningún sitio
- **Precio BTC en tiempo real** — se actualiza automáticamente desde la API pública
- **Tarifa eléctrica por períodos** — punta / llano / valle (2.0TD España y Tarifa VE Iberdrola)
- **Análisis de batería completo** — payback, vida útil, breakeven año a año, tabla de sensibilidad al precio
- **Modo instalación existente** — calcula la ampliación necesaria si ya tienes paneles
- **Proyección mensual con halving** — aplica el ×0,5 del halving automáticamente en el mes correcto
- **Dificultad de red ajustable** — para escenarios optimistas o pesimistas
- **Tema claro/oscuro** — modo dark por defecto, toggle en el header
- **Responsive** — funciona en móvil

## 🧮 ¿Cómo funciona el cálculo?

```
Consumo diario = ASIC (W) × 24h / 1000          → kWh/día
Producción/panel = W × HSP × eficiencia / 1000   → kWh/día/panel
Paneles necesarios = consumo_diario / prod_panel

Consumo nocturno = consumo_diario - consumo_durante_sol
Baterías necesarias = consumo_nocturno / (capacidad × % utilizable)

Precio medio ponderado (24/7):
  = 23,8% × precio_punta + 23,8% × precio_llano + 52,4% × precio_valle

Payback batería = inversión_batería / (consumo_nocturno × precio_medio × 365)
Vida útil batería = ciclos / 365 días
```

## 📂 Estructura

```
calculadora-solar-mineria-v9.html   ← Versión actual (la que usar)
guion-video-calculadora-solar.html  ← Guión del vídeo de presentación
README.md
```

## 🚀 Uso

1. Descarga `calculadora-solar-mineria-v9.html`
2. Ábrelo en cualquier navegador moderno (Chrome, Firefox, Edge)
3. Introduce tus datos y obtén el análisis completo

No necesita conexión a internet excepto para la actualización automática del precio de Bitcoin y los gráficos (Chart.js vía CDN).

## 🤝 Contribuir

¿Tienes ideas para mejoras? ¡Son bienvenidas!

- Abre un **Issue** describiendo la mejora o el error encontrado
- Haz un **Fork** + **Pull Request** con tu propuesta
- Comenta en el canal de YouTube: https://www.youtube.com/@MarcosReviews

Ideas en las que se puede trabajar:
- [ ] Soporte para más países (tarifas de México, Colombia, Argentina…)
- [ ] Cálculo con múltiples tipos de ASIC distintos en la misma instalación
- [ ] Exportar resultados a PDF directamente desde la calculadora
- [ ] Modo comparativa entre dos configuraciones de batería
- [ ] Gráfica de breakeven solar visual (punto de cruce)

## 📋 Datos de entrada necesarios

| Dato | Dónde encontrarlo |
|------|------------------|
| Consumo del ASIC (W) | [MiningNow.com](https://miningnow.com/) |
| Horas Solares Pico | [FootprintHero.com](https://footprinthero.com/peak-sun-hours-calculator) |
| Producción BTC/día | [MiningNow.com](https://miningnow.com/) → campo "Income/day" |
| Tarifa eléctrica | Tu factura eléctrica (punta / llano / valle) |
| Precio de instalación | Presupuesto de instalador o tiendas online |

## ⚠️ Aviso

Esta herramienta es orientativa. Los resultados dependen de los datos introducidos y de variables externas (precio de Bitcoin, dificultad de la red, irradiación solar real, etc.). No constituye asesoramiento financiero ni de instalación.

---

Hecho con ❤️ para la comunidad de minería de Bitcoin.
