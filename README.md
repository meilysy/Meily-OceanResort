# Ocean Resort Website - Signature Assignment Final Deliverable

**Course:** ITC2400.19967  
**Student:** Meily Sy  
**Email:** sy.m@northeastern.edu  
**Institution:** Northeastern University  
**Submission Date:** December 11, 2025

## Project Overview

This signature assignment demonstrates advanced web development skills through a comprehensive, multi-page resort website. The project showcases mastery of HTML5, CSS3, JavaScript form validation, responsive design, accessibility standards, and modern web development best practices.

**Website Theme:** Ocean Resort - A luxury oceanfront destination  
**Pages:** 8 fully responsive pages  
**Total Lines of CSS:** 1200+  
**JavaScript Features:** Form validation with auto-uppercase and field validation, automatic photo slideshow

## Assignment Objectives Achieved

### Technical Requirements
✅ **Multi-Page Website Structure** - 8 interconnected HTML5 pages  
✅ **Responsive Design** - Mobile-first approach with breakpoints at 960px, 768px, 680px, and 480px  
✅ **Semantic HTML5** - Proper use of `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`  
✅ **CSS Layout Techniques** - CSS Grid, Flexbox, and modern positioning  
✅ **Form Implementation** - Two functional forms with JavaScript validation  
✅ **JavaScript Validation** - Uppercase conversion, email validation, zip code validation  
✅ **Accessibility Compliance** - WCAG 2.1 AA standards with ARIA labels  
✅ **Cross-Browser Compatibility** - Tested on Chrome, Firefox, Safari, and Edge  
✅ **W3C Validation** - All HTML and CSS files validated  
✅ **Support Services Page** - Detailed services with ordered/unordered lists in amenities.html

### Advanced Features Implemented
- **JavaScript Form Validation** - Auto-capitalize first letter of names and city, 5-digit zip validation, email pattern validation
- **Automatic Photo Slideshow** - JavaScript-powered auto-advancing gallery with pause on hover
- **CSS Interactive Elements** - Navigation, modals without heavy frameworks
- **HTML5 Form Validation** - Using `required`, `pattern`, `type`, `min` attributes
- **CSS Pseudo-Classes** - `:target`, `:checked`, `:valid`, `:invalid` for interactivity
- **Responsive Images** - URL-encoded paths and optimized loading
- **Design System** - CSS custom properties for consistent theming
- **Performance Optimization** - Minimal CSS, efficient JavaScript

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
- **Resort Support Services Section** with ordered lists for major categories:
  1. Guest Services & Concierge
  2. Transportation Services
  3. Housekeeping & Maintenance
  4. Dining Services
  5. Business & Meeting Support
  6. Health & Wellness Support
- Each category includes unordered lists with specific hours of operation
- Pricing table for premium services

### 5. **Events (events.html)**
- Wedding packages and venues
- Conference facilities
- Event planning services
- Capacity and pricing information

### 6. **Gallery (gallery.html)**
- Photo slideshow with 12 images
- **JavaScript auto-advancing slideshow** (changes every 5 seconds)
- Manual navigation via clickable dots and arrows
- Pause on hover for reading captions
- Smart resume after manual interaction

### 7. **Special Offers (offers.html)**
- Grand opening specials (25% off)
- Spa experience packages
- Event booking discounts
- Limited-time promotions

### 8. **Contact & Booking (contact.html)**
- Comprehensive booking form with:
  - **City and Zip Code fields** (required)
  - **JavaScript validation** for uppercase first letters (first name, last name, city)
  - **Email validation** with regex pattern
  - **Zip code validation** (exactly 5 digits)
- Contact information display
- General inquiry form with validation
- Modal thank you messages
- Real-time field validation feedback

## 💻 Technical Details

### Technologies Used
- **HTML5**: Semantic markup, accessibility features, form validation attributes
- **CSS3**: Custom properties, Grid, Flexbox, keyframe animations
- **JavaScript**: Form validation (uppercase conversion, email/zip validation), automatic slideshow
- **Responsive Design**: Mobile-first approach with media queries
- **Hybrid Slideshow**: CSS structure with JavaScript auto-advance functionality

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
- Responsive breakpoints (960px, 768px, 680px, 480px)

