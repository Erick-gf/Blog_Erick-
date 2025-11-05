---
layout: default
title: Blog de Analítica Avanzada
---

<div style="background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%); padding: 3.5rem 2.5rem; border-radius: 20px; color: white; margin-bottom: 3rem; box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4); border: 1px solid #0f3460;">
  <h1 style="margin: 0; font-size: 3rem; font-weight: 800; letter-spacing: -1px;">Data Engineering Lab 🔧</h1>
  <p style="font-size: 1.3rem; margin-top: 1.5rem; opacity: 0.95; font-weight: 500; line-height: 1.6;">
    Análisis de datos a escala industrial. Aquí construyo pipelines robustos con <strong>Spark</strong>,
    proceso terabytes de información, y documento soluciones reales para problemas complejos.
    Sin florituras, solo código que funciona.
  </p>
  <div style="margin-top: 2rem; padding-top: 1.5rem; border-top: 1px solid rgba(255,255,255,0.1); display: flex; gap: 1.5rem; flex-wrap: wrap; align-items: center;">
    <span style="background: rgba(255,255,255,0.1); padding: 0.5rem 1.2rem; border-radius: 8px; font-size: 0.95rem; font-weight: 600;">⚡ Apache Spark</span>
    <span style="background: rgba(255,255,255,0.1); padding: 0.5rem 1.2rem; border-radius: 8px; font-size: 0.95rem; font-weight: 600;">🐍 Python/PySpark</span>
    <span style="background: rgba(255,255,255,0.1); padding: 0.5rem 1.2rem; border-radius: 8px; font-size: 0.95rem; font-weight: 600;">📊 Big Data Analytics</span>
  </div>
</div>

## 🛠️ Stack Tecnológico

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 1.5rem; margin: 3rem 0;">
  <div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2rem; border-radius: 16px; border: 2px solid #1a1a2e; box-shadow: 0 8px 24px rgba(0,0,0,0.2);">
    <div style="font-size: 2.5rem; margin-bottom: 0.8rem;">⚡</div>
    <strong style="color: #00d4ff; font-size: 1.2rem; display: block; margin-bottom: 0.5rem;">Apache Spark</strong>
    <span style="color: #94a3b8; font-size: 0.95rem;">Procesamiento distribuido a escala</span>
  </div>
  
  <div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2rem; border-radius: 16px; border: 2px solid #1a1a2e; box-shadow: 0 8px 24px rgba(0,0,0,0.2);">
    <div style="font-size: 2.5rem; margin-bottom: 0.8rem;">🐍</div>
    <strong style="color: #00d4ff; font-size: 1.2rem; display: block; margin-bottom: 0.5rem;">Python & PySpark</strong>
    <span style="color: #94a3b8; font-size: 0.95rem;">Ingeniería de datos eficiente</span>
  </div>
  
  <div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2rem; border-radius: 16px; border: 2px solid #1a1a2e; box-shadow: 0 8px 24px rgba(0,0,0,0.2);">
    <div style="font-size: 2.5rem; margin-bottom: 0.8rem;">🌊</div>
    <strong style="color: #00d4ff; font-size: 1.2rem; display: block; margin-bottom: 0.5rem;">Streaming Real-Time</strong>
    <span style="color: #94a3b8; font-size: 0.95rem;">Datos en movimiento 24/7</span>
  </div>
  
  <div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2rem; border-radius: 16px; border: 2px solid #1a1a2e; box-shadow: 0 8px 24px rgba(0,0,0,0.2);">
    <div style="font-size: 2.5rem; margin-bottom: 0.8rem;">📊</div>
    <strong style="color: #00d4ff; font-size: 1.2rem; display: block; margin-bottom: 0.5rem;">Data Visualization</strong>
    <span style="color: #94a3b8; font-size: 0.95rem;">Insights accionables</span>
  </div>
</div>

---

## 📖 Artículos Técnicos

