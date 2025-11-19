# 🏖️ Meily - Ocean Resort Website

A modern, responsive luxury resort website showcasing oceanfront accommodations, dining, amenities, and event spaces. This project demonstrates professional web development practices with clean HTML5, CSS3, and vanilla JavaScript.

![Ocean Resort](images/hero%20banner.jpg)

## 📋 Project Overview

**Ocean Resort** is a fully functional, multi-page website for a brand new luxury oceanfront resort. The site features a contemporary design, intuitive navigation, and comprehensive information about accommodations, dining, spa facilities, event venues, and special offers.

**Course**: ITC2400.19967  
**Institution**: Northeastern University  
**Developer**: Meily Sy  
**Contact**: sy.m@northeastern.edu

## ✨ Features

### Core Functionality
- 🏠 **8 Fully Responsive Pages** - Optimized for desktop, tablet, and mobile devices
- 🎨 **Modern Design System** - Consistent branding with CSS custom properties
- 📱 **Mobile-First Navigation** - Collapsible hamburger menu for small screens
- 🖼️ **CSS-Only Photo Gallery** - Pure CSS auto-advancing slideshow
- 📝 **Interactive Booking Forms** - Form submissions with thank you messages and auto-reset
- ♿ **WCAG Accessibility** - Semantic HTML, ARIA labels, and keyboard navigation

### Design Highlights
- Fluid typography with `clamp()` for scalable text
- Smooth transitions and hover effects
- Gradient overlays and shadows for depth
- Optimized images with proper alt text
- Dark mode support via CSS media queries

## 🗂️ Site Structure

```
📦 Ocean Resort Website
├── 📄 index.html              # Homepage with resort overview
├── 📄 accommodation.html      # Room types and pricing
├── 📄 restaurant.html         # Dining options and menus
├── 📄 amenities.html          # Spa, fitness, and services
├── 📄 events.html             # Wedding and conference venues
├── 📄 gallery.html            # Photo slideshow gallery
├── 📄 offers.html             # Special packages and deals
├── 📄 contact.html            # Booking form and contact info
├── 🎨 styles.css              # Global stylesheet (945 lines)
└── 🖼️ images/                # Image assets folder
    ├── hero banner.jpg
    ├── logo.PNG
    ├── standard room.jpg
    ├── deluxe ocean view.jpg
    ├── one bedroom suite.jpg
    ├── dining.jpg
    ├── breakfast.jpg
    ├── dinner sunset.jpg
    ├── spa.jpg
    ├── fitness.jpg
    ├── grand ballroom.jpg
    ├── beachfront ceremony.jpg
    └── oceanview conference.jpg
```

## 🎯 Pages Overview

### 1. **Home (index.html)**
- Hero banner with call-to-action buttons
- Resort story and mission statement
- Featured rooms preview
- Special offers highlights
- Resort features and amenities overview

### 2. **Accommodation (accommodation.html)**
- Three room types with detailed descriptions
- Pricing comparison table
- Room features and amenities lists
- Direct booking links

### 3. **Restaurant (restaurant.html)**
- Three dining venues overview
- Breakfast, lunch, and dinner menus
- Bar and lounge options
- Dietary accommodations information

### 4. **Amenities (amenities.html)**
- Spa and wellness services
- Fitness center features
- Resort services (concierge, housekeeping, etc.)
- Pricing table for premium services

### 5. **Events (events.html)**
- Wedding packages and venues
- Conference facilities
- Event planning services
- Capacity and pricing information

### 6. **Gallery (gallery.html)**
- CSS-only photo slideshow with 12 images
- Auto-advancing animation (5 seconds per slide)
- Manual navigation via clickable dots
- Pause on hover for reading captions
- No JavaScript required

### 7. **Special Offers (offers.html)**
- Grand opening specials (25% off)
- Spa experience packages
- Event booking discounts
- Limited-time promotions

### 8. **Contact & Booking (contact.html)**
- Comprehensive booking form with thank you message
- Contact information display
- General inquiry form with confirmation
- Auto-reset forms after submission

## 💻 Technical Details

### Technologies Used
- **HTML5**: Semantic markup, accessibility features
- **CSS3**: Custom properties, Grid, Flexbox, keyframe animations
- **JavaScript**: Minimal JS for mobile navigation and form handling only
- **Responsive Design**: Mobile-first approach with media queries
- **CSS-Only Slideshow**: Pure CSS animations with radio button controls

### CSS Architecture
```css
/* Design System */
- CSS Custom Properties (--brand, --text, --space-*, --step-*)
- Fluid typography with clamp()
- Consistent spacing scale
- Reusable component classes

/* Layout Patterns */
- Grid layouts (.grid-3, .two-column)
- Flexbox components (.nav-links, .banner-overlay)
- Container system with max-width
- Responsive breakpoints (768px, 480px)

/* Components */
- Navigation system (desktop + mobile)
- Cards (.card, .card-body)
- Buttons (.btn, .btn-primary)
- Forms (.form-grid, .form-group)
- Tables (.pricing)
- CSS-Only Slideshow (.css-slideshow-container, .css-slide)
```

