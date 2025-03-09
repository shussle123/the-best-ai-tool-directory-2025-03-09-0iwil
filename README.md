# AI Tool Directory Landing Page - Maintenance Guide

This guide will help you maintain and customize the AI Tool Directory landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo text. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">AI Tool Directory</a>
```
Simply replace "AI Tool Directory" with your desired text.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">The BEST AI Tool Directory</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Best AI Tool For Writing Content</p>
```

To modify:
- Change the h1 text between the tags
- Adjust text size using Tailwind classes:
  - `text-4xl` (mobile)
  - `md:text-5xl` (medium screens)
  - `lg:text-6xl` (large screens)

### Understanding Tailwind Classes

Key classes used in this template:
- `bg-gray-900`: Dark background
- `text-gray-100`: Light text
- `container mx-auto`: Centers content
- `px-6`: Horizontal padding
- `py-4`: Vertical padding
- `rounded-2xl`: Rounded corners
- `hover:scale-105`: Grows element on hover

Example of modifying a feature card:
```html
<!-- Original -->
<div class="bg-gray-800 rounded-2xl p-8 shadow-lg hover:shadow-xl">

<!-- To make it lighter with more padding -->
<div class="bg-gray-700 rounded-2xl p-10 shadow-lg hover:shadow-xl">
```

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. For internal sections, use `#section-id`
3. For external links, use full URL: `https://example.com`

### Call-to-Action Button
The main CTA button appears multiple times:

```html
<!-- Find and update all instances of this URL -->
<a href="https://bestaitoolsforwritingcontent.com" class="inline-block px-8 py-4 bg-blue-600 hover:bg-blue-700 rounded-full">
```

Replace the URL with your desired destination.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` with proper paths:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly
   - Example: `href="#features"` must match `id="features"`
   - Check for typos in both the link and section ID

2. **Responsive Design Issues**
   - Check mobile classes (default)
   - Check medium screen classes (start with `md:`)
   - Check large screen classes (start with `lg:`)

3. **Animation Not Working**
   - Verify AOS script is loaded
   - Check data-aos attributes
   - Make sure AOS is initialized:
```html
<script>
    AOS.init({
        duration: 1000,
        once: true
    });
</script>
```

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all files are in the correct location
3. Ensure all URLs are correctly formatted
4. Test the page in multiple browsers

Remember to always backup your files before making changes, and test your modifications in multiple browsers and screen sizes.