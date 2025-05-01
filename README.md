# Hong Paris Landing Page - Maintenance Guide

This guide will help you maintain and customize the Hong Paris landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-gray-800">Hong Paris</a>
```
Replace "Hong Paris" with your company name. The classes `text-2xl` controls size, and `font-bold` controls weight.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <!-- Other menu items -->
</div>
```
- Change text between `<a>` tags to update menu items
- `hidden md:flex` means the menu is hidden on mobile and visible on medium screens
- `space-x-8` adds spacing between items

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">Best Websites In Hong Paris</h1>
<p class="text-xl md:text-2xl text-gray-600">{hero_statement}</p>
```
- Replace the h1 text with your main headline
- Replace `{hero_statement}` with your subheading
- Text sizes are responsive: `text-4xl` on mobile, `text-5xl` on medium screens, `text-6xl` on large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">Your feature description</p>
</div>
```
To modify:
1. Change the h3 text for the feature title
2. Update the paragraph text for the description
3. Keep the existing classes to maintain styling

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Change the `href` value to match your section IDs
2. For external links, use complete URLs: `href="https://example.com"`
3. For internal page links, use relative paths: `href="/about.html"`

### Call-to-Action Buttons
The page contains several CTA buttons:
```html
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white">
```
Replace `https://sigmaseo.io` with your desired URL.

### Footer Links
The footer contains multiple link sections:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white">Web Design</a></li>
    <!-- Other links -->
</ul>
```
Replace the `#` placeholder with actual URLs for each service or page.

## Adding Privacy and Terms Pages

### Step 1: Locate Footer Links
Find the Legal section in the footer:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Step 2: Update Link Paths
Replace the `#` with paths to your policy pages:
```html
<li><a href="/privacy.html" class="hover:text-white">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white">Terms of Service</a></li>
```

### Step 3: Create Policy Pages
Create `privacy.html` and `terms.html` in your root directory using the same styling classes for consistency.

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in URLs
   - Ensure files exist in the specified directory
   - Test all links after updating

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the `container` class on main sections
   - Maintain the existing responsive grid structure

3. **Style Inconsistencies**
   - Copy existing Tailwind classes when adding new elements
   - Use the same color classes (`text-gray-600`, `bg-blue-600`, etc.)
   - Maintain spacing patterns using `mb-4`, `py-24`, etc.

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making changes, and test on multiple devices after updates.