# DSJ Tax Landing Page Maintenance Guide

This guide will help you maintain and customize the DSJ Tax landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Company Name and Logo
```html
<!-- Located in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    DSJ Tax  <!-- Change this text to update company name -->
</div>
```

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6...">
    DSJ Tax Multi-Services South Florida Debt Collection & Tax Preparation  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8">
    Streamlined, fast & efficient tax prep & debt collection  <!-- Subheadline -->
</p>
```

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:` - Applies styles on medium screens (768px and up)
- `lg:` - Applies styles on large screens (1024px and up)
- Example:
```html
<div class="text-xl md:text-2xl">  <!-- Text size increases on medium screens -->
```

#### Common Styling Classes
- Background Colors: `bg-gray-900`, `bg-purple-500`
- Text Colors: `text-gray-100`, `text-purple-400`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Hover Effects: `hover:scale-105`, `hover:text-purple-400`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

To update internal links:
1. Locate the section ID you want to link to
2. Update the `href` attribute with `#` followed by the section ID
3. Example: `<a href="#new-section">New Section</a>`

### External Links
The "Get Started" button links to a JotForm:
```html
<a href="https://form.jotform.com/250476421727054" class="...">
    Get Started
</a>
```

To update external links:
1. Replace the URL in the `href` attribute
2. Ensure the new URL includes `https://` or `http://`
3. Test the link to confirm it works

## Linking Privacy and Terms Pages

### Current Footer Links Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Privacy and Terms Links
1. Create your privacy.html and terms.html files
2. Update the href attributes in the footer:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify section IDs match href attributes exactly
   - Check for typos in IDs and hrefs
   - Ensure section IDs are unique

2. **Responsive Design Issues**
   - Check media query classes (md:, lg:)
   - Test on different screen sizes
   - Verify Tailwind CSS CDN link is working

3. **Styling Problems**
   - Confirm Tailwind CSS classes are spelled correctly
   - Check for conflicting classes
   - Verify class order (later classes override earlier ones)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always back up your files before making changes, and test thoroughly across different devices and browsers.