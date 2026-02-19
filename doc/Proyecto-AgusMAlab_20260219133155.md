# Reporte de proyecto

## Estructura del proyecto

```
C:\xampp\htdocs\GitHub\Proyecto-AgusMAlab
├── .gitignore
├── README.md
├── agusmalab.css
├── agusmalab.js
└── index.html
```

## Código (intercalado)

# Proyecto-AgusMAlab
**README.md**
```markdown
# AgusmaLab v3.0 Professional

Librería de componentes UI con diseño minimalista y profesional.

## Características

### Diseño
- **Minimalista**: Interfaz limpia y enfocada
- **Tema oscuro profesional**: Colores slate/blue sutiles
- **Glassmorphism**: Efectos de cristal esmerilado discretos
- **Iconos SVG**: Vectores optimizados y escalables
- **Animaciones suaves**: Transiciones fluidas y sutiles

### Componentes
- **StatsCard**: Tarjetas de estadísticas
- **DataTable**: Tablas con búsqueda, ordenamiento y paginación
- **BarChart**: Gráficos de barras

### Sistema de Diseño
- Tipografía escalable modular (ratio 1.25)
- Spacing basado en sistema 8px
- Paleta de colores profesional
- Sombras sutiles en 4 niveles

## Iconos Incluidos

`usuarios` • `dinero` • `pedidos` • `estadisticas` • `tendencia` • `productos` • `ventas` • `objetivo`

## Uso

```javascript
new AgusmaLab.StatsCard('#contenedor', {
  titulo: 'Usuarios Activos',
  valor: '2,847',
  icono: 'usuarios',
  colorIcono: 'primary',
  descripcion: 'Registrados hoy',
  cambio: '+12.5%',
  tipoCambio: 'positivo'
});
```

---

**Versión**: 3.0.0 Professional  
**Fecha**: 17 de febrero de 2026
```
**agusmalab.css**
```css
/*!
 * AgusMALab - Librería de Componentes UI v3.0 (Premium)
 * Con Glassmorphism, Animaciones y Tipografía Mejorada
 * Autor: Agustín Mateo
 * Fecha: 17 de febrero de 2026
 */

/* ========================================
   VARIABLES Y TOKENS DE DISEÑO
   ======================================== */
:root {
  /* Colores principales - Paleta profesional minimalista */
  --agl-primary: #3b82f6;
  --agl-primary-light: #60a5fa;
  --agl-primary-dark: #2563eb;
  --agl-secondary: #64748b;
  --agl-secondary-light: #94a3b8;
  --agl-success: #10b981;
  --agl-success-light: #34d399;
  --agl-warning: #f59e0b;
  --agl-warning-light: #fbbf24;
  --agl-danger: #ef4444;
  --agl-danger-light: #f87171;
  --agl-info: #06b6d4;
  --agl-info-light: #22d3ee;
  
  /* Colores de fondo y texto - Tema oscuro profesional */
  --agl-bg: rgba(30, 41, 59, 0.7);
  --agl-bg-solid: #1e293b;
  --agl-bg-alt: rgba(15, 23, 42, 0.5);
  --agl-text: #f1f5f9;
  --agl-text-muted: #94a3b8;
  --agl-text-light: #cbd5e1;
  --agl-border: rgba(148, 163, 184, 0.15);
  
  /* Glassmorphism - Más sutil */
  --agl-glass-bg: rgba(30, 41, 59, 0.6);
  --agl-glass-border: rgba(148, 163, 184, 0.1);
  --agl-glass-shadow: 0 4px 24px rgba(0, 0, 0, 0.2);
  --agl-backdrop-blur: blur(20px);
  
  /* Nuevos colores para indicadores */
  --agl-positive: #10b981;
  --agl-negative: #ef4444;
  --agl-neutral: #64748b;
  
  /* Espaciado - Escala mejorada (base 4px) */
  --agl-space-xs: 0.5rem;     /* 8px */
  --agl-space-sm: 0.75rem;    /* 12px */
  --agl-space-md: 1rem;       /* 16px */
  --agl-space-lg: 1.5rem;     /* 24px */
  --agl-space-xl: 2rem;       /* 32px */
  --agl-space-2xl: 3rem;      /* 48px */
  --agl-space-3xl: 4rem;      /* 64px */
  
  /* Bordes y sombras mejoradas - Minimalistas */
  --agl-radius: 0.75rem;      /* 12px */
  --agl-radius-sm: 0.5rem;    /* 8px */
  --agl-radius-lg: 1rem;      /* 16px */
  --agl-radius-xl: 1.5rem;    /* 24px */
  --agl-shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.12);
  --agl-shadow-md: 0 2px 8px rgba(0, 0, 0, 0.15);
  --agl-shadow-lg: 0 4px 16px rgba(0, 0, 0, 0.2);
  --agl-shadow-xl: 0 8px 24px rgba(0, 0, 0, 0.25);
  
  /* Tipografía - Escala modular (1.25 ratio) */
  --agl-font: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  --agl-font-size-xs: 0.75rem;    /* 12px */
  --agl-font-size-sm: 0.875rem;   /* 14px */
  --agl-font-size: 1rem;          /* 16px - base */
  --agl-font-size-lg: 1.125rem;   /* 18px */
  --agl-font-size-xl: 1.25rem;    /* 20px */
  --agl-font-size-2xl: 1.5rem;    /* 24px */
  --agl-font-size-3xl: 1.875rem;  /* 30px */
  --agl-font-size-4xl: 2.25rem;   /* 36px */
  
  /* Pesos de fuente */
  --agl-font-normal: 400;
  --agl-font-medium: 500;
  --agl-font-semibold: 600;
  --agl-font-bold: 700;
  --agl-font-extrabold: 800;
  
  /* Line heights */
  --agl-leading-tight: 1.25;
  --agl-leading-snug: 1.375;
  --agl-leading-normal: 1.5;
  --agl-leading-relaxed: 1.75;
  --agl-leading-loose: 2;
  
  /* Transiciones mejoradas */
  --agl-transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  --agl-transition-fast: all 0.15s cubic-bezier(0.4, 0, 0.2, 1);
  --agl-transition-slow: all 0.45s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Modo oscuro */
@media (prefers-color-scheme: dark) {
  :root {
    --agl-bg: #1e293b;
    --agl-bg-alt: #0f172a;
    --agl-text: #f1f5f9;
    --agl-text-muted: #94a3b8;
    --agl-border: #334155;
  }
}

/* ========================================
   KEYFRAMES Y ANIMACIONES
   ======================================== */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scale(0.95);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes pulseValue {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
}

@keyframes shimmer {
  0% {
    background-position: -1000px 0;
  }
  100% {
    background-position: 1000px 0;
  }
}

/* ========================================
   RESET Y BASE
   ======================================== */
.agl-container,
.agl-container * {
  box-sizing: border-box;
}

.agl-container {
  font-family: var(--agl-font);
  font-size: var(--agl-font-size);
  color: var(--agl-text);
  line-height: var(--agl-leading-normal);
}

/* Animación de entrada automática */
.agl-animate-in {
  animation: fadeInUp 0.6s cubic-bezier(0.4, 0, 0.2, 1) both;
}

/* Delays escalonados para múltiples elementos */
.agl-animate-in:nth-child(1) { animation-delay: 0.1s; }
.agl-animate-in:nth-child(2) { animation-delay: 0.2s; }
.agl-animate-in:nth-child(3) { animation-delay: 0.3s; }
.agl-animate-in:nth-child(4) { animation-delay: 0.4s; }
.agl-animate-in:nth-child(5) { animation-delay: 0.5s; }
.agl-animate-in:nth-child(6) { animation-delay: 0.6s; }

/* ========================================
   COMPONENTE: StatsCard (Premium Glassmorphism)
   ======================================== */
.agl-stats-card {
  background: var(--agl-glass-bg);
  backdrop-filter: var(--agl-backdrop-blur);
  -webkit-backdrop-filter: var(--agl-backdrop-blur);
  border: 1px solid var(--agl-glass-border);
  border-radius: var(--agl-radius);
  padding: var(--agl-space-xl);
  box-shadow: var(--agl-glass-shadow);
  transition: var(--agl-transition);
  position: relative;
  overflow: hidden;
}

.agl-stats-card:hover {
  box-shadow: var(--agl-shadow-lg);
  transform: translateY(-2px);
  border-color: rgba(148, 163, 184, 0.2);
}

.agl-stats-card-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: var(--agl-space-lg);
}

.agl-stats-card-title {
  font-size: var(--agl-font-size-sm);
  color: var(--agl-text-muted);
  font-weight: var(--agl-font-semibold);
  text-transform: uppercase;
  letter-spacing: 0.075em;
  line-height: var(--agl-leading-tight);
}

.agl-stats-card-icon {
  width: 3rem;
  height: 3rem;
  border-radius: var(--agl-radius);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: var(--agl-transition-fast);
  box-shadow: none;
}

.agl-stats-card-icon svg {
  width: 1.5rem;
  height: 1.5rem;
}

.agl-stats-card:hover .agl-stats-card-icon {
  transform: scale(1.05);
}

.agl-stats-card-icon.primary { background: rgba(59, 130, 246, 0.15); color: var(--agl-primary-light); }
.agl-stats-card-icon.success { background: rgba(16, 185, 129, 0.15); color: var(--agl-success-light); }
.agl-stats-card-icon.warning { background: rgba(245, 158, 11, 0.15); color: var(--agl-warning-light); }
.agl-stats-card-icon.danger { background: rgba(239, 68, 68, 0.15); color: var(--agl-danger-light); }
.agl-stats-card-icon.info { background: rgba(6, 182, 212, 0.15); color: var(--agl-info-light); }

.agl-stats-card-value {
  font-size: var(--agl-font-size-4xl);
  font-weight: var(--agl-font-bold);
  color: var(--agl-text);
  margin-bottom: var(--agl-space-sm);
  line-height: var(--agl-leading-tight);
  transition: var(--agl-transition);
  letter-spacing: -0.025em;
}

.agl-stats-card-value.animating {
  animation: pulseValue 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.agl-stats-card-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: var(--agl-font-size-sm);
}

.agl-stats-card-description {
  color: var(--agl-text-muted);
  font-size: var(--agl-font-size-sm);
  line-height: var(--agl-leading-relaxed);
}

.agl-stats-card-change {
  font-weight: var(--agl-font-semibold);
  padding: 0.375rem 0.625rem;
  border-radius: var(--agl-radius-sm);
  font-size: var(--agl-font-size-xs);
  letter-spacing: 0.025em;
  transition: var(--agl-transition-fast);
}

.agl-stats-card-change.positive {
  color: var(--agl-positive);
  background: rgba(16, 185, 129, 0.1);
}

.agl-stats-card-change.negative {
  color: var(--agl-negative);
  background: rgba(239, 68, 68, 0.1);
}

.agl-stats-card-change.neutral {
  color: var(--agl-neutral);
  background: rgba(100, 116, 139, 0.1);
}

/* ========================================
   COMPONENTE: DataTable (Premium Glassmorphism)
   ======================================== */
.agl-table-wrapper {
  background: var(--agl-glass-bg);
  backdrop-filter: var(--agl-backdrop-blur);
  -webkit-backdrop-filter: var(--agl-backdrop-blur);
  border: 1px solid var(--agl-glass-border);
  border-radius: var(--agl-radius);
  overflow: hidden;
  box-shadow: var(--agl-glass-shadow);
  transition: var(--agl-transition);
}

.agl-table-wrapper:hover {
  box-shadow: var(--agl-shadow-lg);
}

.agl-table-header {
  padding: var(--agl-space-xl);
  border-bottom: 1px solid var(--agl-border);
  background: var(--agl-bg-alt);
  backdrop-filter: var(--agl-backdrop-blur);
  -webkit-backdrop-filter: var(--agl-backdrop-blur);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: var(--agl-space-lg);
  flex-wrap: wrap;
}

.agl-table-title {
  font-size: var(--agl-font-size-xl);
  font-weight: var(--agl-font-bold);
  color: var(--agl-text);
  margin: 0;
  line-height: var(--agl-leading-tight);
  letter-spacing: -0.025em;
}

.agl-table-search {
  padding: 0.625rem 1.125rem;
  border: 1.5px solid var(--agl-border);
  border-radius: var(--agl-radius);
  font-size: var(--agl-font-size-sm);
  font-weight: var(--agl-font-medium);
  background: var(--agl-bg-solid);
  color: var(--agl-text);
  min-width: 280px;
  transition: var(--agl-transition);
  line-height: var(--agl-leading-normal);
}

.agl-table-search::placeholder {
  color: var(--agl-text-light);
}

.agl-table-search:focus {
  outline: none;
  border-color: var(--agl-primary);
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
}

.agl-table {
  width: 100%;
  border-collapse: collapse;
}

.agl-table thead {
  background: var(--agl-bg-alt);
}

.agl-table th {
  padding: var(--agl-space-lg) var(--agl-space-md);
  text-align: left;
  font-weight: var(--agl-font-bold);
  font-size: var(--agl-font-size-sm);
  color: var(--agl-text);
  border-bottom: 2px solid var(--agl-border);
  white-space: nowrap;
  letter-spacing: 0.025em;
  text-transform: uppercase;
  line-height: var(--agl-leading-tight);
}

.agl-table th.sortable {
  cursor: pointer;
  user-select: none;
  transition: var(--agl-transition-fast);
}

.agl-table th.sortable:hover {
  background: var(--agl-border);
}

.agl-table th.sortable::after {
  content: ' ⇅';
  opacity: 0.3;
  font-size: 0.875em;
}

.agl-table th.sorted-asc::after {
  content: ' ↑';
  opacity: 1;
  color: var(--agl-primary);
}

.agl-table th.sorted-desc::after {
  content: ' ↓';
  opacity: 1;
  color: var(--agl-primary);
}

.agl-table td {
  padding: var(--agl-space-md);
  border-bottom: 1px solid var(--agl-border);
  color: var(--agl-text);
}

.agl-table tbody tr {
  transition: var(--agl-transition-fast);
}

.agl-table tbody tr:hover {
  background: var(--agl-bg-alt);
}

.agl-table tbody tr:last-child td {
  border-bottom: none;
}

/* Filas zebra */
.agl-table tbody tr:nth-child(even) {
  background: rgba(0, 0, 0, 0.02);
}

.agl-table tbody tr:nth-child(even):hover {
  background: var(--agl-bg-alt);
}

/* Footer con paginación */
.agl-table-footer {
  padding: var(--agl-space-md) var(--agl-space-lg);
  border-top: 1px solid var(--agl-border);
  background: var(--agl-bg-alt);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: var(--agl-space-md);
  flex-wrap: wrap;
}

.agl-table-info {
  font-size: var(--agl-font-size-sm);
  color: var(--agl-text-muted);
}

.agl-table-pagination {
  display: flex;
  gap: var(--agl-space-sm);
}

.agl-table-pagination button {
  padding: 0.5rem 0.75rem;
  border: 1px solid var(--agl-border);
  background: var(--agl-bg);
  color: var(--agl-text);
  border-radius: var(--agl-radius-sm);
  font-size: var(--agl-font-size-sm);
  cursor: pointer;
  transition: var(--agl-transition-fast);
}

.agl-table-pagination button:hover:not(:disabled) {
  background: var(--agl-primary);
  color: white;
  border-color: var(--agl-primary);
}

.agl-table-pagination button.active {
  background: var(--agl-primary);
  color: white;
  border-color: var(--agl-primary);
  font-weight: 600;
}

.agl-table-pagination button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

/* ========================================
   COMPONENTE: BarChart
   ======================================== */
.agl-chart-wrapper {
  background: var(--agl-bg);
  border: 1px solid var(--agl-border);
  border-radius: var(--agl-radius);
  padding: var(--agl-space-lg);
  box-shadow: var(--agl-shadow-sm);
}

.agl-chart-title {
  font-size: var(--agl-font-size-lg);
  font-weight: 600;
  color: var(--agl-text);
  margin: 0 0 var(--agl-space-lg) 0;
  text-align: center;
}

.agl-chart-canvas {
  display: block;
  max-width: 100%;
  height: auto;
}

/* ========================================
   UTILIDADES
   ======================================== */
.agl-grid {
  display: grid;
  gap: var(--agl-space-lg);
}

.agl-grid-2 {
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
}

.agl-grid-3 {
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}

.agl-grid-4 {
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
}

/* ========================================
   RESPONSIVE
   ======================================== */
@media (max-width: 768px) {
  .agl-stats-card {
    padding: var(--agl-space-md);
  }
  
  .agl-stats-card-value {
    font-size: 1.5rem;
  }
  
  .agl-table {
    font-size: var(--agl-font-size-sm);
  }
  
  .agl-table th,
  .agl-table td {
    padding: var(--agl-space-sm);
  }
  
  .agl-table-search {
    min-width: 100%;
  }
  
  .agl-table-header {
    flex-direction: column;
    align-items: stretch;
  }
  
  .agl-table-footer {
    flex-direction: column;
    align-items: stretch;
  }
  
  .agl-table-pagination {
    justify-content: center;
  }
}


```
**agusmalab.js**
```js
/*!
 * AgusmaLab - Librería de Componentes UI v3.0 (Premium)
 * Con Glassmorphism, Iconos SVG, Animaciones y Tipografía Mejorada
 * Búsqueda, Ordenamiento, Paginación y Gráficos
 * Autor: Agust�n Mateo
 * Fecha: 17 de febrero de 2026
 */

(function (root, factory) {
  if (typeof define === 'function' && define.amd) {
    define([], factory);
  } else if (typeof module === 'object' && module.exports) {
    module.exports = factory();
  } else {
    root.AgusmaLab = factory();
  }
}(typeof self !== 'undefined' ? self : this, function () {
  'use strict';

  /* ========================================
     UTILIDADES
     ======================================== */
  
  const crearElemento = (tag, className = '', content = '') => {
    const elemento = document.createElement(tag);
    if (className) elemento.className = className;
    if (content) elemento.textContent = content;
    return elemento;
  };

  const obtenerElemento = (selector) => {
    return typeof selector === 'string' ? document.querySelector(selector) : selector;
  };

  const normalizar = (str) => {
    return str.normalize('NFD')
      .replace(/[\u0300-\u036f]/g, '')
      .toLowerCase();
  };

  /* ========================================
     ICONOS SVG PROFESIONALES
     ======================================== */
  const Iconos = {
    usuarios: `
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path>
        <circle cx="9" cy="7" r="4"></circle>
        <path d="M23 21v-2a4 4 0 0 0-3-3.87"></path>
        <path d="M16 3.13a4 4 0 0 1 0 7.75"></path>
      </svg>
    `,
    dinero: `
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <line x1="12" y1="1" x2="12" y2="23"></line>
        <path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"></path>
      </svg>
    `,
    pedidos: `
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
        <polyline points="14 2 14 8 20 8"></polyline>
        <line x1="16" y1="13" x2="8" y2="13"></line>
        <line x1="16" y1="17" x2="8" y2="17"></line>
        <polyline points="10 9 9 9 8 9"></polyline>
      </svg>
    `,
    estadisticas: `
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <line x1="18" y1="20" x2="18" y2="10"></line>
        <line x1="12" y1="20" x2="12" y2="4"></line>
        <line x1="6" y1="20" x2="6" y2="14"></line>
      </svg>
    `,
    tendencia: `
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="23 6 13.5 15.5 8.5 10.5 1 18"></polyline>
        <polyline points="17 6 23 6 23 12"></polyline>
      </svg>
    `,
    productos: `
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path>
        <polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline>
        <line x1="12" y1="22.08" x2="12" y2="12"></line>
      </svg>
    `,
    ventas: `
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <circle cx="9" cy="21" r="1"></circle>
        <circle cx="20" cy="21" r="1"></circle>
        <path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"></path>
      </svg>
    `,
    objetivo: `
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <circle cx="12" cy="12" r="10"></circle>
        <circle cx="12" cy="12" r="6"></circle>
        <circle cx="12" cy="12" r="2"></circle>
      </svg>
    `
  };

  const obtenerIconoSVG = (nombreIcono) => {
    return Iconos[nombreIcono] || Iconos.estadisticas;
  };

  /* ========================================
     COMPONENTE: StatsCard (Premium con SVG)
     ======================================== */
  class StatsCard {
    constructor(contenedor, opciones = {}) {
      this.contenedor = obtenerElemento(contenedor);
      
      if (!this.contenedor) {
        throw new Error('AgusmaLab.StatsCard: contenedor no encontrado');
      }

      this.opciones = {
        titulo: opciones.titulo || 'Estadística',
        valor: opciones.valor || '0',
        icono: opciones.icono || 'estadisticas',
        colorIcono: opciones.colorIcono || 'primary',
        descripcion: opciones.descripcion || '',
        cambio: opciones.cambio || null,
        tipoCambio: opciones.tipoCambio || 'neutral',
        ...opciones
      };

      this.renderizar();
    }

    renderizar() {
      this.contenedor.innerHTML = '';
      this.contenedor.className = 'agl-container agl-animate-in';

      const tarjeta = crearElemento('div', 'agl-stats-card');

      // Header
      const header = crearElemento('div', 'agl-stats-card-header');
      const titulo = crearElemento('div', 'agl-stats-card-title', this.opciones.titulo);
      
      // Icono SVG
      const icono = document.createElement('div');
      icono.className = `agl-stats-card-icon ${this.opciones.colorIcono}`;
      icono.innerHTML = obtenerIconoSVG(this.opciones.icono);
      
      header.appendChild(titulo);
      header.appendChild(icono);
      tarjeta.appendChild(header);

      // Valor
      const valor = crearElemento('div', 'agl-stats-card-value', this.opciones.valor);
      tarjeta.appendChild(valor);

      // Footer
      if (this.opciones.descripcion || this.opciones.cambio) {
        const footer = crearElemento('div', 'agl-stats-card-footer');
        
        if (this.opciones.descripcion) {
          const desc = crearElemento('div', 'agl-stats-card-description', this.opciones.descripcion);
          footer.appendChild(desc);
        }
        
        if (this.opciones.cambio) {
          const cambio = crearElemento('div', `agl-stats-card-change ${this.opciones.tipoCambio}`, this.opciones.cambio);
          footer.appendChild(cambio);
        }
        
        tarjeta.appendChild(footer);
      }

      this.contenedor.appendChild(tarjeta);
      
      // Guardar referencias
      this.elementoValor = valor;
      this.elementoCambio = this.contenedor.querySelector('.agl-stats-card-change');
    }

    actualizarValor(nuevoValor, animar = true) {
      this.opciones.valor = nuevoValor;
      if (this.elementoValor) {
        if (animar) {
          this.elementoValor.classList.add('animating');
          setTimeout(() => this.elementoValor.classList.remove('animating'), 400);
        }
        this.elementoValor.textContent = nuevoValor;
      }
    }

    mostrarCambio(cambio, tipo = 'neutral') {
      this.opciones.cambio = cambio;
      this.opciones.tipoCambio = tipo;
      
      if (this.elementoCambio) {
        this.elementoCambio.textContent = cambio;
        this.elementoCambio.className = `agl-stats-card-change ${tipo}`;
      } else {
        this.renderizar();
      }
    }
  }

  /* ========================================
     COMPONENTE: DataTable (Mejorada)
     ======================================== */
  class DataTable {
    constructor(contenedor, opciones = {}) {
      this.contenedor = obtenerElemento(contenedor);
      
      if (!this.contenedor) {
        throw new Error('AgusmaLab.DataTable: contenedor no encontrado');
      }

      this.opciones = {
        titulo: opciones.titulo || 'Tabla de Datos',
        columnas: opciones.columnas || [],
        datos: opciones.datos || [],
        busqueda: opciones.busqueda !== false,
        ordenamiento: opciones.ordenamiento !== false,
        paginacion: opciones.paginacion !== false,
        filasPorPagina: opciones.filasPorPagina || 10,
        ...opciones
      };

      this.paginaActual = 1;
      this.columnaOrden = null;
      this.direccionOrden = 'asc';
      this.terminoBusqueda = '';
      this.datosFiltrados = [...this.opciones.datos];

      this.renderizar();
    }

    renderizar() {
      this.contenedor.innerHTML = '';
      this.contenedor.className = 'agl-container';

      const wrapper = crearElemento('div', 'agl-table-wrapper');

      // Header con título y búsqueda
      const header = crearElemento('div', 'agl-table-header');
      const titulo = crearElemento('h3', 'agl-table-title', this.opciones.titulo);
      header.appendChild(titulo);

      if (this.opciones.busqueda) {
        this.inputBusqueda = crearElemento('input', 'agl-table-search');
        this.inputBusqueda.type = 'search';
        this.inputBusqueda.placeholder = 'Buscar...';
        this.inputBusqueda.value = this.terminoBusqueda;
        header.appendChild(this.inputBusqueda);
      }

      wrapper.appendChild(header);

      // Tabla
      const tabla = crearElemento('table', 'agl-table');
      
      // Thead
      const thead = document.createElement('thead');
      const filaHeader = document.createElement('tr');
      
      this.opciones.columnas.forEach((col, index) => {
        const campo = col.campo || col;
        const etiqueta = col.etiqueta || col;
        const ordenable = col.ordenable !== false && this.opciones.ordenamiento;
        
        const th = crearElemento('th', '', etiqueta);
        
        if (ordenable) {
          th.classList.add('sortable');
          th.dataset.campo = campo;
          
          if (this.columnaOrden === campo) {
            th.classList.add(this.direccionOrden === 'asc' ? 'sorted-asc' : 'sorted-desc');
          }
        }
        
        filaHeader.appendChild(th);
      });
      
      thead.appendChild(filaHeader);
      tabla.appendChild(thead);

      // Tbody
      const tbody = document.createElement('tbody');
      const datosPaginados = this._obtenerDatosPaginados();
      
      if (datosPaginados.length === 0) {
        const filaVacia = document.createElement('tr');
        const celdaVacia = crearElemento('td', '', 'No hay datos para mostrar');
        celdaVacia.colSpan = this.opciones.columnas.length;
        celdaVacia.style.textAlign = 'center';
        celdaVacia.style.padding = '2rem';
        celdaVacia.style.color = 'var(--agl-text-muted)';
        filaVacia.appendChild(celdaVacia);
        tbody.appendChild(filaVacia);
      } else {
        datosPaginados.forEach(fila => {
          const tr = document.createElement('tr');
          
          this.opciones.columnas.forEach(col => {
            const campo = col.campo || col;
            const td = crearElemento('td');
            
            // Si la fila es un array, usar índice
            const valor = Array.isArray(fila) ? 
              fila[this.opciones.columnas.indexOf(col)] : 
              fila[campo];
            
            td.textContent = valor !== null && valor !== undefined ? valor : '';
            tr.appendChild(td);
          });
          
          tbody.appendChild(tr);
        });
      }
      
      tabla.appendChild(tbody);
      wrapper.appendChild(tabla);

      // Footer con paginación
      if (this.opciones.paginacion) {
        this._renderizarPaginacion(wrapper);
      }

      this.contenedor.appendChild(wrapper);
      
      // Guardar referencias para actualizaciones parciales
      this.wrapper = wrapper;
      this.tabla = tabla;
      
      this._adjuntarEventos();
    }

    _actualizarContenido() {
      // Actualizar solo tbody y footer sin tocar el header
      if (!this.tabla) return;
      
      // Actualizar tbody
      const tbody = this.tabla.querySelector('tbody');
      if (tbody) {
        tbody.innerHTML = '';
        const datosPaginados = this._obtenerDatosPaginados();
        
        if (datosPaginados.length === 0) {
          const filaVacia = document.createElement('tr');
          const celdaVacia = crearElemento('td', '', 'No hay datos para mostrar');
          celdaVacia.colSpan = this.opciones.columnas.length;
          celdaVacia.style.textAlign = 'center';
          celdaVacia.style.padding = '2rem';
          celdaVacia.style.color = 'var(--agl-text-muted)';
          filaVacia.appendChild(celdaVacia);
          tbody.appendChild(filaVacia);
        } else {
          datosPaginados.forEach(fila => {
            const tr = document.createElement('tr');
            
            this.opciones.columnas.forEach(col => {
              const campo = col.campo || col;
              const td = crearElemento('td');
              
              const valor = Array.isArray(fila) ? 
                fila[this.opciones.columnas.indexOf(col)] : 
                fila[campo];
              
              td.textContent = valor !== null && valor !== undefined ? valor : '';
              tr.appendChild(td);
            });
            
            tbody.appendChild(tr);
          });
        }
      }
      
      // Actualizar thead (para indicadores de ordenamiento)
      const headers = this.tabla.querySelectorAll('th.sortable');
      headers.forEach(th => {
        th.classList.remove('sorted-asc', 'sorted-desc');
        const campo = th.dataset.campo;
        if (this.columnaOrden === campo) {
          th.classList.add(this.direccionOrden === 'asc' ? 'sorted-asc' : 'sorted-desc');
        }
      });
      
      // Actualizar footer de paginación
      if (this.opciones.paginacion) {
        const footerAntiguo = this.wrapper.querySelector('.agl-table-footer');
        if (footerAntiguo) {
          footerAntiguo.remove();
        }
        this._renderizarPaginacion(this.wrapper);
        this._adjuntarEventosPaginacion();
      }
    }

    _renderizarPaginacion(wrapper) {
      const footer = crearElemento('div', 'agl-table-footer');
      
      // Info
      const totalFilas = this.datosFiltrados.length;
      const inicio = (this.paginaActual - 1) * this.opciones.filasPorPagina + 1;
      const fin = Math.min(this.paginaActual * this.opciones.filasPorPagina, totalFilas);
      const info = crearElemento('div', 'agl-table-info', 
        `Mostrando ${inicio}-${fin} de ${totalFilas} registros`);
      footer.appendChild(info);

      // Paginación
      const paginacion = crearElemento('div', 'agl-table-pagination');
      const totalPaginas = Math.ceil(totalFilas / this.opciones.filasPorPagina);

      // Botón anterior
      const btnAnterior = crearElemento('button', '', '← Anterior');
      btnAnterior.disabled = this.paginaActual === 1;
      paginacion.appendChild(btnAnterior);

      // Números de página
      const maxPaginasVisibles = 5;
      let paginaInicio = Math.max(1, this.paginaActual - Math.floor(maxPaginasVisibles / 2));
      let paginaFin = Math.min(totalPaginas, paginaInicio + maxPaginasVisibles - 1);
      
      if (paginaFin - paginaInicio < maxPaginasVisibles - 1) {
        paginaInicio = Math.max(1, paginaFin - maxPaginasVisibles + 1);
      }

      for (let i = paginaInicio; i <= paginaFin; i++) {
        const btnPagina = crearElemento('button', '', i.toString());
        if (i === this.paginaActual) {
          btnPagina.classList.add('active');
        }
        btnPagina.dataset.pagina = i;
        paginacion.appendChild(btnPagina);
      }

      // Botón siguiente
      const btnSiguiente = crearElemento('button', '', 'Siguiente →');
      btnSiguiente.disabled = this.paginaActual === totalPaginas || totalPaginas === 0;
      paginacion.appendChild(btnSiguiente);

      footer.appendChild(paginacion);
      wrapper.appendChild(footer);
    }

    _adjuntarEventos() {
      // Búsqueda
      if (this.inputBusqueda) {
        this.inputBusqueda.addEventListener('input', (e) => {
          this.terminoBusqueda = e.target.value;
          this._filtrarDatos();
          this.paginaActual = 1;
          this._actualizarContenido();
        });
      }

      // Ordenamiento
      const headers = this.contenedor.querySelectorAll('th.sortable');
      headers.forEach(th => {
        th.addEventListener('click', () => {
          const campo = th.dataset.campo;
          if (this.columnaOrden === campo) {
            this.direccionOrden = this.direccionOrden === 'asc' ? 'desc' : 'asc';
          } else {
            this.columnaOrden = campo;
            this.direccionOrden = 'asc';
          }
          this._ordenarDatos();
          this._actualizarContenido();
        });
      });

      this._adjuntarEventosPaginacion();
    }

    _adjuntarEventosPaginacion() {
      // Paginación
      const btnAnterior = this.contenedor.querySelector('.agl-table-pagination button:first-child');
      const btnSiguiente = this.contenedor.querySelector('.agl-table-pagination button:last-child');
      const btnsPagina = this.contenedor.querySelectorAll('.agl-table-pagination button[data-pagina]');

      if (btnAnterior) {
        btnAnterior.addEventListener('click', () => this.paginaAnterior());
      }

      if (btnSiguiente) {
        btnSiguiente.addEventListener('click', () => this.paginaSiguiente());
      }

      btnsPagina.forEach(btn => {
        btn.addEventListener('click', () => {
          this.irAPagina(parseInt(btn.dataset.pagina));
        });
      });
    }

    _filtrarDatos() {
      if (!this.terminoBusqueda) {
        this.datosFiltrados = [...this.opciones.datos];
        return;
      }

      const termino = normalizar(this.terminoBusqueda);
      this.datosFiltrados = this.opciones.datos.filter(fila => {
        return this.opciones.columnas.some((col, index) => {
          const valor = Array.isArray(fila) ? fila[index] : fila[col.campo || col];
          if (valor === null || valor === undefined) return false;
          return normalizar(String(valor)).includes(termino);
        });
      });
    }

    _ordenarDatos() {
      if (!this.columnaOrden) return;

      const indiceColumna = this.opciones.columnas.findIndex(col => 
        (col.campo || col) === this.columnaOrden
      );

      this.datosFiltrados.sort((a, b) => {
        const valorA = Array.isArray(a) ? a[indiceColumna] : a[this.columnaOrden];
        const valorB = Array.isArray(b) ? b[indiceColumna] : b[this.columnaOrden];
        
        if (valorA === null || valorA === undefined) return 1;
        if (valorB === null || valorB === undefined) return -1;
        
        let comparacion = 0;
        if (typeof valorA === 'number' && typeof valorB === 'number') {
          comparacion = valorA - valorB;
        } else {
          comparacion = String(valorA).localeCompare(String(valorB));
        }
        
        return this.direccionOrden === 'asc' ? comparacion : -comparacion;
      });
    }

    _obtenerDatosPaginados() {
      if (!this.opciones.paginacion) {
        return this.datosFiltrados;
      }

      const inicio = (this.paginaActual - 1) * this.opciones.filasPorPagina;
      const fin = inicio + this.opciones.filasPorPagina;
      return this.datosFiltrados.slice(inicio, fin);
    }

    paginaSiguiente() {
      const totalPaginas = Math.ceil(this.datosFiltrados.length / this.opciones.filasPorPagina);
      if (this.paginaActual < totalPaginas) {
        this.paginaActual++;
        this._actualizarContenido();
      }
    }

    paginaAnterior() {
      if (this.paginaActual > 1) {
        this.paginaActual--;
        this._actualizarContenido();
      }
    }

    irAPagina(pagina) {
      const totalPaginas = Math.ceil(this.datosFiltrados.length / this.opciones.filasPorPagina);
      if (pagina >= 1 && pagina <= totalPaginas) {
        this.paginaActual = pagina;
        this._actualizarContenido();
      }
    }

    actualizarDatos(nuevosDatos) {
      this.opciones.datos = nuevosDatos;
      this.datosFiltrados = [...nuevosDatos];
      this.paginaActual = 1;
      this.renderizar();
    }
  }

  /* ========================================
     COMPONENTE: BarChart
     ======================================== */
  class BarChart {
    constructor(contenedor, opciones = {}) {
      this.contenedor = obtenerElemento(contenedor);
      
      if (!this.contenedor) {
        throw new Error('AgusmaLab.BarChart: contenedor no encontrado');
      }

      this.opciones = {
        titulo: opciones.titulo || 'Gráfico de Barras',
        etiquetas: opciones.etiquetas || [],
        datos: opciones.datos || [],
        color: opciones.color || '#3b82f6',
        ancho: opciones.ancho || 600,
        alto: opciones.alto || 300,
        ...opciones
      };

      this.renderizar();
    }

    renderizar() {
      this.contenedor.innerHTML = '';
      this.contenedor.className = 'agl-container';

      const wrapper = crearElemento('div', 'agl-chart-wrapper');

      // Título
      if (this.opciones.titulo) {
        const titulo = crearElemento('h3', 'agl-chart-title', this.opciones.titulo);
        wrapper.appendChild(titulo);
      }

      // Canvas
      const canvas = document.createElement('canvas');
      canvas.className = 'agl-chart-canvas';
      canvas.width = this.opciones.ancho;
      canvas.height = this.opciones.alto;
      wrapper.appendChild(canvas);

      this.contenedor.appendChild(wrapper);

      // Dibujar gráfico
      this._dibujarGrafico(canvas);
    }

    _dibujarGrafico(canvas) {
      const ctx = canvas.getContext('2d');
      const padding = 50;
      const ancho = canvas.width - padding * 2;
      const alto = canvas.height - padding * 2;

      // Limpiar canvas
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Configurar fuente
      ctx.font = '12px -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif';

      // Encontrar valor máximo
      const valorMax = Math.max(...this.opciones.datos);
      const escalaY = alto / valorMax;

      // Calcular ancho de barras
      const numBarras = this.opciones.datos.length;
      const anchoBarra = (ancho / numBarras) * 0.7;
      const espacioBarra = (ancho / numBarras) * 0.3;

      // Dibujar barras
      this.opciones.datos.forEach((valor, i) => {
        const x = padding + (i * (anchoBarra + espacioBarra)) + espacioBarra / 2;
        const alturaBarra = valor * escalaY;
        const y = canvas.height - padding - alturaBarra;

        // Barra
        ctx.fillStyle = this.opciones.color;
        ctx.fillRect(x, y, anchoBarra, alturaBarra);

        // Valor encima de la barra
        ctx.fillStyle = '#cbd5e1';
        ctx.textAlign = 'center';
        ctx.fillText(valor, x + anchoBarra / 2, y - 5);

        // Etiqueta debajo
        if (this.opciones.etiquetas[i]) {
          ctx.fillText(this.opciones.etiquetas[i], x + anchoBarra / 2, canvas.height - padding + 20);
        }
      });

      // Eje Y (línea)
      ctx.strokeStyle = '#e2e8f0';
      ctx.lineWidth = 1;
      ctx.beginPath();
      ctx.moveTo(padding, padding);
      ctx.lineTo(padding, canvas.height - padding);
      ctx.lineTo(canvas.width - padding, canvas.height - padding);
      ctx.stroke();
    }

    actualizarDatos(nuevosDatos, nuevasEtiquetas = null) {
      this.opciones.datos = nuevosDatos;
      if (nuevasEtiquetas) {
        this.opciones.etiquetas = nuevasEtiquetas;
      }
      this.renderizar();
    }
  }

  /* ========================================
     EXPORTAR LIBRERÍA
     ======================================== */
  return {
    StatsCard: StatsCard,
    DataTable: DataTable,
    BarChart: BarChart,
    Iconos: Iconos,
    version: '3.0.0'
  };
}));


```
**index.html**
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AgusmaLab v3.0 Premium - Demo</title>
  <link rel="icon" type="image/png" href="https://static.agusmadev.es/logos/logo-azul-degradado-invertido.png">
  
  <!-- Cargar nuestra librería -->
  <link rel="stylesheet" href="agusmalab.css">
  
  <style>
    body {
      margin: 0;
      padding: 2rem;
      background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #334155 100%);
      background-attachment: fixed;
      min-height: 100vh;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      position: relative;
      overflow-x: hidden;
    }
    
    /* Textura sutil de fondo */
    body::before {
      content: '';
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        radial-gradient(at 20% 30%, rgba(59, 130, 246, 0.08) 0px, transparent 50%),
        radial-gradient(at 80% 70%, rgba(16, 185, 129, 0.06) 0px, transparent 50%);
      pointer-events: none;
    }
    
    .demo-container {
      max-width: 1400px;
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }
    
    .demo-header {
      text-align: center;
      color: white;
      margin-bottom: 3rem;
      animation: fadeInDown 0.8s cubic-bezier(0.4, 0, 0.2, 1);
    }
    
    @keyframes fadeInDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    .demo-header h1 {
      font-size: 2.75rem;
      margin-bottom: 0.5rem;
      text-shadow: none;
      font-weight: 700;
      color: #f8fafc;
      letter-spacing: -0.03em;
    }
    
    .demo-header p {
      font-size: 1.125rem;
      opacity: 0.7;
      margin-top: 0.75rem;
      font-weight: 400;
      color: #cbd5e1;
      letter-spacing: 0;
    }
    
    .demo-section {
      margin-bottom: 4rem;
      animation: fadeInUp 0.8s cubic-bezier(0.4, 0, 0.2, 1) both;
    }
    
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    .demo-section:nth-child(2) { animation-delay: 0.1s; }
    .demo-section:nth-child(3) { animation-delay: 0.2s; }
    .demo-section:nth-child(4) { animation-delay: 0.3s; }
    
    .section-title {
      color: #e2e8f0;
      font-size: 1.5rem;
      margin-bottom: 1.5rem;
      font-weight: 600;
      letter-spacing: -0.01em;
    }
    
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.75rem;
      margin-bottom: 2rem;
    }
    
    .demo-controls {
      background: rgba(30, 41, 59, 0.6);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      padding: 1.5rem;
      border-radius: 0.75rem;
      margin-bottom: 2rem;
      border: 1px solid rgba(148, 163, 184, 0.1);
      box-shadow: 0 4px 24px rgba(0, 0, 0, 0.2);
    }
    
    .demo-controls h4 {
      color: #f1f5f9;
      margin: 0 0 1rem 0;
      font-size: 0.9375rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.05em;
      opacity: 0.9;
    }
    
    .demo-controls button {
      background: rgba(59, 130, 246, 0.9);
      color: white;
      border: 1px solid rgba(96, 165, 250, 0.3);
      padding: 0.75rem 1.5rem;
      border-radius: 0.5rem;
      font-weight: 500;
      font-size: 0.875rem;
      cursor: pointer;
      margin-right: 0.75rem;
      margin-bottom: 0.75rem;
      transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
    }
    
    .demo-controls button:hover {
      transform: translateY(-1px);
      box-shadow: 0 4px 12px rgba(59, 130, 246, 0.3);
      background: rgba(59, 130, 246, 1);
      border-color: rgba(96, 165, 250, 0.5);
    }
    
    .demo-controls button:active {
      transform: translateY(0);
    }
  </style>
