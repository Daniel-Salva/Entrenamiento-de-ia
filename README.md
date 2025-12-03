# <img src="./LogotipoV2-Simple.png" alt="Logotipo" width="56" height="56" /> Entrenamiento-de-ia

![Author](https://img.shields.io/badge/Author-Daniel--Salva-blue?style=for-the-badge&logo=github) ![Language](https://img.shields.io/badge/Languages-Jupyter%20Notebook-orange?style=for-the-badge) ![License](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)

¡Bienvenido! Esta es una demo de un modelo de IA que se ejecuta en el navegador (TensorFlow.js) y viene con un notebook de Google Colab para experimentar. El README está diseñado para ser claro, visual y con tu nombre visible como autor.

## 🚀 Resumen rápido
- index.html — Interfaz web que carga el modelo y hace inferencia en el cliente.  
- model.json — Manifiesto del modelo (formato TF.js).  
- group1-shard1of2.bin, group1-shard2of2.bin — Pesos del modelo (shards).  
- Te_damos_la_bienvenida_a_Colab.ipynb — Notebook para abrir en Google Colab.  
- LogotipoV2-Simple.png, favicon-* — Assets visuales.

## ▶️ Cómo ejecutar (local)
1. Clona el repositorio:
   ```
   git clone https://github.com/Daniel-Salva/Entrenamiento-de-ia.git
   ```
2. Entra al directorio:
   ```
   cd Entrenamiento-de-ia
   ```
3. Sirve los archivos estáticos (ejemplo con Python):
   ```
   python -m http.server 8000
   ```
4. Abre en tu navegador:
   ```
   http://localhost:8000/index.html
   ```

> Por seguridad del navegador, sirve por HTTP (no abras index.html con file://), así evitarás errores al cargar model.json y los .bin.

## 📘 Abrir el notebook
- Haz clic en `Te_damos_la_bienvenida_a_Colab.ipynb` en GitHub y selecciona "Open in Colab", o súbelo a Colab manualmente.

## 🌐 Despliegue en GitHub Pages
Activa GitHub Pages en la configuración del repo (branch: main, folder: /root). La URL será:
```
https://Daniel-Salva.github.io/Entrenamiento-de-ia/index.html
```

## 🔧 Notas técnicas
- `model.json` debe poder acceder a los shards por rutas relativas (p. ej. `group1-shard1of2.bin`).
- Si reexportas el modelo con `tensorflowjs_converter`, se generarán `model.json` y los .bin.

## ✨ Tu nombre en la documentación y en la demo
Ya incluí un badge de autor en la cabecera para que tu nombre aparezca en el README. Si quieres que tu nombre también aparezca dentro de la demo (index.html), añade este pequeño snippet dentro del body de `index.html` (por ejemplo justo dentro del contenedor principal) y el CSS al head o a tu archivo CSS:

HTML (añadir donde quieras mostrar tu nombre):
```html
<div id="owner-badge" class="owner-badge">Daniel-Salva</div>
```

CSS (añadir en <style> o css):
```css
.owner-badge {
  position: fixed;
  bottom: 16px;
  right: 16px;
  background: rgba(0,0,0,0.65);
  color: #fff;
  padding: 8px 12px;
  border-radius: 12px;
  font-family: "Segoe UI", Roboto, Arial, sans-serif;
  font-size: 13px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.3);
  z-index: 9999;
}
```

Con eso tu nombre estará visible en cada página de la demo como un badge discreto.

## ✅ Buenas prácticas recomendadas
- Añadir `LICENSE` (recomiendo MIT si quieres apertura).  
- Considerar Git LFS si los .bin son grandes.  
- Añadir `CONTRIBUTING.md` si esperas colaboraciones.

## 🤝 Créditos y contacto
- Autor: **Daniel-Salva** — https://github.com/Daniel-Salva  
- Si quieres, puedo crear un PR que reemplace el README actual por este (o añadir además docs/DOCUMENTATION.md). Dime si quieres que lo haga y en qué rama prefieres el cambio.
