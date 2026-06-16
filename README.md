# Portafolio Profesional de Luis Téllez

Este repositorio contiene el código fuente del sitio web personal y portafolio profesional de **Luis Téllez**, configurado como una Single Page Application (SPA) responsiva, multilenguaje (ES/EN) y de alto impacto visual.

El sitio está diseñado proyectando una estética de "SOC" (Security Operations Center), con un estilo minimalista y glassmórfico ideal para directores y estrategas de ciberseguridad.

---

## 🚀 Arquitectura y Tecnologías

Para garantizar tiempos de carga ultrarrápidos, total portabilidad y un despliegue libre de mantenimiento en **GitHub Pages**, el sitio se construyó bajo la siguiente arquitectura:

1. **Frontend:** HTML5 semántico y CSS3 estructurado.
2. **Estilos y Diseño:** [Tailwind CSS](https://tailwindcss.com/) (importado vía CDN) integrado con un sistema de diseño personalizado (*Cyber Architect Elite*).
3. **Interactividad e i18n:** Vanilla JavaScript nativo (sin dependencias, frameworks ni pasos de compilación complejos).
4. **Tipografía:** Fuentes premium de Google Fonts:
   * **Hanken Grotesk:** Para encabezados y títulos ejecutivos.
   * **Inter:** Para textos de biografía y descripciones.
   * **JetBrains Mono:** Para etiquetas de tecnología, fechas y detalles monospaciados.

---

## ✨ Características Principales

* **Arquitectura SPA (Single Page Application):** Todo el contenido se carga instantáneamente en una sola vista, dividida por secciones con navegación de scroll suave (*smooth scroll*).
* **Internacionalización Dinámica (ES / EN):** Un selector en el encabezado permite alternar el idioma de todo el sitio al instante. Guarda la preferencia en el `localStorage` del navegador para recordar la elección del usuario en futuras visitas.
* **Optimización SEO Multilingüe:** Los metatítulos y metadescripciones se actualizan en el DOM en tiempo real al cambiar de idioma para mejorar el posicionamiento en motores de búsqueda.
* **Estructura Enriquecida del CV:** Incluye secciones detalladas basadas en la trayectoria profesional del cliente:
  * **Inicio (Hero):** Presentación ejecutiva y llamada a la acción hacia LinkedIn.
  * **Perfil:** Resumen estratégico de más de 15 años de liderazgo tecnológico.
  * **Trayectoria (Experiencia):** Línea de tiempo interactiva con las responsabilidades y fechas de cada rol corporativo.
  * **Educación:** Sección con los grados académicos actuales (Anáhuac e IPN).
  * **Logros:** Cuadrícula con efectos de brillo (*glow*) en hover sobre los hitos estratégicos de ciberseguridad y redes.
  * **Contacto:** Cierre minimalista con enlaces directos seguros.
* **Efectos y Animaciones:** Implementación de un *Intersection Observer* nativo en JS para activar transiciones suaves (*fade-in*) en cada sección a medida que el usuario hace scroll hacia abajo.

---

## 📁 Estructura del Proyecto

El proyecto está organizado de forma limpia en la raíz para permitir el despliegue automático de GitHub Pages:

```text
RepoLT/
├── assets/                     # Directorio de recursos estáticos
│   ├── banner.png              # Imagen panorámica del banner principal
│   ├── portrait_profile.png    # Retrato del perfil profesional
│   └── headshot.png            # Retrato circular del timeline
├── CNAME                       # Vinculación del dominio personalizado de GitHub Pages
├── index.html                  # Código HTML, CSS personalizado, diccionarios de traducción y JS
├── .gitignore                  # Exclusión de archivos fuente, temporales y del sistema
└── README.md                   # Documentación final de entrega (este archivo)
```

---

## 🔧 Configuración del Despliegue y DNS

El sitio está publicado en **GitHub Pages** y configurado para responder en el dominio personalizado **`https://www.tellez.com.mx`**.

### Configuración DNS Aplicada (en cdmon.net):

Para apuntar el dominio al sitio y permitir la redirección automática del dominio raíz (`tellez.com.mx` a `www.tellez.com.mx`), se configuraron los siguientes registros:

1. **Subdominio `www` (CNAME):**
   * **Host:** `www`
   * **Tipo:** `CNAME`
   * **Destino:** `LuisTellez03.github.io`

2. **Dominio Raíz `@` (Registros A):**
   * **Host:** `@` (vacío)
   * **Tipo:** `A`
   * **IPs de Destino (GitHub Pages):**
     * `185.199.108.153`
     * `185.199.109.153`
     * `185.199.110.153`
     * `185.199.111.153`

*Nota: El certificado SSL/TLS (HTTPS) se encuentra activo y forzado de forma nativa en la configuración de la página.*
