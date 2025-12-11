# Terrain Trace Website

## Professional Multi-Page Website for Automated Lawn Care Solutions

This is a complete, professional website for Terrain Trace - an authorized Yarbo dealer in Orem and Provo, Utah, specializing in robotic lawn mowers and snow blowers.

---

## 📁 Project Structure

```
terrain-trace-website/
├── index.html              # Homepage
├── lawn-mowers.html        # (To be created) Lawn mowers product page
├── snow-blower.html        # (To be created) Snow blower product page
├── services.html           # (To be created) Services page
├── about.html              # (To be created) About page
├── contact.html            # (To be created) Contact page
├── css/
│   └── style.css          # Main stylesheet
├── js/
│   └── main.js            # JavaScript functionality
└── images/                 # (Add your images here)
```

---

## ✨ Features

### Design
- **Professional & Classy**: Sophisticated earth-tone color palette with premium serif fonts
- **Fully Responsive**: Mobile-first design that works on all devices
- **Smooth Animations**: Scroll-triggered fade-ins and hover effects
- **Modern UI/UX**: Clean, intuitive navigation and clear calls-to-action

### Functionality
- Fixed navigation bar with scroll effects
- Mobile-friendly hamburger menu
- Smooth scrolling to sections
- Form validation
- Back-to-top button
- Lazy image loading ready
- Active page highlighting

### SEO Ready
- Semantic HTML5 markup
- Meta descriptions
- Proper heading hierarchy
- Fast-loading optimized code

---

## 🎨 Design System

### Color Palette
- **Primary Green**: `#2d6a4f` - Trust, growth, nature
- **Secondary Green**: `#52b788` - Fresh, energetic
- **Accent Green**: `#95d5b2` - Light, approachable
- **Slate Grays**: Professional, clean backgrounds

### Typography
- **Headings**: Crimson Pro (elegant serif)
- **Body**: Lora (readable serif)
- **UI Elements**: System fonts (crisp, modern)

---

## 🚀 Getting Started

### Option 1: Simple Setup (No Server Required)
1. Extract all files to a folder
2. Double-click `index.html` to open in your browser
3. Navigate using the menu

### Option 2: Local Development Server

#### Using Python 3:
```bash
cd terrain-trace-website
python -m http.server 8000
```
Then visit: `http://localhost:8000`

#### Using Node.js:
```bash
npm install -g http-server
cd terrain-trace-website
http-server
```

#### Using PHP:
```bash
cd terrain-trace-website
php -S localhost:8000
```

---

## 📝 Customization Guide

### Update Contact Information

**In all HTML files**, search and replace:
- Phone: `(801) 555-1234` → Your actual phone
- Email: `info@terraintrace.com` → Your actual email

### Add Your Logo
Replace the SVG logo in the navigation with:
```html
<img src="images/logo.png" alt="Terrain Trace Logo">
```

### Add Product Images
1. Place images in the `images/` folder
2. Update the placeholder divs in HTML:
```html
<!-- Replace this: -->
<div class="placeholder-image lawn-mower">
    <svg>...</svg>
</div>

<!-- With this: -->
<img src="images/yarbo-lawn-mower.jpg" alt="Yarbo Lawn Mower">
```

### Change Colors
Edit CSS variables in `css/style.css`:
```css
:root {
    --primary: #2d6a4f;      /* Your primary color */
    --secondary: #52b788;     /* Your secondary color */
    --accent: #95d5b2;        /* Your accent color */
}
```

---

## 📄 Remaining Pages to Create

You'll need to create these additional pages following the same structure as `index.html`:

### 1. lawn-mowers.html
- Hero section for lawn mowers
- Comparison: Standard vs Pro models
- Detailed specifications
- Photo gallery
- Pricing options
- Installation info

### 2. snow-blower.html
- Hero section for snow blower
- Key features and specs
- Winter performance details
- Photo gallery
- Pricing and packages

### 3. services.html
- Detailed service descriptions
- Installation process
- Maintenance packages
- Leasing options
- Warranty information

### 4. about.html
- Company story
- Team introduction
- Why choose Terrain Trace
- Service area map
- Testimonials

### 5. contact.html
- Contact form (already styled)
- Location information
- Business hours
- Map embed
- FAQ section

**Each page should include:**
- Same header/navigation
- Same footer
- Consistent styling
- Unique content

---

## 🔧 Technical Details

### Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

### Performance
- Minimal dependencies (no frameworks required)
- CSS and JS are vanilla (no jQuery, React, etc.)
- Optimized for fast loading
- Lazy loading ready for images

### Accessibility
- Semantic HTML
- ARIA labels where needed
- Keyboard navigation support
- Screen reader friendly

---

## 📱 Mobile Menu

The mobile menu activates automatically on screens under 768px width. It features:
- Full-screen overlay
- Smooth animations
- Touch-friendly buttons
- Auto-close on link click

---

## 🎯 Call-to-Actions

Strategic CTAs throughout the site:
1. **Primary**: "Get Started" / "Explore Lawn Mowers"
2. **Secondary**: "Request Quote" / "Schedule Consultation"
3. **Tertiary**: Product-specific "Learn More" buttons

---

## 📊 Analytics Setup

To add Google Analytics:

1. Get your GA4 tracking ID
2. Add before `</head>` in each HTML file:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🌐 Deployment Options

### Option 1: Netlify (Recommended - Free)
1. Create account at netlify.com
2. Drag & drop your website folder
3. Done! Netlify provides HTTPS and CDN

### Option 2: GitHub Pages (Free)
1. Create GitHub repository
2. Push files to repo
3. Enable GitHub Pages in settings

### Option 3: Traditional Web Hosting
1. Upload via FTP/SFTP
2. Point your domain to the hosting
3. Configure SSL certificate

---

## 📧 Form Backend Setup

The contact form needs a backend. Options:

### Formspree (Easiest)
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Netlify Forms
Add `netlify` attribute:
```html
<form netlify name="contact">
```

### Custom Backend
Integrate with your own server/API

---

## 🔐 Important Notes

1. **Update all placeholder content** before going live
2. **Test forms** thoroughly
3. **Add real images** to improve visual appeal
4. **Set up SSL certificate** for security
5. **Create a favicon** for browser tabs
6. **Add Google My Business** listing for local SEO

---

## 📞 Support

For questions about this website:
- Review the code comments
- Check browser console for errors
- Validate HTML at validator.w3.org
- Test CSS at jigsaw.w3.org/css-validator

---

## 📜 License

This website template is created specifically for Terrain Trace. Modify as needed for your business.

---

## 🎉 Next Steps

1. ✅ Review the homepage
2. ⬜ Create remaining pages (lawn-mowers.html, etc.)
3. ⬜ Add real product images
4. ⬜ Update contact information
5. ⬜ Set up form backend
6. ⬜ Test on multiple devices
7. ⬜ Deploy to web hosting
8. ⬜ Set up Google Analytics
9. ⬜ Submit to Google Search Console
10. ⬜ Launch! 🚀

---

**Built with care for Terrain Trace** | Last Updated: December 2024
