# Interactive County/Regional Map

A standalone, embeddable interactive map built with Leaflet.js that works on any website platform (Wix, WordPress, Squarespace, custom sites, etc.).

## Features

- **Standalone HTML file** - No backend required, works completely client-side
- **Interactive markers** - Hover and click functionality for each region
- **Responsive design** - Works on desktop and mobile devices
- **Modern UI** - Clean design with smooth animations and transitions
- **Tooltip popups** - Detailed information display for each area
- **Easy customization** - Simple data structure for updating map information

## Quick Start

### Option 1: Direct Embedding (iframe)

1. Upload `interactive-map.html` to your web server or hosting service
2. Embed it using an iframe:

```html
<iframe src="https://yourdomain.com/interactive-map.html" 
        width="100%" 
        height="600" 
        frameborder="0" 
        style="border-radius: 16px;">
</iframe>
```

### Option 2: Code Injection (Direct HTML)

1. Copy the entire contents of `interactive-map.html`
2. Paste it into your website's HTML editor or custom code section
3. For platforms like Wix/WordPress, use the "HTML Embed" or "Custom Code" widget

### Option 3: Standalone Page

Simply open `interactive-map.html` in a web browser - it works completely standalone!

## Customization Guide

### Updating Map Data

Edit the `mapData` array in the JavaScript section to add, remove, or modify regions:

```javascript
const mapData = [
    {
        name: "Your Region Name",        // Display name
        lat: 33.1581,                     // Latitude coordinate
        lng: -117.3506,                  // Longitude coordinate
        color: "#667eea",                // Marker color (hex code)
        category: "Primary Region",      // Category label
        population: "125,000",           // Population info
        area: "45.2 sq mi",              // Area info
        description: "Your description"  // Detailed description
    },
    // Add more regions here...
];
```

### Changing Map Center and Zoom

Update these variables in the JavaScript:

```javascript
const mapCenter = [33.1215, -117.2878]; // [latitude, longitude]
const mapZoom = 11; // Zoom level (1-19, higher = more zoomed in)
```

### Customizing Colors

1. **Marker colors**: Change the `color` property in each `mapData` entry
2. **Background gradient**: Edit the `background` property in the `body` CSS rule
3. **Legend colors**: Update the `.legend-color` background colors in the HTML

### Styling Customization

All styles are contained in the `<style>` section. Key areas to customize:

- `.map-container`: Map container size and appearance
- `.popup-header`: Popup header styling
- `.popup-content`: Popup content styling
- `.map-legend`: Legend positioning and appearance

## Platform-Specific Instructions

### Wix

1. Add an "HTML Embed" element to your page
2. Paste the entire HTML code from `interactive-map.html`
3. Adjust the container size in the Wix editor

### WordPress

1. Use a "Custom HTML" block or widget
2. Paste the HTML code
3. Or use a plugin like "Insert Headers and Footers" for site-wide embedding

### Squarespace

1. Add a "Code Block" to your page
2. Paste the HTML code
3. The map will render automatically

### Custom Websites

Simply include the HTML file or paste the code directly into your page template.

## Browser Compatibility

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Dependencies

This map uses Leaflet.js loaded from CDN (unpkg.com). No local files or npm packages required.

- **Leaflet.js 1.9.4** - Loaded via CDN
- **OpenStreetMap tiles** - Free map tiles (no API key required)

## Troubleshooting

### Map not displaying

- Check internet connection (requires CDN access for Leaflet)
- Verify coordinates are valid (lat: -90 to 90, lng: -180 to 180)
- Check browser console for errors

### Markers not showing

- Verify `mapData` array is properly formatted
- Check that coordinates are within the map's visible bounds
- Ensure JavaScript is enabled in browser

### Responsive issues

- The map automatically adjusts on resize
- For iframe embedding, ensure responsive iframe code is used
- Check viewport meta tag is present

## Advanced Features

### Adding Custom Map Tiles

Replace the tile layer URL in the JavaScript:

```javascript
L.tileLayer('YOUR_TILE_URL/{z}/{x}/{y}.png', {
    attribution: 'Your attribution',
    maxZoom: 19
}).addTo(map);
```

### Adding More Interactive Features

The code is structured to easily add:
- Custom click handlers
- Additional popup content
- Animation effects
- Data filtering
- Search functionality

## License

Free to use and modify for any purpose.

## Support

For customization help or issues, refer to:
- [Leaflet Documentation](https://leafletjs.com/)
- [OpenStreetMap](https://www.openstreetmap.org/)

