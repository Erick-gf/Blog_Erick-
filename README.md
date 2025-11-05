# 🔧 Data Engineering Blog - Erick Gonzalez

Blog técnico profesional para análisis de datos a escala con Apache Spark. Construido con Jekyll, optimizado para GitHub Pages.

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/ErickGonzalez/data-engineering-blog)
[![Jekyll](https://img.shields.io/badge/jekyll-4.3.0-red)](https://jekyllrb.com/)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

## 🚀 Quick Start

### Prerrequisitos

```bash
# Ruby 3.x (Windows: https://rubyinstaller.org/)
ruby -v  # >= 3.0.0

# Bundler
gem -v   # >= 2.0.0
```

### Instalación

```bash
# 1. Clonar repositorio
git clone https://github.com/ErickGonzalez/data-engineering-blog.git
cd data-engineering-blog

# 2. Instalar dependencias Ruby
gem install bundler jekyll
bundle install

# 3. Instalar dependencias Python (para gráficas)
pip install matplotlib pandas numpy seaborn scipy

# 4. Generar visualizaciones
python generate_graphs.py

# 5. Iniciar servidor de desarrollo
bundle exec jekyll serve --livereload

# Acceder en: http://localhost:4000
```

## 📁 Estructura del Proyecto

```
data-engineering-blog/
│
├── _config.yml                 # Configuración Jekyll (autor: Erick Gonzalez)
│
├── _includes/                  # Componentes modulares
│   ├── head.html              # Meta tags, CSS, SEO
│   └── footer.html            # Footer con enlaces técnicos
│
├── _layouts/                   # Templates
│   ├── default.html           # Layout principal (dark theme)
│   └── post.html              # Template para artículos técnicos
│
├── _posts/                     # Artículos del blog
│   └── 2025-10-29-analisis-clickstream-spark.md
│
├── assets/
│   ├── css/
│   │   └── style.css          # Diseño varonil profesional
│   │
│   ├── images/                # Visualizaciones generadas
│   │   ├── top_users_chart.png
│   │   ├── temporal_analysis.png
│   │   ├── clicks_vs_sessions.png
│   │   ├── user_distribution.png
│   │   └── activity_heatmap.png
│   │
│   └── data/
│       └── clickstream_data.csv
│
├── _site/                      # Sitio generado (no versionar)
├── index.md                    # Homepage
├── generate_graphs.py          # Script de visualizaciones
├── Gemfile                     # Dependencias Ruby
└── README.md                   # Este archivo
```

## 🎨 Personalización

### Actualizar Información del Autor

Editar `_config.yml`:

```yaml
title: "Data Engineering Lab - Erick Gonzalez"
description: "Análisis de Datos a Escala Industrial con Apache Spark"
author:
  name: "Erick Gonzalez"
  bio: "Data Engineer | Big Data Specialist"

baseurl: "/data-engineering-blog"
url: "https://ErickGonzalez.github.io"
```

### Crear Nuevo Artículo

```bash
# 1. Crear archivo en _posts/ con formato: YYYY-MM-DD-titulo.md
touch _posts/2025-11-15-kafka-spark-integration.md
```

```markdown
---
layout: post
title: "Integración Real-Time: Kafka + Spark Structured Streaming"
date: 2025-11-15
author: Erick Gonzalez
categories: [kafka, spark, streaming, real-time]
---

# Tu contenido técnico aquí

## Arquitectura

...

## Código

```python
# Tu código PySpark
```
```

### Modificar Diseño

El tema dark profesional está en `assets/css/style.css`:

```css
:root {
  --primary: #00d4ff;      /* Azul eléctrico */
  --bg-primary: #0a0e27;   /* Fondo oscuro */
  --text-primary: #e2e8f0; /* Texto claro */
}
```

## 📊 Generar Visualizaciones

El script `generate_graphs.py` crea 5 gráficas técnicas:

```bash
python generate_graphs.py
```

**Output:**
1. `top_users_chart.png` — Top 15 usuarios por actividad
2. `temporal_analysis.png` — Serie temporal de clicks
3. `clicks_vs_sessions.png` — Análisis de correlación
4. `user_distribution.png` — Histograma de distribución
5. `activity_heatmap.png` — Heatmap de actividad por usuario/tiempo

### Personalizar Gráficas

```python
# Editar generate_graphs.py

# Cambiar colores (esquema dark tech)
colors = {
    'primary': '#00d4ff',
    'secondary': '#0f3460',
    'accent': '#e94560'
}

# Ajustar tamaño
plt.figure(figsize=(14, 8))

# Cambiar estilo
plt.style.use('dark_background')
```

## 🚀 Despliegue en GitHub Pages

### Opción 1: Repositorio Personal (username.github.io)

```bash
# 1. Crear repo: ErickGonzalez.github.io
# 2. Clonar y subir archivos
git init
git add .
git commit -m "Initial deployment - Data Engineering Blog"
git branch -M main
git remote add origin https://github.com/ErickGonzalez/ErickGonzalez.github.io.git
git push -u origin main

# 3. Acceder en: https://ErickGonzalez.github.io
```

### Opción 2: Repositorio de Proyecto

```bash
# 1. Crear repo: data-engineering-blog
# 2. Actualizar _config.yml:
baseurl: "/data-engineering-blog"
url: "https://ErickGonzalez.github.io"

# 3. Subir a GitHub
git push

# 4. Habilitar Pages
# Settings > Pages > Branch: main > Save

# 5. Acceder en: https://ErickGonzalez.github.io/data-engineering-blog
```

### CI/CD con GitHub Actions

Crear `.github/workflows/jekyll.yml`:

```yaml
name: Deploy Jekyll

on:
  push:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Setup Ruby
        uses: ruby/setup-ruby@v1
        with:
          ruby-version: 3.0
          bundler-cache: true
      
      - name: Build site
        run: bundle exec jekyll build
      
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./_site
```

## 🔧 Comandos Útiles

```bash
# Desarrollo local
bundle exec jekyll serve --livereload --drafts

# Build de producción
bundle exec jekyll build

# Limpiar archivos generados
bundle exec jekyll clean

# Verificar configuración
bundle exec jekyll doctor

# Actualizar dependencias
bundle update

# Ver versiones
bundle exec jekyll -v
ruby -v
gem -v
```

## 📝 Formato de Posts Técnicos

### Front Matter Completo

```yaml
---
layout: post
title: "Título Técnico del Artículo"
date: 2025-10-29
author: Erick Gonzalez
categories: [spark, kafka, streaming, ml]
tags: [apache-spark, pyspark, real-time, big-data]
excerpt: "Breve descripción para SEO (160 chars max)"
image: /assets/images/post-cover.png
comments: true
---
```

### Sintaxis Markdown

**Código con syntax highlighting:**

````markdown
```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("DataEngineering") \
    .getOrCreate()
```
````

**Imágenes:**

```markdown
![Descripción técnica]({{ "/assets/images/diagram.png" | relative_url }})
```

**Tablas técnicas:**

```markdown
| Métrica | Value | Status |
|---------|-------|--------|
| Latency P99 | 1.8s | ✅ |
| Throughput | 48K/s | ✅ |
```

**Alertas/Callouts:**

```markdown
> **⚠️ Importante:** Configurar `spark.sql.shuffle.partitions` según tamaño del cluster.
```

## 🐛 Troubleshooting

### Error: "Could not find gem 'jekyll'"

```bash
gem install jekyll bundler
bundle install
```

### Error: "Port 4000 already in use"

```bash
# Opción 1: Cambiar puerto
bundle exec jekyll serve --port 4001

# Opción 2: Matar proceso
lsof -ti:4000 | xargs kill -9  # Linux/Mac
netstat -ano | findstr :4000   # Windows
```

### Gráficas no se muestran

```bash
# Verificar existencia
ls -la assets/images/

# Regenerar todas
python generate_graphs.py

# Verificar permisos
chmod 644 assets/images/*.png
```

### Cambios CSS no se reflejan

```bash
# Limpiar cache
bundle exec jekyll clean

# Rebuild completo
bundle exec jekyll build --verbose

# Forzar recarga en navegador
Ctrl+Shift+R (Windows/Linux)
Cmd+Shift+R (Mac)
```

### Build falla en GitHub Pages

```bash
# Verificar compatibilidad de gems
bundle exec github-pages health-check

# Ver logs detallados
# Settings > Pages > Ver deployment logs

# Validar _config.yml
bundle exec jekyll doctor
```

## 📚 Recursos Técnicos

### Jekyll & Ruby
- [Jekyll Docs](https://jekyllrb.com/docs/)
- [Liquid Templates](https://shopify.github.io/liquid/)
- [GitHub Pages](https://pages.github.com/)

### Apache Spark
- [Spark Documentation](https://spark.apache.org/docs/latest/)
- [PySpark API](https://spark.apache.org/docs/latest/api/python/)
- [Structured Streaming](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html)

### Data Engineering
- [Kafka Documentation](https://kafka.apache.org/documentation/)
- [Delta Lake](https://delta.io/)
- [AWS EMR](https://aws.amazon.com/emr/)

## 🤝 Contribuciones

Este es un blog personal, pero sugerencias son bienvenidas:

1. Fork el repositorio
2. Crea tu feature branch (`git checkout -b feature/mejora-visualizacion`)
3. Commit cambios (`git commit -m 'Add: nueva gráfica de distribución'`)
4. Push a branch (`git push origin feature/mejora-visualizacion`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo licencia MIT. Ver archivo [LICENSE](LICENSE) para detalles.

## 👨‍💻 Autor

**Erick Gonzalez**  
Data Engineer | Big Data Specialist

- GitHub: [@ErickGonzalez](https://github.com/ErickGonzalez)
- LinkedIn: [Erick Gonzalez](https://linkedin.com/in/erick-gonzalez)
- Email: erick.gonzalez@dataengineering.tech

---

**Stack:** Jekyll 4.3 • GitHub Pages • Apache Spark • Python • PySpark  
**Última actualización:** Noviembre 2025  
**Curso:** Analítica Avanzada 2025

---

<div align="center">
  <strong>Built with ⚡ by Erick Gonzalez</strong>
</div>