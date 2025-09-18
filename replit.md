# Overview

This is a personal landing page website for Maël Rolland, a PhD researcher specializing in the political economy of cryptocurrencies. The site features a retro-pixelated aesthetic inspired by 80s computer culture and Curve Finance's visual identity. It serves as a central hub for his academic work, publications, thesis materials, and professional information, with bilingual support (French/English) and multiple specialized sections including crisis research, curriculum, talks, and contact information.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Static Site Architecture**: Pure HTML/CSS implementation with no JavaScript frameworks
- **Responsive Design**: Mobile-first approach with CSS Grid and Flexbox layouts
- **Theme System**: CSS custom properties (variables) supporting light/dark themes with toggle functionality
- **Typography Strategy**: Google Fonts integration using Press Start 2P (pixel font) and VT323 (terminal font)
- **Component-Based Styling**: Centralized CSS in `style.css` with page-specific style overrides

## Design System
- **Visual Identity**: Retro-pixelated theme with matte red background gradients, yellow/orange text (#ffcc66, #ffaa33), and green accents (#33ff33)
- **Color Palette**: CSS custom properties defining primary backgrounds, text colors, and interactive states
- **Button System**: Consistent pixel-style button components with hover effects and border styling
- **Grid Layouts**: Responsive card systems for content organization, particularly in the crisis research hub

## Content Architecture
- **Multilingual Structure**: Parallel file structure with `-fr.html` suffixes for French versions
- **Specialized Sections**: 
  - Crisis research hub with interactive timeline and case studies
  - Thesis materials with chapter downloads
  - Professional curriculum and publications
  - Workshop/collaboration information
- **Navigation System**: Breadcrumb navigation and language switchers across pages

## Asset Management
- **Icon System**: Pixelated icons stored in `assets/icons/` directory for thematic consistency
- **Favicon Implementation**: Multiple favicon sizes for cross-platform compatibility
- **Image Optimization**: Pixel art rendering with `image-rendering: pixelated` CSS property

## SEO and Metadata
- **Comprehensive Meta Tags**: Open Graph, Twitter Cards, and structured data implementation
- **Semantic HTML**: Proper heading hierarchy and accessibility considerations
- **Multilingual SEO**: Language-specific canonical URLs and hreflang considerations

# External Dependencies

## Font Services
- **Google Fonts**: Press Start 2P and VT323 fonts with preconnect optimization for performance

## Third-Party Libraries
- **Chart.js**: JavaScript charting library for interactive timeline visualization in crisis research section

## Hosting and Deployment
- **GitHub Pages**: Primary hosting platform with potential for decentralized hosting (Swarm mentioned in documentation)
- **Static File Serving**: No server-side processing required, pure client-side rendering

## Development Tools
- **CSS Preprocessor**: None currently used, vanilla CSS with custom properties
- **Build System**: No build process, direct file deployment model
- **Version Control**: Git-based workflow compatible with GitHub Pages deployment