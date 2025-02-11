# Anatome Landing Page - Maintenance Guide

This guide will help you maintain and customize the Anatome landing page. It's written for beginners and provides detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Fixing Navigation Links](#fixing-navigation-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and main navigation. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold">Anatome</div>
```
- Simply replace "Anatome" with your company name
- Adjust text size by changing `text-2xl` to `text-3xl` for larger text

### Hero Section
Located at the top of the page with the main image:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight mb-6">
    Anatome is the scaffolding of life, each piece is unique just like its humans
</h1>
```
- Replace the text between the `<h1>` tags
- `md:text-6xl` makes text larger on desktop screens
- `mb-6` adds bottom margin spacing

2. **Hero Image:**
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
     alt="Hero image" 
     class="w-full h-full object-cover">
```
- Replace the `src` URL with your image path
- Always update the `alt` text to describe your new image

### Features Section
To modify feature cards:

```html
<div class="bg-white p-8 rounded-lg shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-3xl mb-4">🎨</div>
    <h3 class="text-xl font-semibold mb-4">Limited Edition Drops</h3>
    <p class="text-gray-600">Exclusive collections with only 75 pieces per color ever made.</p>
</div>
```
- Replace emoji inside `text-3xl mb-4` div
- Update heading text in `<h3>` tags
- Modify description in `<p>` tags

## Fixing Navigation Links

### Main Navigation
Current navigation links are placeholders:

```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="hover:text-gray-600 transition-colors">Shop</a>
    <a href="#" class="hover:text-gray-600 transition-colors">About</a>
    <a href="#" class="hover:text-gray-600 transition-colors">Contact</a>
</div>
```

To update:
1. Replace `#` with actual page URLs
2. Example:
```html
<a href="/shop.html" class="hover:text-gray-600 transition-colors">Shop</a>
```

### Footer Links
Located at the bottom of the page:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors">Shop</a></li>
    <li><a href="#" class="hover:text-white transition-colors">About</a></li>
    <li><a href="#" class="hover:text-white transition-colors">FAQ</a></li>
</ul>
```

Update these links to match your site structure:
```html
<li><a href="/shop.html" class="hover:text-white transition-colors">Shop</a></li>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Footer Section
Add this code before the copyright notice in the footer:

```html
<div class="mt-8 text-center">
    <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors mr-4">Privacy Policy</a>
    <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a>
</div>
```

### Step 2: Style Consistency
- Uses same `text-gray-400` class as other footer links
- Maintains hover effect with `hover:text-white`
- `mr-4` adds spacing between links

## Troubleshooting

### Common Issues:

1. **Images Not Loading**
   - Check if image URLs are correct
   - Ensure images are uploaded to your server
   - Verify file paths are relative to your HTML file

2. **Responsive Design Issues**
   - Don't remove `md:` prefixed classes - they control desktop layout
   - Keep `container` and `mx-auto` classes for proper centering
   - Maintain the viewport meta tag in the header

3. **Link Problems**
   - Test all links after updating
   - Use complete URLs for external links
   - Use relative paths for internal pages

### CSS Class Reference:
- `container`: Sets maximum width and centers content
- `mx-auto`: Centers elements horizontally
- `px-4`: Adds horizontal padding
- `py-4`: Adds vertical padding
- `text-center`: Centers text
- `md:`: Applies styles only on medium screens and larger

Remember to test all changes on both mobile and desktop screens before publishing updates.