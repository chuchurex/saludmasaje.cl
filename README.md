# SaludMasaje.cl - Sitio Web

Sitio web profesional para servicios de masajes terapéuticos de Javier Mena.

## 🚀 Despliegue en Cloudflare Pages

### Opción 1: Despliegue Directo (Recomendado)

1. **Subir a GitHub:**
   ```bash
   cd saludmasaje
   git init
   git add .
   git commit -m "Initial commit - SaludMasaje website"
   git branch -M main
   git remote add origin https://github.com/chuchurex/saludmasaje.cl.git
   git push -u origin main
   ```

2. **Conectar con Cloudflare Pages:**
   - Ve a [Cloudflare Dashboard](https://dash.cloudflare.com)
   - Navega a **Workers & Pages** > **Create application** > **Pages**
   - Selecciona **Connect to Git**
   - Autoriza y selecciona el repositorio `saludmasaje.cl`
   - Configuración de build:
     - **Framework preset:** None
     - **Build command:** (dejar vacío)
     - **Build output directory:** `/` o `.`
   - Click en **Save and Deploy**

3. **Configurar Dominio Personalizado:**
   - En el proyecto de Pages, ve a **Custom domains**
   - Añade `saludmasaje.cl`
   - Si el dominio ya está en Cloudflare, se configurará automáticamente

### Opción 2: Despliegue Manual con Wrangler

```bash
# Instalar Wrangler (si no lo tienes)
npm install -g wrangler

# Login en Cloudflare
wrangler login

# Desplegar
wrangler pages deploy . --project-name=saludmasaje
```

## 📁 Estructura del Proyecto

```
saludmasaje/
├── index.html      # Página principal (todo incluido)
└── README.md       # Este archivo
```

## ✨ Características

- ✅ Diseño responsive (móvil, tablet, desktop)
- ✅ Optimizado para SEO
- ✅ Botón flotante de WhatsApp
- ✅ Formulario de contacto que envía a WhatsApp
- ✅ Animaciones suaves al scroll
- ✅ Tabs para servicios empresas/particulares
- ✅ FAQ acordeón interactivo
- ✅ Paleta de colores corporativa (azul/violeta)
- ✅ Carga ultra rápida (single HTML file)

## 🎨 Personalización

### Cambiar colores
Edita las variables CSS en `:root` al inicio del archivo:
```css
--primary: #2d5a87;        /* Azul principal */
--accent-violet: #6b5b95;  /* Violeta acento */
--accent-warm: #d4a574;    /* Dorado cálido */
```

### Cambiar precios
Busca las clases `.service-price` en el HTML y modifica los valores.

### Agregar logo
Reemplaza el emoji 💆 en `.logo-icon` por una imagen:
```html
<div class="logo-icon">
    <img src="logo.png" alt="SaludMasaje" style="width:100%;height:100%;object-fit:contain">
</div>
```

### Testimonios
Los testimonios actuales son de ejemplo. Reemplázalos con testimonios reales cuando estén disponibles.

## 📱 Contacto configurado

- **WhatsApp:** +56 9 9539 9487
- **Email:** javier@saludmasaje.cl
- **Cobertura:** Santiago de Chile

## 🔧 Próximos pasos (Fase 2)

- [ ] Sistema de agendamiento online (Calendly o similar)
- [ ] Integración con Google Calendar
- [ ] Testimonios dinámicos desde base de datos
- [ ] Blog con artículos de bienestar
- [ ] Versión en inglés

## 📄 Licencia

© 2026 SaludMasaje - Javier Mena. Todos los derechos reservados.

---

Desarrollado por [Chuchurex](https://chuchurex.cl) 🚀
