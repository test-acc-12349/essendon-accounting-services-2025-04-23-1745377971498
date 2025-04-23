# Essendon Accounting Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Essendon Accounting landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-xl font-bold tracking-tight text-white hover:text-blue-400 transition duration-300">
    Essendon Accounting  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Change menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page, featuring main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-8">
    Essendon accounting services  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Trusted advisors for your financial future  <!-- Update subheading -->
</p>
```

### Tailwind CSS Class Guide
Common classes used throughout the page:

- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, etc.
- Colors: `text-white`, `text-gray-300`, `text-blue-400`
- Background colors: `bg-gray-900`, `bg-blue-600`
- Spacing: `p-8` (padding), `m-4` (margin), `space-x-8` (horizontal spacing)
- Responsive prefixes: `md:` (medium screens), `lg:` (large screens)

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
<a href="https://theaccountants.com">Get Started</a>  <!-- External link to update -->
```

### Updating Links
1. Internal Links (Sections):
   - Keep the `#` prefix for same-page navigation
   - Ensure the `id` attribute matches in the corresponding section

2. External Links:
   - Replace `https://theaccountants.com` with your actual website URL
   - Example:
```html
<a href="https://your-actual-website.com">Get Started</a>
```

3. Email Links:
```html
<a href="mailto:support@example.com">support@example.com</a>
<!-- Replace with your actual email address -->
```

## Linking Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To properly link your privacy and terms pages:

1. Create two new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the href attributes:
```html
<!-- For same directory -->
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>

<!-- For subdirectory -->
<a href="legal/privacy.html">Privacy Policy</a>
<a href="legal/terms.html">Terms of Service</a>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links:**
   - Verify that section IDs match the href attributes
   - Example: `href="#services"` should match `id="services"`

2. **Responsive Design Issues:**
   - Check mobile display using browser dev tools
   - Ensure proper use of responsive prefixes (`sm:`, `md:`, `lg:`)

3. **Missing Styles:**
   - Verify Tailwind CSS link in header:
```html
<link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
```

### Best Practices

1. Always test links after updating
2. Maintain consistent styling across all pages
3. Keep backup copies before making major changes
4. Test on multiple browsers and devices
5. Validate HTML using W3C Validator

Need additional help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).