# Airco Keuze Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Airco Keuze landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Airco Keuze</a>
```
Simply replace "Airco Keuze" with your desired text.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
    <!-- Additional menu items -->
</div>
```
Replace the text between `<a>` tags to update menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 text-gray-900">
    Snel De Juiste Airco Voor De Laagste Prijs
</h1>
```
- To modify heading size: adjust `text-4xl`, `text-5xl`, or `text-6xl`
- To change spacing: modify `mb-6` (margin-bottom)
- To update text color: change `text-gray-900`

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`
- Colors: `text-blue-600`, `text-gray-600`, `text-white`
- Spacing: `px-6` (padding-x), `py-4` (padding-y), `mb-6` (margin-bottom)
- Hover effects: `hover:bg-blue-700`, `hover:text-white`

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Voordelen</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Identify the section id you want to link to
2. Update the `href` attribute with `#section-id`
3. Example: `<a href="#new-section">New Section</a>`

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Over ons</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
</ul>
```
To update:
1. Replace `#` with your actual URL
2. Example: `<a href="about.html">Over ons</a>`

## Adding Privacy and Terms Pages

### Step 1: Locate Footer Links
Find this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Update Link References
Replace the placeholder `#` with actual page links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- Example: `href="#features"` must match `id="features"`
- IDs are case-sensitive

2. **Responsive Design Issues**
- Check mobile display using browser dev tools
- Verify that `md:` and `lg:` classes are properly set
- Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. **Style Changes Not Applying**
- Confirm Tailwind CSS is properly loaded
- Check for typos in class names
- Verify class order (later classes override earlier ones)

### Need Help?
- Double-check the Tailwind CSS documentation
- Use browser developer tools to inspect elements
- Ensure all HTML tags are properly closed
- Validate your HTML using W3C Validator

Remember to always test changes across different screen sizes and browsers before deploying to production.