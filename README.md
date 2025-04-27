# Clarksburg Glass Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Clarksburg Glass landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- CTA Section
- Footer

### Updating Text Content

#### Company Name
```html
<!-- Located in the header -->
<a href="/" class="text-2xl font-bold">
    Clarksburg Glass
</a>
```
To change the company name, simply modify the text between the `<a>` tags.

#### Hero Section Text
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8">
    Clarksburg Shower Glass Company
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Low-iron glass - crystal clear designs...
</p>
```
To update:
1. Locate the `<h1>` tag in the hero section
2. Replace the text while keeping the HTML tags intact
3. Update the description in the `<p>` tag below

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
In this template, responsive classes use these prefixes:
- `md:` - applies to medium screens (768px and up)
- `lg:` - applies to large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-6xl (3.75rem)
- Desktop: text-7xl (4.5rem)

#### Common Tailwind Classes Used
- Layout: `container`, `mx-auto`, `px-6`, `py-24`
- Flex: `flex`, `items-center`, `justify-center`
- Colors: `bg-gray-900`, `text-white`, `text-gray-300`
- Typography: `text-xl`, `font-bold`, `text-center`

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

2. Call-to-Action Links:
```html
<a href="http://www.customeuroglass.com">Get Started</a>
```

### Updating Links
1. Internal Links (Same Page):
   - Use `#section-id` format
   - Ensure the referenced section has matching ID
   ```html
   <!-- Navigation link -->
   <a href="#features">Features</a>
   
   <!-- Matching section -->
   <section id="features">
   ```

2. External Links:
   - Replace `http://www.customeuroglass.com` with your desired URL
   - Always include `http://` or `https://`
   ```html
   <a href="https://your-website.com">Get Started</a>
   ```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
        <!-- Add these new links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling:
```html
<body class="bg-gray-900 text-gray-100 font-inter antialiased">
    <!-- Header (copy from index.html) -->
    
    <main class="container mx-auto px-6 py-24">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>
    
    <!-- Footer (copy from index.html) -->
</body>
```

## Troubleshooting

### Common Issues

1. Broken Internal Links
- Check that section IDs match exactly with href values
- IDs are case-sensitive
- Remove any spaces in IDs

2. Responsive Design Issues
- Verify media query prefixes (`md:`, `lg:`)
- Test at different screen sizes
- Check for missing responsive classes

3. Styling Inconsistencies
- Maintain the same color scheme:
  ```html
  text-gray-300 /* for secondary text */
  bg-gray-900 /* for dark backgrounds */
  from-blue-400 to-emerald-400 /* for gradients */
  ```
- Use consistent spacing classes (`px-6`, `py-24`)

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making changes, and test all modifications across different devices and browsers.