### JavaScript Features
```javascript
// Mobile Navigation Toggle
- Hamburger menu functionality
- ARIA attribute management
- Dynamic year in footer

// Form Handling
- Booking form submission with thank you alert
- Contact form submission with confirmation
- Automatic form reset after submission

// CSS-Only Slideshow (No JavaScript!)
- Pure CSS animations with @keyframes
- Radio button state management
- Auto-advance every 5 seconds
- Manual navigation via label clicks
- Hover to pause animation
```

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No build tools or dependencies required

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/ocean-resort.git
cd ocean-resort
```

2. **Open in browser**
```bash
# Simply open index.html in your browser
# Or use a local server (recommended)
python -m http.server 8000
# Then visit http://localhost:8000
```

3. **Or use VS Code Live Server**
- Install Live Server extension
- Right-click `index.html`
- Select "Open with Live Server"

## 📱 Browser Compatibility

Tested and working on:
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## ♿ Accessibility Features

- Semantic HTML5 elements (`<header>`, `<nav>`, `<main>`, `<footer>`)
- ARIA labels for navigation and interactive elements
- Skip links and screen reader-only text where appropriate
- Keyboard navigation support
- Focus indicators for interactive elements
- Color contrast ratios meeting WCAG AA standards
- Alt text for all images
- Form labels and error messages properly associated

## 🎨 Design System

### Color Palette
```css
--brand: #007ea7;      /* Ocean Blue */
--brand-2: #80ced7;    /* Sky Blue */
--text: #1e3d59;       /* Dark Blue Gray */
--muted: #6b8599;      /* Muted Text */
--paper: #ffffff;      /* Background White */
--soft: #f6f8fb;       /* Light Background */
--line: #e6edf3;       /* Borders/Dividers */
```

### Typography Scale
```css
--step--1: 0.875rem - 0.95rem   /* Small text */
--step-0:  1rem - 1.05rem       /* Body text */
--step-1:  1.125rem - 1.25rem   /* Subheadings */
--step-2:  1.35rem - 1.6rem     /* H3 */
--step-3:  1.7rem - 2.1rem      /* H2 */
--step-4:  2.1rem - 2.8rem      /* H1 */
```

### Spacing Scale
```css
--space-1: 0.5rem - 0.65rem
--space-2: 0.8rem - 1rem
--space-3: 1.2rem - 1.6rem
--space-4: 1.8rem - 2.4rem
--space-5: 2.6rem - 3.4rem
```

## 📊 Performance Optimization

- Image preloading for hero banners
- Optimized CSS (no unused styles)
- Minimal JavaScript (vanilla JS, no frameworks or libraries)
- CSS-only slideshow reduces JavaScript dependency
- Efficient selectors and specificity
- Responsive images with appropriate sizing
- CSS containment for better rendering
- Hardware-accelerated CSS animations

## 🔧 Customization

### Changing Colors
Edit CSS custom properties in `styles.css`:
```css
:root {
  --brand: #007ea7;    /* Change primary color */
  --brand-2: #80ced7;  /* Change secondary color */
}
```

### Adding New Pages
1. Copy an existing HTML file
2. Update `<title>` and meta description
3. Modify navigation active state
4. Update content in `<main>` section
5. Ensure footer links are correct

### Modifying the CSS-Only Slideshow
Edit `gallery.html` to add/remove slides:
```html
<!-- Add radio button for new slide -->
<input type="radio" name="slideshow" id="slide13">

<!-- Add slide content -->
<div class="css-slide">
  <img src="images/your-image.jpg" alt="Description">
  <div class="slide-caption">Your caption here</div>
</div>

<!-- Add dot indicator -->
<label for="slide13" class="css-dot" aria-label="Go to slide 13"></label>
```

Update the CSS animation timings in `styles.css` if changing the number of slides!

## 📝 Code Quality

### Standards Followed
- HTML5 semantic markup
- CSS3 modern features (Grid, Flexbox, Custom Properties, Keyframe Animations)
- BEM-inspired naming conventions
- Consistent indentation (2 spaces)
- Comprehensive comments
- Accessible form practices
- Mobile-first responsive design
- Progressive enhancement (works without JavaScript)

### Validation
- ✅ HTML validated (W3C Markup Validation)
- ✅ CSS validated (W3C CSS Validation)
- ✅ Accessibility checked (WAVE, axe DevTools)
- ✅ Responsive design tested across devices

## 🐛 Known Issues

None at this time. Please report any issues via GitHub Issues.

## 📈 Future Enhancements

Potential improvements for future versions:
- [ ] Backend integration (Node.js/Express)
- [ ] Database for bookings (MongoDB/PostgreSQL)
- [ ] Real-time availability calendar
- [ ] Payment gateway integration
- [ ] Email notification system
- [ ] Admin dashboard for content management
- [ ] Multi-language support (i18n)
- [ ] Advanced image gallery (lightbox)
- [ ] Virtual tour integration
- [ ] Live chat support

## 📄 License

This project is created for educational purposes as part of coursework at Northeastern University.

## 👤 Author

**Meily Sy**
- 📧 Email: sy.m@northeastern.edu
- 🎓 Institution: Northeastern University
- 📚 Course: ITC2400.19967

## 🙏 Acknowledgments

- Images sourced from stock photo libraries (ensure proper licensing)
- Color palette inspired by modern hospitality design
- Typography choices based on web accessibility guidelines
- Layout patterns influenced by current web design trends

## 📸 Screenshots

### Desktop View
![Desktop Homepage](screenshots/desktop-home.png)
![Accommodation Page](screenshots/desktop-accommodation.png)

### Mobile View
![Mobile Navigation](screenshots/mobile-nav.png)
![Mobile Gallery](screenshots/mobile-gallery.png)

---

**Note**: This is a student project for academic purposes. All resort information is fictional and for demonstration only.

---

⭐ **If you find this project helpful, please consider giving it a star!**

Last Updated: November 19, 2025
