# Photo-Shoot Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Photo-Shoot landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Location: Inside the header tag -->
<h1 class="text-2xl font-bold">Photo-Shoot</h1>  <!-- Company name -->
```
To modify the company name, simply replace "Photo-Shoot" with your desired text.

#### Hero Section
```html
<h2 class="text-4xl md:text-6xl font-bold mb-6 tracking-tight">Photo-Shoot</h2>
<p class="text-xl md:text-2xl mb-8">Get the ultimate product photography lightbox</p>
```
- Update the main heading by replacing "Photo-Shoot"
- Modify the subheading by changing the text within the `<p>` tag

#### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-lg shadow-lg hover:shadow-xl transition duration-300 transform hover:scale-105">
    <h3 class="text-xl font-bold mb-4">USB Powered</h3>
    <p class="text-gray-600">Connect to any USB port for consistent, reliable power supply.</p>
</div>
```
To update features:
1. Locate the feature cards within the `features` section
2. Modify the `<h3>` text for feature titles
3. Update the `<p>` text for feature descriptions

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Colors: `text-gray-600`, `bg-blue-600`
- Responsive Design: `md:text-6xl` (applies at medium screens)
- Hover Effects: `hover:bg-blue-700`

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Reference Tailwind's documentation for available classes
4. Add or replace classes as needed

Example:
```html
<!-- Original -->
<button class="bg-blue-600 hover:bg-blue-700">

<!-- Modified for red theme -->
<button class="bg-red-600 hover:bg-red-700">
```

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://buy.stripe.com/14k5mM58ObjBbRK000">Buy Now</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For internal links (starting with #), ensure the ID matches your section
3. For external links, replace the full URL

### Buy Now Button Links
The purchase button appears multiple times:
```html
<!-- Example button -->
<a href="https://buy.stripe.com/14k5mM58ObjBbRK000" class="inline-flex items-center...">
```

To update:
1. Search for all instances of the Stripe URL
2. Replace with your new purchase link
3. Test each button to ensure proper functionality

## 3. Linking Privacy and Terms Pages

### Footer Policy Links
Current structure:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-200">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-200">Terms of Service</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-200">Shipping Policy</a></li>
</ul>
```

To add policy pages:
1. Create your policy HTML files (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-200">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-200">Terms of Service</a></li>
```

## Troubleshooting Tips

1. Broken Internal Links
- Ensure section IDs match exactly with href attributes
- IDs are case-sensitive
- Check for extra spaces in IDs

2. Responsive Design Issues
- Test all changes at different screen sizes
- Maintain the `md:` prefix for medium-screen styles
- Don't remove responsive classes unless you're sure about the impact

3. Style Inconsistencies
- Keep the same color classes throughout (e.g., `blue-600`)
- Maintain consistent spacing classes
- Preserve hover effects and transitions

## Need Help?

If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all links are properly formatted
3. Ensure all HTML tags are properly closed
4. Test on multiple browsers
5. Contact technical support at admin@photoshoot.site

Remember to always back up your files before making changes, and test thoroughly after each modification.