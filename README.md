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