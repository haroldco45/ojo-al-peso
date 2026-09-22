# Ojo al peso: la JEP en cifras

App ciudadana (PWA) que muestra cuánto cuesta la Jurisdicción Especial para la Paz, qué ha entregado y cuánto le toca a cada contribuyente. Cada cifra lleva su fuente.

**En vivo:** https://haroldco45.github.io/ojo-al-peso/

## Qué incluye

- Recibo del contribuyente: presupuesto 2026 repartido por persona y por hogar.
- Calculadora de costo por decisión con las cifras de Gobierno, analistas y del debate en la Cámara.
- Presupuesto año por año (2022 a 2027).
- Transcripción del debate de la Comisión Primera (9 de septiembre de 2026).
- Argumentos de los críticos y respuesta de la JEP.
- Derecho de petición listo para copiar y botón para compartir por WhatsApp.
- Funciona sin conexión e instalable en el celular.

## Estructura

```
index.html              App completa (HTML, CSS y JS en un solo archivo)
manifest.webmanifest    Manifiesto PWA
sw.js                   Service worker (red primero para el HTML, caché para lo demás)
icons/                  Íconos 192, 512 y maskable
og.png                  Imagen de vista previa para WhatsApp y redes
.nojekyll               Evita que GitHub Pages procese el sitio con Jekyll
```

## Publicar en GitHub Pages

1. Crear el repositorio `ojo-al-peso` en la cuenta `haroldco45` (público).
2. Subir todos los archivos a la rama `main`, en la raíz.
3. Ir a **Settings → Pages**, en *Source* elegir **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guardar.
4. En uno o dos minutos queda en `https://haroldco45.github.io/ojo-al-peso/`.

## Actualizar cifras

Los datos están en `index.html`:
- `BUDGET_2026`, `POP` y `ADULTS` en el bloque del recibo.
- El arreglo `data` de la gráfica de presupuesto.
- Las opciones de la calculadora (`name="m"` y `name="o"`).

Al cambiar datos, sube la versión de `CACHE` en `sw.js` (por ejemplo `ojo-al-peso-v2-AAAA-MM-DD`) para que los celulares descarguen la nueva versión.

## Fuentes

Cámara de Representantes, El Tiempo, Cambio, Minuto60, Blu Radio, Infobae, IFM Noticias y proyecciones de población del DANE. Los enlaces están al final de la app.

Corte de cifras: 22 de septiembre de 2026 (hora de Colombia, UTC-5).

---
Hecho por **Vibras Positivas HM**, Caucasia, Antioquia.