{% for post in site.posts %}
<article style="background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%); border-radius: 16px; padding: 2.5rem; margin-bottom: 2.5rem; box-shadow: 0 10px 40px rgba(0,0,0,0.3); border-left: 4px solid #00d4ff; transition: transform 0.3s, box-shadow 0.3s;">
  
  <h3 style="margin-top: 0; font-size: 1.8rem; font-weight: 700;">
    <a href="{{ post.url | relative_url }}" style="color: #00d4ff; text-decoration: none; transition: color 0.3s;">
      {{ post.title }}
    </a>
  </h3>
  
  <div style="color: #94a3b8; font-size: 0.9rem; margin-bottom: 1.5rem; display: flex; align-items: center; gap: 1.5rem; flex-wrap: wrap;">
    <span style="display: flex; align-items: center; gap: 0.4rem;">
      <span style="color: #00d4ff;">📅</span> {{ post.date | date: "%d %b %Y" }}
    </span>
    {% if post.author %}
    <span style="display: flex; align-items: center; gap: 0.4rem;">
      <span style="color: #00d4ff;">✍️</span> {{ post.author }}
    </span>
    {% endif %}
    <span style="display: flex; align-items: center; gap: 0.4rem;">
      <span style="color: #00d4ff;">⏱️</span> 8 min
    </span>
  </div>
  
  <p style="color: #cbd5e1; line-height: 1.8; margin-bottom: 1.8rem; font-size: 1.05rem;">
    {{ post.excerpt | strip_html | truncatewords: 40 }}
  </p>
  
  {% if post.categories %}
  <div style="margin-bottom: 1.8rem; display: flex; flex-wrap: wrap; gap: 0.6rem;">
    {% for category in post.categories %}
    <span style="background: rgba(0, 212, 255, 0.1); color: #00d4ff; padding: 0.4rem 1rem; border-radius: 6px; font-size: 0.85rem; font-weight: 600; border: 1px solid rgba(0, 212, 255, 0.3); text-transform: uppercase; letter-spacing: 0.5px;">
      {{ category }}
    </span>
    {% endfor %}
  </div>
  {% endif %}
  
  <a href="{{ post.url | relative_url }}" style="display: inline-flex; align-items: center; gap: 0.6rem; padding: 0.9rem 2rem; background: linear-gradient(135deg, #00d4ff 0%, #0099cc 100%); color: #0a0e27; text-decoration: none; border-radius: 8px; font-weight: 700; transition: all 0.3s; box-shadow: 0 4px 20px rgba(0, 212, 255, 0.3); text-transform: uppercase; letter-spacing: 0.5px; font-size: 0.9rem;">
    Leer Análisis Completo
    <span style="transition: transform 0.3s; font-size: 1.2rem;">→</span>
  </a>
  
</article>
{% endfor %}

---

## 🎯 Contenido del Blog

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; margin: 3rem 0;">
  
  <div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2.5rem; border-radius: 16px; border: 2px solid #1a1a2e; box-shadow: 0 10px 30px rgba(0,0,0,0.3);">
    <div style="font-size: 3rem; margin-bottom: 1.2rem;">🔬</div>
    <h4 style="color: #00d4ff; margin: 0 0 1rem 0; font-size: 1.3rem; font-weight: 700;">Casos de Uso Reales</h4>
    <p style="color: #cbd5e1; margin: 0; line-height: 1.7; font-size: 1.05rem;">
      Implementaciones production-ready con datasets empresariales. Arquitecturas escalables 
      y patrones de diseño probados en entornos de alta demanda.
    </p>
  </div>
  
  <div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2.5rem; border-radius: 16px; border: 2px solid #1a1a2e; box-shadow: 0 10px 30px rgba(0,0,0,0.3);">
    <div style="font-size: 3rem; margin-bottom: 1.2rem;">⚙️</div>
    <h4 style="color: #00d4ff; margin: 0 0 1rem 0; font-size: 1.3rem; font-weight: 700;">Código Optimizado</h4>
    <p style="color: #cbd5e1; margin: 0; line-height: 1.7; font-size: 1.05rem;">
      Soluciones eficientes con análisis de performance. Cada línea de código está 
      documentada y optimizada para rendimiento máximo.
    </p>
  </div>
  
  <div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2.5rem; border-radius: 16px; border: 2px solid #1a1a2e; box-shadow: 0 10px 30px rgba(0,0,0,0.3);">
    <div style="font-size: 3rem; margin-bottom: 1.2rem;">📈</div>
    <h4 style="color: #00d4ff; margin: 0 0 1rem 0; font-size: 1.3rem; font-weight: 700;">Analytics Avanzado</h4>
    <p style="color: #cbd5e1; margin: 0; line-height: 1.7; font-size: 1.05rem;">
      Visualizaciones técnicas que revelan insights profundos. Dashboards interactivos 
      diseñados para toma de decisiones estratégicas.
    </p>
  </div>
  
  <div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2.5rem; border-radius: 16px; border: 2px solid #1a1a2e; box-shadow: 0 10px 30px rgba(0,0,0,0.3);">
    <div style="font-size: 3rem; margin-bottom: 1.2rem;">🚀</div>
    <h4 style="color: #00d4ff; margin: 0 0 1rem 0; font-size: 1.3rem; font-weight: 700;">Best Practices</h4>
    <p style="color: #cbd5e1; margin: 0; line-height: 1.7; font-size: 1.05rem;">
      Metodologías industry-standard y técnicas de optimización. Aprendizajes 
      de proyectos reales en ambientes de producción.
    </p>
  </div>
  