</head>
<body>
  <div class="demo-container">
    <!-- Header -->
    <div class="demo-header">
      <h1>AgusmaLab v3.0</h1>
      <p>Librería de Componentes UI Profesional</p>
    </div>

    <!-- Sección: Tarjetas de Estadísticas -->
    <div class="demo-section">
      <h2 class="section-title">
        Tarjetas de Estadísticas
      </h2>
      
      <div class="demo-controls">
        <h4>Controles Interactivos</h4>
        <button onclick="simularActualizacion()">Simular Actualización de Datos</button>
        <button onclick="simularCambios()">Mostrar Cambios Aleatorios</button>
      </div>
      
      <div class="stats-grid">
        <div id="stat1"></div>
        <div id="stat2"></div>
        <div id="stat3"></div>
        <div id="stat4"></div>
      </div>
    </div>

    <!-- Sección: Tabla Interactiva -->
    <div class="demo-section">
      <h2 class="section-title">
        Tabla Interactiva
      </h2>
      
      <div class="demo-controls">
        <h4>Características de la Tabla</h4>
        <p style="color: #94a3b8; margin: 0; font-size: 0.875rem;">
          Búsqueda en tiempo real | Ordenamiento por columnas | Paginación automática
        </p>
      </div>
      
      <div id="tabla-usuarios"></div>
    </div>

    <!-- Sección: Gráfico de Barras -->
    <div class="demo-section">
      <h2 class="section-title">
        Gráfico de Barras
      </h2>
      
      <div class="demo-controls">
        <h4>Controles del Gráfico</h4>
        <button onclick="actualizarGrafico1()">Ver Trimestre 1</button>
        <button onclick="actualizarGrafico2()">Ver Trimestre 2</button>
        <button onclick="actualizarGrafico3()">Datos Aleatorios</button>
      </div>
      
      <div id="grafico-ventas"></div>
    </div>
  </div>

  <!-- Cargar JavaScript -->
  <script src="agusmalab.js"></script>
  
  <!-- Inicialización y Demos -->
  <script>
    // ========================================
    // VARIABLES GLOBALES
    // ========================================
    
    let tarjeta1, tarjeta2, tarjeta3, tarjeta4;
    let grafico;
    
    // ========================================
    // TARJETAS DE ESTADÍSTICAS
    // ========================================
    
    tarjeta1 = new AgusmaLab.StatsCard('#stat1', {
      titulo: 'Usuarios Activos',
      valor: '2,847',
      icono: 'usuarios',
      colorIcono: 'primary',
      descripcion: 'Registrados hoy',
      cambio: '+12.5%',
      tipoCambio: 'positivo'
    });

    tarjeta2 = new AgusmaLab.StatsCard('#stat2', {
      titulo: 'Ingresos del Mes',
      valor: '€127,543',
      icono: 'dinero',
      colorIcono: 'success',
      descripcion: 'Objetivo: €150,000',
      cambio: '+23.8%',
      tipoCambio: 'positivo'
    });

    tarjeta3 = new AgusmaLab.StatsCard('#stat3', {
      titulo: 'Pedidos Pendientes',
      valor: '47',
      icono: 'pedidos',
      colorIcono: 'warning',
      descripcion: 'Procesar hoy',
      cambio: '-5 desde ayer',
      tipoCambio: 'neutral'
    });

    tarjeta4 = new AgusmaLab.StatsCard('#stat4', {
      titulo: 'Tasa de Conversión',
      valor: '3.42%',
      icono: 'tendencia',
      colorIcono: 'info',
      descripcion: 'Este mes',
      cambio: '-0.3%',
      tipoCambio: 'negativo'
    });

    // ========================================
    // TABLA INTERACTIVA
    // ========================================
    
    const tablaUsuarios = new AgusmaLab.DataTable('#tabla-usuarios', {
      titulo: 'Gestión de Usuarios - Sistema CRM',
      columnas: [
        { campo: 'id', etiqueta: 'ID', ordenable: true },
        { campo: 'nombre', etiqueta: 'Nombre Completo', ordenable: true },
        { campo: 'email', etiqueta: 'Email', ordenable: true },
        { campo: 'ciudad', etiqueta: 'Ciudad', ordenable: true },
        { campo: 'pais', etiqueta: 'País', ordenable: true },
        { campo: 'registro', etiqueta: 'F. Registro', ordenable: true },
        { campo: 'estado', etiqueta: 'Estado', ordenable: true }
      ],
      datos: [
        { id: 1, nombre: 'Ana García Pérez', email: 'ana.garcia@empresa.com', ciudad: 'Madrid', pais: 'España', registro: '2024-01-15', estado: 'Activo' },
        { id: 2, nombre: 'Carlos López Martín', email: 'carlos.lopez@empresa.com', ciudad: 'Barcelona', pais: 'España', registro: '2024-01-18', estado: 'Activo' },
        { id: 3, nombre: 'María Fernández Ruiz', email: 'maria.fernandez@empresa.com', ciudad: 'Valencia', pais: 'España', registro: '2024-02-01', estado: 'Activo' },
        { id: 4, nombre: 'Juan Martínez Soto', email: 'juan.martinez@empresa.com', ciudad: 'Sevilla', pais: 'España', registro: '2024-02-05', estado: 'Inactivo' },
        { id: 5, nombre: 'Laura Sánchez Gil', email: 'laura.sanchez@empresa.com', ciudad: 'Bilbao', pais: 'España', registro: '2024-02-08', estado: 'Activo' },
        { id: 6, nombre: 'Pedro Gómez Castro', email: 'pedro.gomez@empresa.com', ciudad: 'Málaga', pais: 'España', registro: '2024-02-10', estado: 'Activo' },
        { id: 7, nombre: 'Isabel Ruiz Moreno', email: 'isabel.ruiz@empresa.com', ciudad: 'Zaragoza', pais: 'España', registro: '2024-02-12', estado: 'Activo' },
        { id: 8, nombre: 'Miguel Torres Prieto', email: 'miguel.torres@empresa.com', ciudad: 'Murcia', pais: 'España', registro: '2024-02-14', estado: 'Pendiente' },
        { id: 9, nombre: 'Carmen Díaz Vega', email: 'carmen.diaz@empresa.com', ciudad: 'Palma', pais: 'España', registro: '2024-02-15', estado: 'Activo' },
        { id: 10, nombre: 'Antonio Jiménez Luna', email: 'antonio.jimenez@empresa.com', ciudad: 'Las Palmas', pais: 'España', registro: '2024-02-16', estado: 'Activo' },
        { id: 11, nombre: 'Rosa Álvarez Blanco', email: 'rosa.alvarez@empresa.com', ciudad: 'Valladolid', pais: 'España', registro: '2023-12-20', estado: 'Activo' },
        { id: 12, nombre: 'Francisco Romero Ortiz', email: 'francisco.romero@empresa.com', ciudad: 'Córdoba', pais: 'España', registro: '2023-12-22', estado: 'Inactivo' },
        { id: 13, nombre: 'Lucía Navarro Ramos', email: 'lucia.navarro@empresa.com', ciudad: 'Alicante', pais: 'España', registro: '2024-01-05', estado: 'Activo' },
        { id: 14, nombre: 'Javier Serrano Mendez', email: 'javier.serrano@empresa.com', ciudad: 'Vigo', pais: 'España', registro: '2024-01-08', estado: 'Activo' },
        { id: 15, nombre: 'Elena Molina Cruz', email: 'elena.molina@empresa.com', ciudad: 'Gijón', pais: 'España', registro: '2024-01-10', estado: 'Activo' },
        { id: 16, nombre: 'David Moreno Santos', email: 'david.moreno@empresa.com', ciudad: 'Hospitalet', pais: 'España', registro: '2024-01-12', estado: 'Pendiente' },
        { id: 17, nombre: 'Patricia Guerrero Silva', email: 'patricia.guerrero@empresa.com', ciudad: 'Coruña', pais: 'España', registro: '2024-01-20', estado: 'Activo' },
        { id: 18, nombre: 'Roberto Iglesias Vargas', email: 'roberto.iglesias@empresa.com', ciudad: 'Granada', pais: 'España', registro: '2024-01-22', estado: 'Activo' },
        { id: 19, nombre: 'Cristina Delgado Herrera', email: 'cristina.delgado@empresa.com', ciudad: 'Elche', pais: 'España', registro: '2024-01-25', estado: 'Activo' },
        { id: 20, nombre: 'Ángel Caballero Peña', email: 'angel.caballero@empresa.com', ciudad: 'Oviedo', pais: 'España', registro: '2024-01-28', estado: 'Inactivo' }
      ],
      busqueda: true,
      ordenamiento: true,
      paginacion: true,
      filasPorPagina: 8
    });

    // ========================================
    // GRÁFICO DE BARRAS
    // ========================================
    
    grafico = new AgusmaLab.BarChart('#grafico-ventas', {
      titulo: 'Ventas Mensuales 2024 - Primer Trimestre',
      etiquetas: ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo'],
      datos: [125, 180, 165, 220, 195],
      color: '#10b981',
      ancho: 800,
      alto: 350
    });

    // ========================================
    // FUNCIONES INTERACTIVAS
    // ========================================
    
    function simularActualizacion() {
      const nuevoValor = Math.floor(Math.random() * 5000) + 2000;
      tarjeta1.actualizarValor(nuevoValor.toLocaleString(), true);
      
      const nuevoIngreso = Math.floor(Math.random() * 50000) + 100000;
      tarjeta2.actualizarValor('€' + nuevoIngreso.toLocaleString(), true);
      
      const nuevosPedidos = Math.floor(Math.random() * 100) + 20;
      tarjeta3.actualizarValor(nuevosPedidos.toString(), true);
      
      const nuevaTasa = (Math.random() * 2 + 2).toFixed(2);
      tarjeta4.actualizarValor(nuevaTasa + '%', true);
      
      console.log('✨ Datos actualizados!');
    }
    
    function simularCambios() {
      const cambios = [
        { valor: (Math.random() * 30 - 10).toFixed(1), tipo: Math.random() > 0.5 ? 'positivo' : 'negativo' },
        { valor: (Math.random() * 30 - 10).toFixed(1), tipo: Math.random() > 0.5 ? 'positivo' : 'negativo' },
        { valor: (Math.random() * 30 - 10).toFixed(1), tipo: Math.random() > 0.5 ? 'positivo' : 'negativo' },
        { valor: (Math.random() * 30 - 10).toFixed(1), tipo: Math.random() > 0.5 ? 'positivo' : 'negativo' }
      ];
      
      tarjeta1.mostrarCambio((cambios[0].valor > 0 ? '+' : '') + cambios[0].valor + '%', cambios[0].tipo);
      tarjeta2.mostrarCambio((cambios[1].valor > 0 ? '+' : '') + cambios[1].valor + '%', cambios[1].tipo);
      tarjeta3.mostrarCambio((cambios[2].valor > 0 ? '+' : '') + cambios[2].valor + ' pedidos', cambios[2].tipo);
      tarjeta4.mostrarCambio((cambios[3].valor > 0 ? '+' : '') + cambios[3].valor + '%', cambios[3].tipo);
      
      console.log('📊 Cambios aplicados!');
    }
    
    function actualizarGrafico1() {
      grafico.actualizarDatos(
        [125, 180, 165, 220, 195],
        ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo']
      );
      console.log('📈 Gráfico actualizado - Trimestre 1');
    }
    
    function actualizarGrafico2() {
      grafico.actualizarDatos(
        [210, 195, 240, 225, 260],
        ['Junio', 'Julio', 'Agosto', 'Sept', 'Octubre']
      );
      console.log('📈 Gráfico actualizado - Trimestre 2');
    }
    
    function actualizarGrafico3() {
      const datosAleatorios = Array.from({length: 5}, () => Math.floor(Math.random() * 200) + 100);
      grafico.actualizarDatos(datosAleatorios);
      console.log('📈 Gráfico actualizado - Datos aleatorios');
    }

    // ========================================
    // INFORMACIÓN EN CONSOLA
    // ========================================
    
    console.log('%c AgusmaLab v3.0 Professional ', 'background: #1e293b; color: #60a5fa; font-size: 14px; font-weight: bold; padding: 8px 16px; border-radius: 4px;');
    console.log('%c Características:', 'color: #94a3b8; font-size: 12px; font-weight: bold; margin-top: 8px;');
    console.log('  → Diseño minimalista profesional');
    console.log('  → Tema oscuro slate/blue');
    console.log('  → Iconos SVG optimizados');
    console.log('  → Glassmorphism sutil');
    console.log('  → Animaciones fluidas');
    console.log('');
    console.log('📦 Componentes:', Object.keys(AgusmaLab).filter(k => k !== 'version' && k !== 'Iconos').join(', '));
    console.log('🔢 Versión:', AgusmaLab.version);
  </script>
</body>
</html>



```