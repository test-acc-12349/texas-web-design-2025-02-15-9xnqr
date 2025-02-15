# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original header text -->
<h1 class="text-2xl font-bold text-blue-600">TWD</h1>
```
To update the company name, simply replace "TWD" with your desired text.

#### Hero Section
```html
<h2 class="text-4xl md:text-6xl font-bold mb-4">Texas Web Design</h2>
<p class="text-xl md:text-2xl mb-8">Best Websites In Texas</p>
```
- Replace "Texas Web Design" with your main heading
- Update "Best Websites In Texas" with your tagline

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow">
    <i class="fas fa-server text-4xl text-blue-600 mb-4"></i>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package</p>
</div>
```
To modify features:
1. Update the icon class (e.g., `fa-server` to `fa-cloud`)
2. Change the heading text
3. Modify the description text

### Tailwind CSS Modifications

#### Color Scheme
The primary color is blue-600. To change the color scheme:
1. Find all instances of `blue-600` and replace with your desired color (e.g., `red-600`)
2. Common color classes used:
   - `bg-blue-600`: Background color
   - `text-blue-600`: Text color
   - `hover:bg-blue-700`: Hover state color

#### Responsive Design
The page uses these breakpoints:
- `md:`: Medium screens (768px and up)
- Default: Mobile screens

Example:
```html
<h2 class="text-4xl md:text-6xl">
```
- `text-4xl`: Mobile size
- `md:text-6xl`: Desktop size

## Fixing Broken Links

### Current Link Structure

#### Navigation Menu
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://twd.com">Get Started</a>
</div>
```

To update links:
1. Internal links (starting with #) connect to section IDs
2. External links need full URLs
3. Replace `https://twd.com` with your actual website URL

#### Footer Links
```html
<ul class="space-y-2">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#faq">FAQ</a></li>
</ul>
```

### Social Media Links
```html
<a href="#" class="text-gray-400 hover:text-white transition-colors">
    <i class="fab fa-facebook"></i>
</a>
```
Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them

Example privacy.html structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header section -->
    
    <main class="container mx-auto px-4 py-24">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your privacy policy content here -->
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check mobile view using browser developer tools
   - Verify `md:` classes are properly set
   - Test all breakpoints

3. **Icon Not Showing**
   - Verify Font Awesome CDN is loaded
   - Check icon class names against Font Awesome documentation
   - Ensure proper prefix (`fas`, `fab`, etc.)

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all CDN links are accessible
3. Test the page in multiple browsers
4. Ensure all HTML tags are properly closed

For additional support, contact the development team at admin@twd.com.