</div>

---

## 👨‍💻 Sobre el Autor

<div style="background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%); padding: 3rem; border-radius: 16px; border-left: 5px solid #00d4ff; box-shadow: 0 10px 40px rgba(0,0,0,0.3);">
  
  <p style="font-size: 1.2rem; color: #e2e8f0; line-height: 1.8; margin-bottom: 1.8rem; font-weight: 500;">
    <strong style="color: #00d4ff; font-size: 1.3rem;">Erick Gonzalez</strong> — Ingeniero de Datos especializado 
    en procesamiento distribuido y sistemas de Big Data. Mi enfoque está en construir arquitecturas robustas 
    que procesen millones de eventos por segundo sin inmutarse.
  </p>
  
  <p style="color: #cbd5e1; line-height: 1.8; margin-bottom: 1.8rem; font-size: 1.05rem;">
    Este blog documenta implementaciones técnicas, benchmarks de performance, y arquitecturas de datos 
    que he diseñado y optimizado. Es mi repositorio de conocimiento técnico aplicado.
  </p>
  
  <div style="background: rgba(0, 212, 255, 0.05); padding: 1.5rem; border-radius: 12px; border-left: 3px solid #00d4ff;">
    <p style="color: #e2e8f0; line-height: 1.8; margin: 0; font-size: 1.05rem;">
      <strong style="color: #00d4ff;">Filosofía:</strong> El código debe ser elegante, eficiente y mantenible. 
      Si una solución requiere explicación compleja, probablemente necesita refactoring. Creo en la documentación 
      técnica precisa y en compartir conocimiento que resuelva problemas reales.
    </p>
  </div>
  
</div>

---

## 💬 Contacto Técnico

<div style="background: linear-gradient(135deg, #0f3460 0%, #16213e 100%); padding: 2.5rem; border-radius: 16px; border: 2px solid #1a1a2e; text-align: center; box-shadow: 0 10px 30px rgba(0,0,0,0.3);">
  <p style="color: #e2e8f0; font-size: 1.15rem; margin-bottom: 1.2rem; font-weight: 500;">
    ¿Preguntas técnicas, sugerencias de optimización o bugs en el código?
  </p>
  <p style="color: #94a3b8; margin: 0; font-size: 1.05rem; line-height: 1.6;">
    Deja tus comentarios en cualquier artículo. Siempre estoy abierto a discusiones técnicas 
    y mejoras de arquitectura. El peer review hace mejor código.
  </p>
</div>

---

<div style="text-align: center; padding: 3rem; background: linear-gradient(135deg, #0a0e27 0%, #16213e 100%); border-radius: 16px; margin-top: 4rem; border: 2px solid #1a1a2e; box-shadow: 0 10px 40px rgba(0,0,0,0.4);">
  <p style="color: #94a3b8; margin: 0; font-size: 1rem; font-weight: 600; text-transform: uppercase; letter-spacing: 1px;">
    <strong style="color: #00d4ff;">Stack:</strong> Jekyll • GitHub Pages • Apache Spark • Python • Docker
  </p>
  <p style="color: #64748b; font-size: 0.9rem; margin-top: 1rem;">
    Build: {{ site.time | date: "%Y.%m.%d" }} | Última actualización: {{ site.time | date: "%d %B %Y" }}
  </p>
</div>