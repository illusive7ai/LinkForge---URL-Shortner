# LinkForge---URL-Shortner
A professional URL shortening application that provides link compression, QR code generation, bulk processing capabilities and rich link previews.


## Overview

LinkForge is a comprehensive URL management tool that transforms long web addresses into concise, shareable links. The application features a modern interface with support for single URL shortening, bulk operations, automatic QR code generation and intelligent link previews that display metadata from target pages.

## Features

### Single URL Shortening
- Instant conversion of long URLs to short links
- Automatic protocol detection and correction (http/https)
- Real-time link preview showing title, description, and image metadata
- One-click copy functionality

### QR Code Generation
- Automatic QR code generation for every shortened link
- High-resolution QR code download as PNG images
- Toggle visibility of QR codes on demand

### Bulk URL Processing
- Process multiple URLs simultaneously (one per line)
- Batch shortening with progress feedback
- Individual and bulk copy functionality for results
- Error handling for invalid or failed URLs

### Link Previews
- Automatic metadata extraction from target pages
- Display of page titles, descriptions, and Open Graph images
- Graceful fallback when metadata is unavailable

### Technical Architecture
- Pure HTML, CSS, and JavaScript implementation
- Tailwind CSS for responsive design
- Lucide icon library for vector graphics
- QRCode.js for QR code generation
- Dual API fallback system (is.gd and v.gd) for high availability

## User Interface

The interface features a dark theme with animated gradient background and glass-morphism design elements. The application includes:

- Tabbed interface for single and bulk operations
- Responsive layout compatible with desktop and mobile devices
- Toast notification system for user feedback
- Keyboard shortcuts (Enter key for URL submission)
- Sticky navigation with feature shortcuts

## API Integration

LinkForge utilizes two public URL shortening services with automatic failover:

| Service | Endpoint | Purpose |
|---------|----------|---------|
| is.gd | create.php | Primary shortening service |
| v.gd | create.php | Fallback service |

The application also integrates with AllOrigins for cross-origin metadata fetching to enable link previews.

## Installation

No installation process or build steps are required. LinkForge runs entirely in the browser as a single HTML file with no server dependencies.

### Requirements
- Modern web browser with JavaScript enabled
- Internet connection for API calls and external resources

### Deployment Options
1. Download the HTML file and open it directly in any browser
2. Host the file on any static web server
3. Serve via local development server

## Usage Guide

### Shortening a Single URL

1. Navigate to the Single URL tab
2. Paste or type the long URL into the input field
3. Click the Shorten button or press Enter
4. Copy the resulting short URL using the Copy button
5. Generate a QR code by clicking the QR button
6. Download the QR code as an image file

### Bulk URL Shortening

1. Switch to the Bulk Shorten tab
2. Enter multiple URLs with one URL per line
3. Click the Shorten All URLs button
4. Review the results displayed in the results panel
5. Copy individual URLs or use Copy All Results

### Link Preview Feature

After shortening a URL, LinkForge automatically attempts to fetch and display:
- Page title
- Meta description
- Open Graph image (if available)
- Original URL for reference

The preview appears below the shortened link result.

## Error Handling

The application includes comprehensive error management for the following scenarios:

- Invalid URL format detection and user feedback
- Network failures during shortening operations
- API unavailability with automatic fallback to secondary service
- Descriptive error messages via the toast notification system

## Performance Considerations

- Asynchronous API requests prevent UI blocking during operations
- Efficient DOM manipulation for bulk result rendering
- Lazy loading of QR codes only when requested
- Debounced particle animation system for visual effects

## Browser Support

LinkForge is compatible with all modern browsers that support:

- ES6 JavaScript features
- CSS Grid and Flexbox
- Fetch API
- Clipboard API
- LocalStorage (not required but supported)

## Customization

The application can be customized by modifying:

- Color scheme in the Tailwind configuration and CSS variables
- Animation timing and particle effect parameters
- Default API endpoints in the shortening functions
- QR code dimensions in the generation parameters

## Limitations

- Maximum URL length is constrained by API provider limits
- Link preview functionality is subject to CORS policies and target site metadata availability
- QR code generation is client-side only with no server storage
- Bulk processing speed depends on network conditions and API response times

## Security

- All shortening operations are performed through HTTPS endpoints
- No user data is stored or transmitted to third parties beyond the shortening APIs
- Links are processed entirely client-side without logging

## License

This tool is provided for general use. The underlying icons and external libraries are subject to their respective licenses.

## Support

For issues related to the shortening APIs, refer to the is.gd and v.gd service documentation. For functional issues with the application interface, clear browser cache and ensure JavaScript is enabled.

## Version History

Version 1.0 - Initial release featuring single URL shortening, QR codes, bulk operations, and link previews.
