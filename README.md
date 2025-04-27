# House Of Doodles Landing Page - Maintenance Guide

This guide will help you maintain and customize the House Of Doodles landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the site logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold text-purple-600">
    House Of Doodles  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu item text here -->
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subtext:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Koop House Of Doodles Met Korting  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Nog maar enkele exemplaren beschikbaar!  <!-- Subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-{size}`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-{size}`: Adds padding top and bottom
- `bg-{color}`: Sets background color
- `hover:`: Prefix for hover effects

Example of modifying a button:
```html
<!-- Original button -->
<a href="https://amzn.to/4jPt4Xc" class="inline-block bg-purple-600 text-white px-8 py-4 rounded-full">

<!-- To make button larger and change color -->
<a href="https://amzn.to/4jPt4Xc" class="inline-block bg-blue-600 text-white px-10 py-5 rounded-full">
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal sections, keep the `#` prefix
2. Ensure the href matches the section's ID
3. For external links, use the full URL

Example:
```html
<!-- Change internal link -->
<a href="#new-section">New Section</a>

<!-- Add external link -->
<a href="https://example.com/page">External Page</a>
```

### Call-to-Action Buttons
Update the Amazon affiliate links:
```html
<!-- Find these buttons -->
<a href="https://amzn.to/4jPt4Xc" class="inline-block bg-purple-600...">
    Bekijk Aanbieding
</a>

<!-- Replace with your new link -->
<a href="https://your-new-link.com" class="inline-block bg-purple-600...">
    Bekijk Aanbieding
</a>
```

## Linking Privacy and Terms Pages

### Footer Links Section
Current footer links structure:
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-purple-400">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-purple-400">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the footer links:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="hover:text-purple-400">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-purple-400">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
- Ensure section IDs match exactly with href attributes
- Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues:**
- Check responsive classes (e.g., `md:`, `lg:`)
- Test on different screen sizes
- Don't remove responsive prefixes unless intended

3. **Style Changes Not Working:**
- Verify Tailwind CSS is properly loaded
- Check for typos in class names
- Ensure classes are in the correct order

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always backup your files before making changes, and test thoroughly on different devices and browsers after updates.