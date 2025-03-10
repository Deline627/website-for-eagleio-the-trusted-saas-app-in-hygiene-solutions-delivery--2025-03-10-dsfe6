# EagleiO Landing Page Maintenance Guide

This guide will help you maintain and customize the EagleiO landing page. Follow these instructions carefully to make updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    EagleiO  <!-- Update this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>  <!-- Update menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    Soar Above Service Hassles with EagleiO  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    The trusted SaaS App revolutionizing Hygiene Solutions delivery  <!-- Subheading -->
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Sets font size (increases with md: and lg: prefixes)
- `mb-8`: Adds margin bottom spacing
- `hidden md:flex`: Hides on mobile, shows as flex on medium screens
- `space-x-8`: Adds horizontal spacing between elements

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://www.eagle360.app">Get Started</a>  <!-- External link -->
```

To update:
1. Internal links (starting with #) connect to section IDs
2. Replace `https://www.eagle360.app` with your actual app URL
3. Ensure section IDs match:
```html
<section id="features">  <!-- Must match href="#features" -->
<section id="benefits">  <!-- Must match href="#benefits" -->
<section id="faq">       <!-- Must match href="#faq" -->
```

### Call-to-Action Links
Update all CTA buttons:
```html
<a href="https://www.eagle360.app" class="px-8 py-4 text-lg font-semibold rounded-full bg-gradient-to-r from-blue-500 to-teal-400">
    Start Your Journey
</a>
```

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-4">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Cookie Policy</a></li>
    </ul>
</div>
```

To update:
1. Replace `href="#"` with actual page links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
<li><a href="cookies.html" class="text-gray-400 hover:text-white transition-colors duration-300">Cookie Policy</a></li>
```

2. Create corresponding HTML files in the same directory:
- privacy.html
- terms.html
- cookies.html

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
- Check that section IDs exactly match href attributes
- IDs are case-sensitive
- Remove any spaces in IDs

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the `container` class on parent elements
- Maintain the responsive class structure:
```html
class="text-4xl md:text-5xl lg:text-6xl"  <!-- Keeps mobile-first design -->
```

3. **Gradient Text Not Showing**
- Ensure all three classes are present:
```html
class="bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent"
```

### Need Help?
If you encounter issues:
1. Check class names match exactly
2. Verify all closing tags are present
3. Keep the existing responsive structure
4. Test on multiple screen sizes
5. Maintain the same class order as the original

Remember to test all changes across different devices and browsers before deploying to production.