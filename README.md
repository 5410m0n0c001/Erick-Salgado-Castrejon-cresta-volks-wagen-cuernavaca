# Tarjeta Digital Profesional - Erick Salgado Castrejon

Tarjeta de presentación digital premium para Erick Salgado Castrejon, Gerente de Cresta Volkswagen Cuernavaca. Desplegada automáticamente en GitHub Pages.

## 🚀 Características

- **Diseño Premium**: Glassmorphism con paleta de colores Volkswagen
- **Responsive**: Optimizado para móvil, tablet y desktop
- **Animaciones Modernas**: Scroll-triggered animations y micro-interacciones
- **Accesibilidad**: Navegación por teclado y soporte para lectores de pantalla
- **Performance**: Optimizado para carga rápida y Lighthouse score > 90
- **Funcionalidades**:
  - Botones CTA funcionales (llamadas, WhatsApp, email, ubicación)
  - Descarga automática de vCard
  - Redes sociales desplegables
  - Videos de fondo optimizados
  - Cursor personalizado y efectos magnéticos

## 📁 Estructura del Proyecto

```
wolkswaguen/
├── index.html          # Archivo principal
├── README.md           # Este archivo
└── assets/             # Recursos multimedia
    ├── logo.png        # Logo para botón flotante
    ├── hero.mp4        # Video de fondo hero
    ├── footer.mp4      # Video de fondo footer
    └── poster.mp4      # Video adicional (si se usa)
```

## 🛠️ Tecnologías Utilizadas

- **HTML5**: Semántico y accesible
- **CSS3**: Grid, Flexbox, Custom Properties, Animations
- **Vanilla JavaScript**: ES6+ sin frameworks
- **Librerías CDN**:
  - AOS (Animate On Scroll)
  - Font Awesome (Iconos)

## 🚀 Despliegue en GitHub Pages

### Opción 1: Desde VS Code (Recomendado)

1. **Crear repositorio en GitHub**:
   ```bash
   # En VS Code, abre el terminal integrado
   git init
   git add .
   git commit -m "feat: initial digital business card"
   ```

2. **Crear repositorio en GitHub**:
   - Ve a https://github.com/new
   - Nombre: `tu-usuario.github.io` (para página principal) o cualquier nombre
   - Haz push inicial:
   ```bash
   git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
   git push -u origin main
   ```

3. **Activar GitHub Pages**:
   - Ve a Settings > Pages en tu repositorio
   - Selecciona branch `main` (o `master`)
   - Source: `/(root)`
   - Save

4. **URL final**: `https://tu-usuario.github.io/tu-repo/`

### Opción 2: GitHub Actions (Avanzado)

Crea `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3

    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18'

    - name: Install dependencies
      run: npm install

    - name: Build
      run: npm run build

    - name: Deploy
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./dist
```

## 📱 Personalización

### Cambiar Información Personal

Edita las variables en `index.html`:

```javascript
// En la función downloadVCard()
const vCardData = `BEGIN:VCARD
VERSION:3.0
FN:Tu Nombre Completo
TITLE:Tu Cargo
ORG:Tu Empresa
TEL;TYPE=CELL:+52XXXXXXXXXX
TEL;TYPE=WORK:+52XXXXXXXXXX
EMAIL:tu-email@empresa.com
URL:https://tu-sitio-web.com/
END:VCARD`;
```

### Cambiar Colores

Modifica las variables CSS en `:root`:

```css
:root {
    --vw-blue: #001E50;
    --vw-light-blue: #00B0F0;
    --white: #FFFFFF;
    /* ... otros colores */
}
```

### Actualizar Enlaces

Cambia los href en los botones CTA:

```html
<a href="tel:+52XXXXXXXXXX">Llamar Móvil</a>
<a href="https://wa.me/52XXXXXXXXXX?text=Mensaje">WhatsApp</a>
<a href="mailto:tu-email@empresa.com">Email</a>
<a href="https://maps.app.goo.gl/TU-UBICACION">Ubicación</a>
<a href="https://tu-sitio-web.com/">Sitio Web</a>
```

## 🎨 Efectos Visuales

### Animaciones Implementadas

- **Text Reveal**: Nombre aparece con animación letra por letra
- **Scroll Animations**: Elementos aparecen al hacer scroll (AOS)
- **Magnetic Buttons**: Botones atraen el cursor
- **Glassmorphism**: Efectos de vidrio con backdrop-filter
- **Custom Cursor**: Cursor azul que sigue el mouse (desktop)
- **Hover Effects**: Transformaciones 3D y glow effects

### Responsive Breakpoints

- **Mobile**: < 768px - Botones en columna, cursor deshabilitado
- **Tablet**: 768px - 1024px - Grid de 3 columnas
- **Desktop**: > 1024px - Todos los efectos activos

## 🔧 Optimizaciones de Performance

- **Lazy Loading**: Videos se cargan solo cuando son visibles
- **WebP Fallback**: Para compatibilidad con navegadores antiguos
- **Reduced Motion**: Respeta la preferencia del usuario
- **Optimized Assets**: Videos comprimidos para web
- **CDN Libraries**: Librerías externas para mejor caching

## 📊 Compatibilidad

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ iOS Safari 14+
- ✅ Android Chrome 90+

## 🐛 Solución de Problemas

### Videos no se reproducen
- Verifica que los archivos estén en `/assets/`
- Asegúrate de que sean formato MP4/WebM
- Comprueba permisos CORS si usas CDN

### Animaciones no funcionan
- Verifica que AOS esté cargando correctamente
- Revisa consola del navegador por errores
- Confirma que no tengas `prefers-reduced-motion: reduce`

### Botones no responden en móvil
- Asegúrate de que los `tel:` y `mailto:` links estén correctos
- Prueba en dispositivo real, no solo emulador

## 📈 Mejoras Futuras

- [ ] Integración con Google Analytics
- [ ] Modo oscuro automático
- [ ] PWA (Progressive Web App)
- [ ] Multi-idioma (ES/EN)
- [ ] Formulario de contacto integrado
- [ ] Integración con CRM

## 📞 Soporte

Para soporte técnico o personalizaciones:
- Email: erick.crestavw@gmail.com
- Tel: +52 777 367 6346

---

**Desarrollado con ❤️ para Cresta Volkswagen Cuernavaca**