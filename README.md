# Connor Barrett - Portfolio Website

A clean, responsive portfolio website showcasing full-stack development experience with a focus on environmental impact and clean energy solutions.

## 🏗️ Architecture Overview

This is a **static website** originally designed in Webflow and then customized with hand-coded improvements for better performance, accessibility, and maintainability. The architecture follows a simple but effective pattern for a personal portfolio site.

### Technology Stack

- **Frontend**: Vanilla HTML5, CSS3, JavaScript
- **Design System**: Webflow-generated CSS with custom modifications
- **Forms**: Formspree API for contact form handling
- **Hosting**: GitHub Pages
- **Domain**: Google Domains
- **Font Loading**: Google Fonts (Manrope)
- **Version Control**: Git/GitHub

## 📁 Project Structure

```
my-webflow-portfolio/
├── index.html             # Main page (single-page application)
├── 401.html               # Unauthorized access page
├── 404.html               # Page not found
├── css/
│   ├── normalize.css      # CSS reset/normalization
│   ├── webflow.css        # Core Webflow framework styles
│   └── connor-freelance-portfolio-23-24.webflow.css  # Custom styles
├── js/
│   └── webflow.js         # Webflow interactive components
├── images/                # Optimized images with multiple resolutions
│   ├── Cover-Me1*.png     # Profile images (multiple sizes)
│   ├── project-images/    # Project screenshots
│   └── travel-photos/     # Personal photography
└── .github/
    └── workflows/
        └── static.yml     # GitHub Pages deployment
```

## 🎨 Design System

### CSS Architecture
The styling follows a **three-layer approach**:

1. **Base Layer** (`normalize.css`): Cross-browser consistency
2. **Framework Layer** (`webflow.css`): Webflow's component system and utilities
3. **Custom Layer** (`connor-freelance-portfolio-23-24.webflow.css`): Site-specific styles

### Color Palette
```css
:root {
  --primary-500: #09de67;    /* Primary green */
  --neutral-950: #151c1e;    /* Dark text */
  --neutral-50: #f5f8f8;     /* Light background */
  --warning-500: #f73c3c;    /* Error states */
  /* Earth-toned palette supporting environmental theme */
}
```

### Responsive Design
- **Desktop First**: Designed for desktop, then adapted
- **Breakpoints**: 991px, 767px, 479px
- **Grid System**: CSS Grid with Webflow's grid utilities
- **Image Optimization**: Multiple srcsets for different screen sizes

## 🏗️ Component Architecture

### Page Sections
1. **Navigation**: Sticky header with mobile hamburger menu
2. **Hero**: Introduction with profile image
3. **About**: Personal background with travel photography
4. **Projects**: Portfolio showcasing technical work
5. **Skills**: Technical capabilities overview
6. **Blog**: Featured articles and writing
7. **Contact**: Contact form and social links
8. **Footer**: Site navigation and social media

### Key Components

#### Navigation System
- **Desktop**: Clean horizontal navigation
- **Mobile**: Hamburger menu with slide-out panel
- **Accessibility**: Proper ARIA labels and keyboard navigation

#### Contact Form
- **Service**: Formspree (https://formspree.io/f/mnqklnog)
- **Validation**: HTML5 validation with custom styling
- **Security**: CSRF protection via Formspree

#### Image Management
- **Optimization**: Multiple resolution versions for responsive images
- **Formats**: PNG for graphics, JPG for photography
- **Loading**: Lazy loading for below-the-fold images

## 🔧 Development Workflow

### Local Development
```bash
# No build process required - static files
# Simply open index.html in browser or use local server
python -m http.server 8000  # Python
# or
npx serve .                 # Node.js
```

### Deployment Pipeline
Automated via **GitHub Actions**:

```yaml
# .github/workflows/static.yml
name: Deploy static content to Pages
on:
  push:
    branches: ["main"]
# Deploys to: https://connorbarrett.dev
```

## 🌐 External Dependencies

### Core Services
- **Formspree**: Contact form processing
  - Endpoint: `https://formspree.io/f/mnqklnog`
  - Features: Spam protection, email notifications
  
- **Google Fonts**: Typography
  - Font: Manrope (weights: 200, 300)
  - Loading: Async with font-display optimization

### CDN Dependencies
- **jQuery**: `3.5.1` (Webflow requirement)
- **WebFont Loader**: Font loading optimization

## ⚡ Performance Considerations

### Optimization Strategy
- **CSS**: Minified production stylesheets
- **Images**: Multiple resolutions with appropriate sizing
- **Fonts**: Preconnected to Google Fonts with async loading
- **JavaScript**: Minimal JS footprint (primarily Webflow utilities)

### Core Web Vitals
- **LCP**: Optimized hero image loading
- **FID**: Minimal JavaScript execution
- **CLS**: Proper image dimensions to prevent layout shift

## 🔐 Security & Privacy

### Implemented Measures
- **External Links**: `rel="noopener"` for security
- **Form Protection**: Formspree spam filtering
- **Content Security**: Static hosting eliminates server vulnerabilities

## 📊 Analytics & Monitoring

Currently no analytics implemented, but recommended additions:
- **Google Analytics 4**: User behavior tracking
- **Core Web Vitals**: Performance monitoring
- **Formspree Analytics**: Contact form conversion tracking

## 🔄 Maintenance

### Regular Tasks
- **Image Optimization**: Compress new images for web
- **Content Updates**: Blog posts and project additions
- **Dependency Updates**: Monitor Webflow and external service changes
- **Performance Audits**: Regular Lighthouse testing

### Known Technical Debt
- Large CSS bundle (85KB) - could be optimized
- Some images could be converted to WebP format
- Consider implementing a build process for further optimization

## 🚀 Future Enhancements

### Planned Improvements
1. **Performance**: WebP image format adoption
2. **Accessibility**: Full WCAG 2.1 AA compliance audit
3. **SEO**: Structured data implementation
4. **Analytics**: Privacy-focused analytics integration
5. **CMS**: Headless CMS for easier content management

### Migration Considerations
For scaling beyond static hosting:
- **Next.js**: For improved performance and SEO
- **Headless CMS**: Sanity or Strapi for content management
- **Image CDN**: Cloudinary for advanced image optimization

---

## 📞 External Service Links

- **Live Site**: [connorbarrett.dev](https://connorbarrett.dev)
- **Webflow Preview**: [Design System](https://preview.webflow.com/preview/connor-freelance-portfolio-23-24?utm_medium=preview_link&utm_source=dashboard&utm_content=connor-freelance-portfolio-23-24&preview=db22b4165967bb4708214909a28d8b30&workflow=preview)
- **Form Management**: [Formspree Dashboard](https://formspree.io/forms/mnqklnog/submissions)
- **Domain Management**: [Google Domains](https://domains.google.com/registrar/connorbarrett.dev)
