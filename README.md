# Armadale Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Armadale accounting services landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-indigo-500 bg-clip-text text-transparent">
    Armadale  <!-- Change this text to update company name -->
</a>
```

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

### Hero Section
The main headline and subheading can be updated here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent">
    Building financial clarity in a complex world  <!-- Main headline -->
</h1>
<p class="text-xl text-gray-400 mb-8">
    Professional accounting services tailored to your business needs  <!-- Subheading -->
</p>
```

### Tailwind CSS Class Guide
Common classes and their purposes:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-{weight}`: Controls text weight (bold, semibold, medium)
- `bg-{color}`: Sets background color
- `text-{color}`: Sets text color
- `p-{size}`: Sets padding
- `m-{size}`: Sets margin
- `rounded-{size}`: Controls border radius

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<!-- Update these href attributes -->
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<!-- Update with actual URL -->
<a href="https://theaccountants.com" class="inline-block px-8 py-4...">
    Get Started Today
</a>
```

3. Footer Links:
```html
<!-- Update these placeholder links -->
<ul class="space-y-2 text-gray-400">
    <li><a href="#">Business Valuation</a></li>
    <li><a href="#">Audit Preparation</a></li>
    <li><a href="#">Compliance Monitoring</a></li>
</ul>
```

### How to Update Links
1. Internal Links (same page):
   - Use `#section-id` format
   - Example: `<a href="#services">Services</a>`

2. External Links:
   - Use full URL including https://
   - Example: `<a href="https://your-domain.com/page">Link</a>`

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate this section in the footer:
```html
<div class="flex space-x-6 mt-4 md:mt-0">
    <!-- Update these href attributes -->
    <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
</div>
```

To add new policy pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes to point to these files
3. Maintain consistent styling by copying the classes

## Troubleshooting

### Common Issues and Solutions

1. Broken Layout:
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure responsive classes (md:, lg:) are properly ordered

2. Links Not Working:
   - Verify file paths are correct
   - Check for typos in href attributes
   - Ensure IDs match exactly for internal links

3. Styling Issues:
   - Confirm Tailwind CSS is properly loaded
   - Check for conflicting classes
   - Verify class names match Tailwind v2.x syntax

### Need Help?
- Review the [Tailwind CSS documentation](https://v2.tailwindcss.com/docs)
- Check browser developer tools (F12) for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different screen sizes using your browser's developer tools before deploying to production.