/* Components */
- Navigation system (desktop + mobile hamburger)
- Cards (.card, .card-body)
- Buttons (.btn, .btn-primary)
- Forms (.form-grid, .form-group, validation states)
- Tables (.pricing)
- Slideshow (.slideshow-container, .slide)
- Services lists (.major-services, .service-details)
```

### JavaScript Features

**Form Validation (contact.html)**
```javascript
// Capitalize first letter of input fields
function capitalizeFirstLetter(input) {
  input.value = input.value.charAt(0).toUpperCase() + 
                input.value.slice(1).toLowerCase();
}

// Email validation with regex
function validateEmail(email) {
  const emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
  return emailPattern.test(email);
}

// Zip code validation (5 digits)
function validateZip(zip) {
  const zipPattern = /^\d{5}$/;
  return zipPattern.test(zip);
}
```

**Automatic Slideshow (gallery.html)**
```javascript
// Auto-advance every 5 seconds
let currentSlide = 1;
setInterval(() => {
  currentSlide = currentSlide >= 12 ? 1 : currentSlide + 1;
  document.getElementById('slide' + currentSlide).checked = true;
}, 5000);

// Pause on hover, manual navigation pauses then resumes
```

### Pure CSS Implementation Details

**Mobile Navigation**
```css
/* Checkbox hack for hamburger menu */
.nav-toggle-checkbox:checked ~ .nav-links { display: flex; }
.nav-toggle-checkbox:checked + .nav-toggle span:nth-child(1) { 
  transform: rotate(45deg) translate(5px, 5px); 
}
```

**Modal Thank You Messages**
```css
/* Hash-based modal display */
.modal:target { display: flex; }
/* Forms submit to hash URLs: action="#booking-thanks" */
```

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No build tools or dependencies required

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/MeilySy/ocean-resort.git
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
- Efficient JavaScript (vanilla JS, no frameworks or libraries)
- Automatic slideshow with smart pause/resume
- Efficient selectors and specificity
- Responsive images with appropriate sizing
- CSS containment for better rendering
- Hardware-accelerated CSS animations


## Project Files

### HTML Pages (8 files)
- `index.html` - Homepage with resort overview
- `accommodation.html` - Room types and pricing tables
- `restaurant.html` - Dining venues and menus
- `amenities.html` - Spa, fitness facilities, and support services (ordered/unordered lists)
- `events.html` - Wedding and conference packages
- `gallery.html` - JavaScript auto-advancing photo slideshow (12 images)
- `offers.html` - Special promotions and deals
- `contact.html` - Booking forms with JavaScript validation (city, zip, email, uppercase conversion)

### Stylesheet
- `styles.css` - Comprehensive stylesheet (1204 lines)
  - Design system with CSS custom properties
  - Responsive layouts with Grid and Flexbox (960px, 768px, 680px, 480px breakpoints)
  - Form validation styling
  - Services list styling with icons
  - Print styles and accessibility features

### JavaScript Files (embedded in HTML)
- `contact.html` - Form validation script (132 lines)
  - capitalizeFirstLetter() function
  - validateEmail() function  
  - validateZip() function
  - Event listeners for blur and submit
- `gallery.html` - Automatic slideshow script (58 lines)
  - Auto-advance with 5-second intervals
  - Pause on hover and manual interaction
  - Smart resume functionality

### Assets
- `images/` folder - 14 optimized images with URL-encoded paths

## How to View

1. Download/extract the "Signature Assignment Final Deliverable" folder
2. Open `index.html` in any modern web browser
3. Test the contact form validation by filling out the booking form
4. Visit the gallery to see the automatic slideshow
5. Check amenities.html for the support services section

## Technical Specifications

- **HTML Version:** HTML5
- **CSS Version:** CSS3
- **JavaScript:** Vanilla JavaScript (190 lines total across 2 files)
  - Form validation: ~132 lines
  - Slideshow automation: ~58 lines
- **Responsive Breakpoints:** 960px, 768px, 680px, 480px
- **Total Files:** 8 HTML + 1 CSS + 14 images = 23 files
- **CSS Lines:** 1204 lines
- **Validation:** W3C compliant (HTML + CSS)

---

## Academic Integrity Statement

This signature assignment represents original work completed independently by Meily Sy for course ITC2400.19967 at Northeastern University. All code, design decisions, and documentation are the result of the student's own effort and learning. This website is a fictional resort created solely for educational purposes.

**Student:** Meily Sy  
**Email:** sy.m@northeastern.edu  
**Course:** ITC2400.19967  
**Institution:** Northeastern University  
**Date:** December 11, 2025

---

**End of Documentation**
