# Test Product Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your Test Product landing page. This document provides step-by-step instructions for beginners to modify content, links, and styling while preserving the page's design and functionality.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Common Customizations](#common-customizations)
8. [Troubleshooting Guide](#troubleshooting-guide)

---

## Getting Started

### What You'll Need

- A text editor (VS Code, Sublime Text, Notepad++, or even Notepad)
- Basic understanding of HTML tags and structure
- The `index.html` file from this landing page
- Optional: A local server or web hosting to test changes

### File Organization

Organize your project folder like this:

```
project-folder/
├── index.html          (main landing page)
├── privacy.html        (privacy policy page - we'll create this)
├── terms.html          (terms of service page - we'll create this)
├── blog.html           (blog page - linked in footer)
└── README.md           (this file)
```

### How to Open and Edit

1. **Locate your `index.html` file** on your computer
2. **Right-click** on the file
3. **Select "Open with"** and choose your text editor
4. Make changes following the instructions below
5. **Save the file** (Ctrl+S or Cmd+S)
6. **Refresh your browser** to see changes (F5 or Cmd+R)

---

## Understanding the Page Structure

Your landing page is organized into these main sections:

### Section Overview

| Section | Purpose | Location in HTML |
|---------|---------|------------------|
| **Header/Navigation** | Site logo, menu links, mobile menu | Lines 96-140 |
| **Hero Section** | Main headline and call-to-action | Lines 142-206 |
| **Features Section** | Three feature cards with icons | Lines 208-278 |
| **Benefits Section** | Four benefit items with icons | Lines 280-354 |
| **Testimonials Section** | Four customer testimonial cards | Lines 356-463 |
| **About Us Section** | Company information and stats | Lines 465-510 |
| **CTA Section** | Final call-to-action with background | Lines 512-536 |
| **Footer** | Links, social media, copyright | Lines 538-620 |

### Key Concepts for Beginners

**HTML Tags**: Think of these as containers that hold content. Examples:
- `<h1>` = Heading (largest text)
- `<p>` = Paragraph (regular text)
- `<a>` = Link
- `<button>` = Button

**Tailwind CSS Classes**: These are shortcuts that apply styling. Instead of writing complex CSS, you add class names like `text-blue-600` for blue text or `p-8` for padding.

---

## Updating Text Content

### Hero Section - Main Headline

**Location**: Lines 155-161

**Current text**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Unlock Your Potential with <span class="gradient-text">Test Product</span>!
</h1>
```

**How to change it**:

1. Find the text "Unlock Your Potential with Test Product!"
2. Replace it with your own headline
3. **Keep the `<span class="gradient-text">` tags** around the part you want colored with the purple-blue gradient
4. Save and refresh

**Example**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Transform Your Skills with <span class="gradient-text">PowerLearn</span>!
</h1>
```

### Hero Section - Subtitle

**Location**: Lines 163-168

**Current text**:
```html
<p class="text-lg md:text-xl text-gray-700 leading-relaxed max-w-2xl">
    Go beyond the ordinary. Test Product helps you achieve peak performance and discover untapped possibilities within yourself. Transform your capabilities and reach new heights with our revolutionary platform.
</p>
```

**How to change it**:

1. Replace the text between `<p>` and `</p>`
2. Keep the class names exactly as they are
3. Save and refresh

**Example**:
```html
<p class="text-lg md:text-xl text-gray-700 leading-relaxed max-w-2xl">
    Master new skills faster than ever before. PowerLearn adapts to your learning style and keeps you motivated every step of the way.
</p>
```

### Navigation Menu Text

**Location**: Lines 110-117 (Desktop menu)

**Current text**:
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Testimonials</a>
<a href="#about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">About</a>
```

**How to change menu items**:

1. Replace "Features", "Benefits", "Testimonials", "About" with your own menu items
2. **Important**: Keep the `href="#features"` parts the same (these are anchor links)
3. Make the same changes in the mobile menu (Lines 126-131)

**Note**: The `#features`, `#benefits`, etc. are anchor links that jump to sections. Don't change these unless you also change the corresponding section IDs.

### Feature Card Titles and Descriptions

**Location**: Lines 229-244 (Feature 1), Lines 246-261 (Feature 2), Lines 263-278 (Feature 3)

**Current Feature 1**:
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">Personalized Insights</h3>
<p class="text-gray-700 leading-relaxed mb-4">
    Receive AI-powered, data-driven insights uniquely tailored to your individual needs...
</p>
```

**How to change feature titles and descriptions**:

1. Find the `<h3>` tag with the feature title
2. Replace "Personalized Insights" with your feature name
3. Replace the paragraph text below it with your description
4. Repeat for all three features

**Example**:
```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">Smart Analytics</h3>
<p class="text-gray-700 leading-relaxed mb-4">
    Get real-time analytics that show you exactly what's working and what needs improvement.
</p>
```

### Feature Card Bullet Points

**Location**: Lines 240-244 (Feature 1), Lines 257-261 (Feature 2), Lines 274-278 (Feature 3)

**Current bullet points**:
```html
<ul class="space-y-2 text-sm text-gray-600">
    <li class="flex items-center"><i class="fas fa-check text-blue-600 mr-3"></i>Real-time analytics</li>
    <li class="flex items-center"><i class="fas fa-check text-blue-600 mr-3"></i>Behavioral analysis</li>
    <li class="flex items-center"><i class="fas fa-check text-blue-600 mr-3"></i>Custom recommendations</li>
</ul>
```

**How to change bullet points**:

1. Replace "Real-time analytics", "Behavioral analysis", "Custom recommendations" with your own points
2. Keep the `<i class="fas fa-check..."></i>` parts (these are checkmark icons)
3. Keep the `<li>` tags and structure

**Example**:
```html
<ul class="space-y-2 text-sm text-gray-600">
    <li class="flex items-center"><i class="fas fa-check text-blue-600 mr-3"></i>Dashboard overview</li>
    <li class="flex items-center"><i class="fas fa-check text-blue-600 mr-3"></i>Data visualization</li>
    <li class="flex items-center"><i class="fas fa-check text-blue-600 mr-3"></i>Export reports</li>
</ul>
```

### Testimonial Cards

**Location**: Lines 382-408 (Testimonial 1), Lines 410-436 (Testimonial 2), Lines 438-464 (Testimonial 3), Lines 466-492 (Testimonial 4)

**Current testimonial structure**:
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "Test Product completely revolutionized how I approach my daily workflow..."
</p>
<div class="flex items-center">
    <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=48&h=48&fit=crop&crop=faces" alt="Sarah Johnson" class="w-12 h-12 rounded-full mr-4 object-cover">
    <div>
        <p class="font-bold text-gray-900">Sarah Johnson</p>
        <p class="text-sm text-gray-600">Marketing Director, Tech Innovations Inc.</p>
    </div>
</div>
```

**How to change testimonials**:

1. Replace the quote text between the quotation marks
2. Replace the image URL with your own image (or use an Unsplash URL)
3. Replace "Sarah Johnson" with the customer's actual name
4. Replace "Marketing Director, Tech Innovations Inc." with their title and company

**Example**:
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "This platform completely changed how our team works together. We're now 50% more efficient!"
</p>
<div class="flex items-center">
    <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=48&h=48&fit=crop&crop=faces" alt="John Smith" class="w-12 h-12 rounded-full mr-4 object-cover">
    <div>
        <p class="font-bold text-gray-900">John Smith</p>
        <p class="text-sm text-gray-600">Operations Manager, Global Tech Corp</p>
    </div>
</div>
```

### Footer Text

**Location**: Lines 545-555 (Company info), Lines 560-567 (Product links), Lines 569-576 (Resources), Lines 578-585 (Legal & Contact)

**Company description**:
```html
<p class="text-sm leading-relaxed">
    Unlock your potential with our revolutionary platform designed to help you achieve peak performance and discover untapped possibilities.
</p>
```

**How to change it**:

1. Find this text in the footer
2. Replace it with your company description
3. Keep the `<p>` tags and class names

**Footer links example**:
```html
<li><a href="#features" class="hover:text-blue-500 transition-colors duration-300">Features</a></li>
<li><a href="#benefits" class="hover:text-blue-500 transition-colors duration-300">Benefits</a></li>
```

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind Classes

Tailwind CSS uses descriptive class names that control styling. Here are the most common ones on this page:

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-{color}-{number}` | Text color | `text-blue-600` = blue text |
| `bg-{color}-{number}` | Background color | `bg-blue-600` = blue background |
| `text-{size}` | Font size | `text-2xl` = large text |
| `p-{number}` | Padding (space inside) | `p-8` = padding around content |
| `m-{number}` | Margin (space outside) | `m-4` = margin around element |
| `rounded-{size}` | Rounded corners | `rounded-xl` = very rounded |
| `shadow-{size}` | Drop shadow | `shadow-xl` = large shadow |
| `w-{size}` | Width | `w-full` = full width |
| `h-{size}` | Height | `h-12` = height of 12 units |

### Color Palette Reference

Your page uses these colors (from Tailwind):

```
Blues:     blue-50, blue-100, blue-200, blue-400, blue-500, blue-600, blue-700, blue-900
Purples:   purple-50, purple-100, purple-200, purple-500, purple-600, purple-900
Greens:    green-50, green-100, green-200, green-600
Grays:     gray-50, gray-100, gray-200, gray-400, gray-600, gray-700, gray-900
Oranges:   orange-600
```

**Lower numbers** (50, 100) = lighter shades
**Higher numbers** (600, 700, 900) = darker shades

### Changing Button Colors

**Location**: Lines 36-44 (Custom button styles)

**Current primary button**:
```css
.btn-primary {
    @apply bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-8 rounded-lg transition-all duration-300 transform hover:scale-105 hover:shadow-lg;
}
```

**How to change it**:

1. Find `.btn-primary` in the `<style>` section
2. Change `bg-blue-600` to a different color (e.g., `bg-green-600`)
3. Change `hover:bg-blue-700` to the darker version (e.g., `hover:bg-green-700`)
4. Save and refresh

**Example - Change to green**:
```css
.btn-primary {
    @apply bg-green-600 hover:bg-green-700 text-white font-semibold py-3 px-8 rounded-lg transition-all duration-300 transform hover:scale-105 hover:shadow-lg;
}
```

### Changing Feature Card Colors

**Location**: Lines 229-244 (Feature 1 - Blue), Lines 246-261 (Feature 2 - Purple), Lines 263-278 (Feature 3 - Green)

**Current Feature 1 (Blue)**:
```html
<div class="card-hover bg-gradient-to-br from-blue-50 to-blue-100 p-8 rounded-xl border border-blue-200 hover:border-blue-400 cursor-pointer group">
    <div class="bg-blue-600 text-white rounded-lg p-4 w-16 h-16 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
        <i class="fas fa-lightbulb text-2xl"></i>
    </div>
```

**How to change feature card colors**:

1. Find the feature card you want to change
2. Replace `blue-50`, `blue-100`, `blue-200`, `blue-400`, `blue-600` with your chosen color
3. Use the same color family (e.g., all `green-` or all `purple-`)

**Example - Change Feature 1 to Green**:
```html
<div class="card-hover bg-gradient-to-br from-green-50 to-green-100 p-8 rounded-xl border border-green-200 hover:border-green-400 cursor-pointer group">
    <div class="bg-green-600 text-white rounded-lg p-4 w-16 h-16 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
        <i class="fas fa-lightbulb text-2xl"></i>
    </div>
```

### Changing Hero Section Background

**Location**: Lines 142-144

**Current background**:
```html
<section class="relative bg-gradient-to-br from-blue-50 via-white to-purple-50 py-24 md:py-32 lg:py-40 overflow-hidden">
```

**How to change it**:

1. Find `bg-gradient-to-br from-blue-50 via-white to-purple-50`
2. Change the colors:
   - `from-blue-50` = starting color
   - `via-white` = middle color
   - `to-purple-50` = ending color
3. Save and refresh

**Example - Change to green gradient**:
```html
<section class="relative bg-gradient-to-br from-green-50 via-white to-green-50 py-24 md:py-32 lg:py-40 overflow-hidden">
```

### Changing Text Size

**Location**: Throughout the page

**Common text size classes**:
- `text-sm` = small
- `text-base` = normal
- `text-lg` = large
- `text-xl` = extra large
- `text-2xl` = 2x large
- `text-3xl` = 3x large
- `text-4xl` = 4x large

**Example - Make headline smaller**:

Current:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
```

Changed:
```html
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold">
```

### Changing Spacing (Padding & Margins)

**Padding classes** (space inside):
- `p-4` = small padding
- `p-8` = medium padding
- `p-12` = large padding

**Margin classes** (space outside):
- `m-4` = small margin
- `m-8` = medium margin
- `m-12` = large margin

**Example - Increase feature card padding**:

Current:
```html
<div class="card-hover bg-gradient-to-br from-blue-50 to-blue-100 p-8 rounded-xl">
```

Changed:
```html
<div class="card-hover bg-gradient-to-br from-blue-50 to-blue-100 p-12 rounded-xl">
```

### Responsive Design Classes

These classes change styling on different screen sizes:

- `md:` = applies on medium screens and up (tablets)
- `lg:` = applies on large screens and up (desktops)

**Example**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```

This means:
- On phones: `text-4xl` (4x large)
- On tablets: `md:text-5xl` (5x large)
- On desktops: `lg:text-6xl` (6x large)

---

## Fixing and Managing Links

### Understanding Links on This Page

Your landing page has three types of links:

1. **Anchor links** - Jump to sections on the same page (e.g., `#features`)
2. **External links** - Go to outside websites (e.g., `https://example.com`)
3. **Page links** - Go to other pages on your site (e.g., `privacy.html`)

### Finding All Links

Here's a complete list of links that need attention:

| Link Type | Location | Current Value | Purpose |
|-----------|----------|----------------|---------|
| External | Line 119 | `https://example.com` | Desktop "Get Started" button |
| Anchor | Line 111 | `#features` | Features menu link |
| Anchor | Line 112 | `#benefits` | Benefits menu link |
| Anchor | Line 113 | `#testimonials` | Testimonials menu link |
| Anchor | Line 114 | `#about` | About menu link |
| External | Line 123 | `https://example.com` | Mobile "Get Started" button |
| External | Line 173 | `https://example.com` | Hero "Start Your Journey" button |
| External | Line 524 | `https://example.com` | CTA "Start Free Trial" button |
| Page | Line 561 | `blog.html` | Footer Blog link |
| Page | Line 585 | `privacy.html` | Footer Privacy Policy link |
| Page | Line 586 | `terms.html` | Footer Terms of Service link |
| Email | Line 587 | `mailto:test@example.com` | Footer Contact email |

### Updating External Links (Buttons to Sign Up)

These are the most important links to update. They should point to your signup or product page.

**Location 1 - Desktop Header Button (Line 119)**:
```html
<a href="https://example.com" class="btn-primary">Get Started</a>
```

**How to change it**:

1. Find `https://example.com`
2. Replace it with your actual URL (e.g., `https://myproduct.com/signup`)
3. Save and test by clicking the button

**Updated example**:
```html
<a href="https://myproduct.com/signup" class="btn-primary">Get Started</a>
```

**Location 2 - Mobile Menu Button (Line 123)**:
```html
<a href="https://example.com" class="btn-primary text-center">Get Started</a>
```

**Change it the same way**:
```html
<a href="https://myproduct.com/signup" class="btn-primary text-center">Get Started</a>
```

**Location 3 - Hero Section "Start Your Journey" (Line 173)**:
```html
<a href="https://example.com" class="btn-primary text-center">
    <i class="fas fa-play mr-2"></i>Start Your Journey
</a>
```

**Change it**:
```html
<a href="https://myproduct.com/signup" class="btn-primary text-center">
    <i class="fas fa-play mr-2"></i>Start Your Journey
</a>
```

**Location 4 - CTA Section Button (Line 524)**:
```html
<a href="https://example.com" class="bg-white hover:bg-gray-100 text-blue-600 font-bold py-4 px-10 rounded-lg transition-all duration-300 transform hover:scale-105 hover:shadow-lg inline-flex items-center justify-center">
    <i class="fas fa-rocket mr-3"></i>Start Free Trial
</a>
```

**Change it**:
```html
<a href="https://myproduct.com/signup" class="bg-white hover:bg-gray-100 text-blue-600 font-bold py-4 px-10 rounded-lg transition-all duration-300 transform hover:scale-105 hover:shadow-lg inline-flex items-center justify-center">
    <i class="fas fa-rocket mr-3"></i>Start Free Trial
</a>
```

### Updating Email Contact Link

**Location**: Line 587 (Footer)

**Current**:
```html
<li><a href="mailto:test@example.com" class="hover:text-blue-500 transition-colors duration-300">Contact: test@example.com</a></li>
```

**How to change it**:

1. Replace `test@example.com` with your actual email address (both places)
2. Keep `mailto:` at the beginning

**Example**:
```html
<li><a href="mailto:support@mycompany.com" class="hover:text-blue-500 transition-colors duration-300">Contact: support@mycompany.com</a></li>
```

### Updating Footer Links

**Location**: Lines 560-587 (Footer navigation)

The footer has links to other pages. If you're creating new pages, update these:

**Current footer links**:
```html
<!-- Product Links -->
<li><a href="#features" class="hover:text-blue-500 transition-colors duration-300">Features</a></li>
<li><a href="#benefits" class="hover:text-blue-500 transition-colors duration-300">Benefits</a></li>
<li><a href="#testimonials" class="hover:text-blue-500 transition-colors duration-300">Testimonials</a></li>
<li><a href="#about" class="hover:text-blue-500 transition-colors duration-300">About Us</a></li>
<li><a href="https://example.com" class="hover:text-blue-500 transition-colors duration-300">Pricing</a></li>

<!-- Resources -->
<li><a href="blog.html" class="hover:text-blue-500 transition-colors duration-300">Blog</a></li>
<li><a href="#" class="hover:text-blue-500 transition-colors duration-300">Documentation</a></li>
<li><a href="#" class="hover:text-blue-500 transition-colors duration-300">Support Center</a></li>
<li><a href="#" class="hover:text-blue-500 transition-colors duration-300">API Reference</a></li>

<!-- Legal & Contact -->
<li><a href="privacy.html" class="hover:text-blue-500 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-500 transition-colors duration-300">Terms of Service</a></li>
<li><a href="#" class="hover:text-blue-500 transition-colors duration-300">Cookie Policy</a></li>
<li><a href="mailto:test@example.com" class="hover:text-blue-500 transition-colors duration-300">Contact: test@example.com</a></li>
```

**How to update footer links**:

1. **Pricing link** (Line 566): Change `https://example.com` to your pricing page URL
2. **Blog link** (Line 570): Keep as `blog.html` if you have a blog page
3. **Documentation link** (Line 571): Change `#` to your documentation URL
4. **Support Center link** (Line 572): Change `#` to your support page URL
5. **API Reference link** (Line 573): Change `#` to your API docs URL
6. **Privacy Policy link** (Line 576): Keep as `privacy.html` (we'll create this)
7. **Terms of Service link** (Line 577): Keep as `terms.html` (we'll create this)
8. **Cookie Policy link** (Line 578): Change `#` to your cookie policy URL or create a new page
9. **Contact email** (Line 579): Change `test@example.com` to your email

**Example - Updated footer**:
```html
<li><a href="https://myproduct.com/pricing" class="hover:text-blue-500 transition-colors duration-300">Pricing</a></li>
<li><a href="blog.html" class="hover:text-blue-500 transition-colors duration-300">Blog</a></li>
<li><a href="https://docs.myproduct.com" class="hover:text-blue-500 transition-colors duration-300">Documentation</a></li>
<li><a href="https://support.myproduct.com" class="hover:text-blue-500 transition-colors duration-300">Support Center</a></li>
<li><a href="https://api.myproduct.com" class="hover:text-blue-500 transition-colors duration-300">API Reference</a></li>
<li><a href="privacy.html" class="hover:text-blue-500 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-500 transition-colors duration-300">Terms of Service</a></li>
<li><a href="cookies.html" class="hover:text-blue-500 transition-colors duration-300">Cookie Policy</a></li>
<li><a href="mailto:support@mycompany.com" class="hover:text-blue-500 transition-colors duration-300">Contact: support@mycompany.com</a></li>
```

### Testing Links

After updating links, test them:

1. **Save your file** (Ctrl+S or Cmd+S)
2. **Refresh your browser** (F5 or Cmd+R)
3. **Click each button and link** to make sure they work
4. **Check both desktop and mobile** versions
5. **External links** should open in a new tab (good practice)

### Making Links Open in New Tab

To make any link open in a new tab, add `target="_blank"`:

**Before**:
```html
<a href="https://example.com" class="btn-primary">Get Started</a>
```

**After**:
```html
<a href="https://example.com" target="_blank" class="btn-primary">Get Started</a>
```

---

## Adding Privacy and Terms Pages

### Why You Need These Pages

- **Legal requirement**: Most countries require privacy policies and terms of service
- **Trust**: Shows users you take their data seriously
- **Linked from footer**: Your current footer links to `privacy.html` and `terms.html`

### Creating the Privacy Policy Page

**Step 1: Create a new file**

1. Open your text editor
2. Click "File" → "New File"
3. Save it as `privacy.html` in the same folder as `index.html`

**Step 2: Add the basic HTML structure**

Copy this template and paste it into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Test Product">
    <meta name="author" content="Test Product">
    <title>Privacy Policy - Test Product</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <a href="index.html" class="text-3xl font-bold gradient-text">
                    <i class="fas fa-rocket"></i> Test Product
                </a>
            </div>
            <div class="flex items-center space-x-4">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Back to Home</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-gradient-to-br from-blue-50 via-white to-purple-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">
                Privacy <span class="gradient-text">Policy</span>
            </h1>

            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <p class="text-lg leading-relaxed">
                    <strong>Last Updated: January 2025</strong>
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Introduction</h2>
                <p>
                    Test Product ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li><strong>Personal Data:</strong> Name, email address, phone number, and other contact information you provide</li>
                    <li><strong>Usage Data:</strong> Information about how you interact with our services</li>
                    <li><strong>Device Information:</strong> Browser type, IP address, and device identifiers</li>
                    <li><strong>Cookies:</strong> Small files stored on your device to enhance your experience</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. How We Use Your Information</h2>
                <p>
                    We use the information we collect in the following ways:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>To provide and maintain our services</li>
                    <li>To notify you about changes to our services</li>
                    <li>To allow you to participate in interactive features</li>
                    <li>To provide customer support</li>
                    <li>To gather analysis or valuable information so we can improve our services</li>
                    <li>To monitor the usage of our services</li>
                    <li>To detect, prevent and address technical and security issues</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Disclosure of Your Information</h2>
                <p>
                    We may share your information in the following situations:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li><strong>By Law or to Protect Rights:</strong> If required by law or if we have a good faith belief that disclosure is necessary</li>
                    <li><strong>Third-Party Service Providers:</strong> We may share your information with vendors, consultants, and other service providers</li>
                    <li><strong>Business Transfers:</strong> We may share or transfer your information in connection with a merger, sale, or acquisition</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or electronic storage is completely secure, and we cannot guarantee absolute security.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Your Rights</h2>
                <p>
                    Depending on your location, you may have the following rights:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>The right to access your personal data</li>
                    <li>The right to correct inaccurate data</li>
                    <li>The right to request deletion of your data</li>
                    <li>The right to opt-out of marketing communications</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">7. Contact Us</h2>
                <p>
                    If you have questions about this Privacy Policy, please contact us at:
                </p>
                <p>
                    <strong>Test Product</strong><br>
                    Email: <a href="mailto:privacy@example.com" class="text-blue-600 hover:text-blue-700">privacy@example.com</a><br>
                    Website: <a href="index.html" class="text-blue-600 hover:text-blue-700">www.testproduct.com</a>
                </p>

                <p class="text-sm text-gray-600 mt-12 pt-8 border-t border-gray-200">
                    This Privacy Policy is effective as of January 2025 and will remain in effect except with respect to any changes in its provisions in the future, which will be in effect immediately after being posted on this page.
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center border-t border-gray-800 pt-8">
                <p>&copy; 2025 Test Product. All rights reserved.</p>
                <p class="mt-2">
                    <a href="index.html" class="hover:text-blue-500 transition-colors duration-300">Home</a> | 
                    <a href="privacy.html" class="hover:text-blue-500 transition-colors duration-300">Privacy Policy</a> | 
                    <a href="terms.html" class="hover:text-blue-500 transition-colors duration-300">Terms of Service</a>
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the privacy policy**

Replace these placeholder items with your actual information:

- **Email address**: Change `privacy@example.com` to your real email
- **Website URL**: Change `www.testproduct.com` to your actual website
- **Company name**: Replace "Test Product" with your company name
- **Last Updated date**: Update to today's date
- **Content**: Modify the policy text to match your actual practices

### Creating the Terms of Service Page

**Step 1: Create a new file**

1. Open your text editor
2. Click "File" → "New File"
3. Save it as `terms.html` in the same folder as `index.html`

**Step 2: Add the basic HTML structure**

Copy this template and paste it into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Test Product">
    <meta name="author" content="Test Product">
    <title>Terms of Service - Test Product</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <a href="index.html" class="text-3xl font-bold gradient-text">
                    <i class="fas fa-rocket"></i> Test Product
                </a>
            </div>
            <div class="flex items-center space-x-4">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Back to Home</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 bg-gradient-to-br from-blue-50 via-white to-purple-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">
                Terms of <span class="gradient-text">Service</span>
            </h1>

            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <p class="text-lg leading-relaxed">
                    <strong>Last Updated: January 2025</strong>
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website and services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on Test Product's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Disclaimer</h2>
                <p>
                    The materials on Test Product's website are provided on an 'as is' basis. Test Product makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Limitations</h2>
                <p>
                    In no event shall Test Product or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Test Product's website, even if Test Product or an authorized representative has been notified orally or in writing of the possibility of such damage.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Test Product's website could include technical, typographical, or photographic errors. Test Product does not warrant that any of the materials on its website are accurate, complete, or current. Test Product may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Links</h2>
                <p>
                    Test Product has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Test Product of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">7. Modifications</h2>
                <p>
                    Test Product may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of [Your Country/State] and you irrevocably submit to the exclusive jurisdiction of the courts located in that location.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">9. Contact Us</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p>
                    <strong>Test Product</strong><br>
                    Email: <a href="mailto:legal@example.com" class="text-blue-600 hover:text-blue-700">legal@example.com</a><br>
                    Website: <a href="index.html" class="text-blue-600 hover:text-blue-700">www.testproduct.com</a>
                </p>

                <p class="text-sm text-gray-600 mt-12 pt-8 border-t border-gray-200">
                    These Terms of Service are effective as of January 2025 and will remain in effect except with respect to any changes in its provisions in the future, which will be in effect immediately after being posted on this page.
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center border-t border-gray-800 pt-8">
                <p>&copy; 2025 Test Product. All rights reserved.</p>
                <p class="mt-2">
                    <a href="index.html" class="hover:text-blue-500 transition-colors duration-300">Home</a> | 
                    <a href="privacy.html" class="hover:text-blue-500 transition-colors duration-300">Privacy Policy</a> | 
                    <a href="terms.html" class="hover:text-blue-500 transition-colors duration-300">Terms of Service</a>
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the terms of service**

Replace these placeholder items with your actual information:

- **Email address**: Change `legal@example.com` to your real email
- **Website URL**: Change `www.testproduct.com` to your actual website
- **Company name**: Replace "Test Product" with your company name
- **Location**: Change `[Your Country/State]` in section 8 to your actual location
- **Last Updated date**: Update to today's date
- **Content**: Modify the terms to match your actual policies

### Verifying the Links Work

**Step 1: Check your file structure**

Make sure you have these three files in the same folder:
```
project-folder/
├── index.html
├── privacy.html
├── terms.html
```

**Step 2: Test the links**

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - it should take you to `privacy.html`
4. Click on "Terms of Service" - it should take you to `terms.html`
5. On those pages, click "Back to Home" to return to `index.html`

**Step 3: Verify the footer links work**

On the privacy and terms pages, the footer should have links to all three pages that work correctly.

---

## Common Customizations

### Changing the Logo and Branding

**Location**: Line 108 (Header logo)

**Current**:
```html
<div class="text-3xl font-bold gradient-text">
    <i class="fas fa-rocket"></i> Test Product
</div>
```

**How to change it**:

1. Replace `<i class="fas fa-rocket"></i>` with a different icon
2. Replace "Test Product" with your company name

**Available icons** (from Font Awesome):
- `fa-rocket` = Rocket
- `fa-star` = Star
- `fa-bolt` = Lightning bolt
- `fa-fire` = Fire
- `fa-crown` = Crown
- `fa-diamond` = Diamond
- `fa-trophy` = Trophy
- `fa-target` = Target

**Example - Change to star and new name**:
```html
<div class="text-3xl font-bold gradient-text">
    <i class="fas fa-star"></i> PowerLearn
</div>
```

### Adding a Logo Image Instead of Text

If you have a logo file (PNG, JPG, etc.), you can use it instead of text:

```html
<div class="flex items-center space-x-2">
    <img src="logo.png" alt="Company Logo" class="h-10 w-10">
    <span class="text-2xl font-bold gradient-text">Your Company Name</span>
</div>
```

**Note**: Place your `logo.png` file in the same folder as `index.html`

### Changing the Gradient Color

The gradient colors appear in multiple places. The main gradient is defined in the CSS:

**Location**: Lines 31-37

**Current gradient**:
```css
.gradient-text {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
```

**How to change it**:

The gradient uses hex color codes:
- `#667eea` = Blue-purple
- `#764ba2` = Purple

Replace these with your own colors:

**Example - Change to green to orange**:
```css
.gradient-text {
    background: linear-gradient(135deg, #10b981 0%, #f97316 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
```

**Common hex color codes**:
- Blue: `#3b82f6`
- Green: `#10b981`
- Purple: `#a855f7`
- Orange: `#f97316`
- Red: `#ef4444`
- Pink: `#ec4899`

### Changing the Hero Section Image

**Location**: Line 203

**Current**:
```html
<img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=600&fit=crop" alt="Test Product Dashboard" class="relative rounded-2xl shadow-2xl w-full h-auto">
```

**How to change it**:

1. Go to [Unsplash.com](https://unsplash.com) or [Pexels.com](https://pexels.com)
2. Search for an image related to your product
3. Copy the image URL
4. Replace the current URL with your new URL

**Example**:
```html
<img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=600&fit=crop" alt="Your Product Image" class="relative rounded-2xl shadow-2xl w-full h-auto">
```

### Adding or Removing Sections

To remove a section (e.g., Testimonials), find the section tags and delete everything between them:

**Find**:
```html
<!-- Testimonials Section -->
<section id="testimonials" class="py-24 md:py-32 bg-white">
    ... all the testimonial content ...
</section>
```

**Delete** the entire section including the opening `<section>` and closing `</section>` tags.

**Note**: Also update the navigation menu to remove the link to that section.

### Changing Section Backgrounds

Each section has a background color. To change it:

**Current example (Benefits section)**:
```html
<section id="benefits" class="py-24 md:py-32 bg-gradient-to-br from-gray-50 to-gray-100">
```

**Change the background**:
- `bg-white` = White background
- `bg-gray-50` = Light gray background
- `bg-blue-50` = Light blue background
- `bg-gradient-to-br from-gray-50 to-gray-100` = Gradient from light gray to medium gray

**Example - Change to white**:
```html
<section id="benefits" class="py-24 md:py-32 bg-white">
```

### Adding Social Media Links

**Location**: Lines 549-558 (Footer social links)

**Current**:
```html
<a href="#" class="text-gray-400 hover:text-blue-500 transition-colors duration-300 text-lg">
    <i class="fab fa-facebook"></i>
</a>
```

**How to change it**:

1. Replace `#` with your actual social media URL
2. Keep the icon class (e.g., `fab fa-facebook`)

**Example - Add your Facebook page**:
```html
<a href="https://facebook.com/yourpage" class="text-gray-400 hover:text-blue-500 transition-colors duration-300 text-lg">
    <i class="fab fa-facebook"></i>
</a>
```

**Available social media icons**:
- `fab fa-facebook` = Facebook
- `fab fa-twitter` = Twitter
- `fab fa-linkedin` = LinkedIn
- `fab fa-instagram` = Instagram
- `fab fa-youtube` = YouTube
- `fab fa-github` = GitHub
- `fab fa-tiktok` = TikTok

### Changing Font Sizes

**Heading sizes**:
- `text-2xl` = Small heading
- `text-3xl` = Medium heading
- `text-4xl` = Large heading
- `text-5xl` = Extra large heading
- `text-6xl` = Massive heading

**Body text sizes**:
- `text-sm` = Small text
- `text-base` = Normal text
- `text-lg` = Large text
- `text-xl` = Extra large text

**Example - Make hero heading smaller**:

Current:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
```

Changed:
```html
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold">
```

---

## Troubleshooting Guide

### Problem: Links Don't Work

**Symptoms**: Clicking a button or link does nothing or shows an error

**Solutions**:

1. **Check the URL format**
   - External links should start with `https://` (e.g., `https://example.com`)
   - Page links should have the filename (e.g., `privacy.html`)
   - Anchor links should start with `#` (e.g., `#features`)

2. **Verify file names**
   - Make sure `privacy.html` and `terms.html` are spelled exactly right
   - File names are case-sensitive on some systems

3. **Check file location**
   - All HTML files should be in the same folder
   - If files are in subfolders, use the correct path (e.g., `pages/privacy.html`)

4. **Test in browser**
   - Right-click the link and select "Inspect" to see the actual href value
   - Make sure there are no typos

### Problem: Text Changes Don't Appear

**Symptoms**: You edited text but the website still shows the old content

**Solutions**:

1. **Save your file**
   - Make sure you pressed Ctrl+S (Windows) or Cmd+S (Mac)
   - Look for an asterisk (*) next to the filename in your editor - it means unsaved changes

2. **Refresh the browser**
   - Press F5 or Ctrl+R (Windows)
   - Press Cmd+R (Mac)
   - Try hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)

3. **Clear browser cache**
   - This forces the browser to reload the latest version
   - Instructions vary by browser (check your browser's help menu)

4. **Check for typos**
   - Make sure you're editing the right file (`index.html`)
   - Verify you're in the correct section

### Problem: Styling Looks Wrong

**Symptoms**: Colors, spacing, or layout looks broken

**Solutions**:

1. **Don't delete class names**
   - Each class name controls specific styling
   - If you remove a class, that styling disappears
   - Always keep the full class attribute

2. **Check for typos in class names**
   - `text-blue-600` ✓ Correct
   - `text-blue-60` ✗ Wrong (should be 600)
   - `text-blue600` ✗ Wrong (missing hyphen)

3. **Use valid Tailwind classes**
   - Check the Tailwind documentation for valid class names
   - Common mistake: `text-color-red` should be `text-red-600`

4. **Keep class names together**
   - Don't add spaces or line breaks inside the class attribute
   - Wrong: `class="text-blue-600 p-8 rounded-lg"`
   - Right: `class="text-blue-600 p-8 rounded-lg"`

### Problem: Mobile Menu Doesn't Work

**Symptoms**: Mobile menu button doesn't open/close the menu

**Solutions**:

1. **Check the JavaScript**
   - Make sure you didn't accidentally delete the `<script>` section at the end
   - The script should be between `<!-- JavaScript -->` and `</body>`

2. **Verify button HTML**
   - The mobile menu button should have class `mobile-menu-button`
   - The mobile menu should have class `mobile-menu`
   - These classes are referenced in the JavaScript

3. **Test on actual mobile device**
   - Resize your browser window to simulate mobile
   - Or test on a real phone

### Problem: Images Don't Display

**Symptoms**: Image placeholders appear instead of actual images

**Solutions**:

1. **Check the image URL**
   - If using Unsplash URLs, make sure they're complete
   - If using local images, make sure the filename is correct
   - Image files should be in the same folder as `index.html`

2. **Verify file format**
   - Supported formats: `.jpg`, `.jpeg`, `.png`, `.gif`, `.webp`
   - Check the file extension is correct

3. **Check file permissions**
   - Make sure the image file isn't read-only
   - Try moving the image file to the project folder

4. **Use correct path**
   - Same folder: `<img src="image.png">`
   - Subfolder: `<img src="images/image.png">`
   - URL: `<img src="https://example.com/image.png">`

### Problem: Buttons Look Wrong or Don't Work

**Symptoms**: Buttons appear broken or don't respond to clicks

**Solutions**:

1. **Check button type**
   - Links should use `<a>` tags: `<a href="...">Button Text</a>`
   - Buttons should use `<button>` tags: `<button>Button Text</button>`

2. **Verify href attribute**
   - Make sure the `href` attribute exists and has a valid URL
   - Wrong: `<a class="btn-primary">Click me</a>`
   - Right: `<a href="https://example.com" class="btn-primary">Click me</a>`

3. **Check class names**
   - Buttons should have `btn-primary` or `btn-secondary` class
   - Make sure these classes are defined in the `<style>` section

4. **Test clicking**
   - Try right-clicking and selecting "Inspect Element"
   - Look for any JavaScript errors in the browser console

### Problem: Page Looks Different on Mobile

**Symptoms**: Layout breaks on phone screens

**Solutions**:

1. **Check responsive classes**
   - Classes like `md:` and `lg:` control mobile/tablet/desktop views
   - Make sure you didn't remove these classes

2. **Test on actual device**
   - Use Chrome DevTools to simulate mobile (F12, then click device icon)
   - Or test on a real phone

3. **Check viewport meta tag**
   - Make sure this line exists in the `<head>` section:
   - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
   - If missing, add it back

4. **Verify Tailwind CSS is loaded**
   - Make sure this line exists in the `<head>`:
   - `<script src="https://cdn.tailwindcss.com"></script>`
   - If missing, add it back

### Problem: Gradient Text Doesn't Show

**Symptoms**: Text appears invisible or wrong color

**Solutions**:

1. **Check the gradient-text class**
   - Make sure the `.gradient-text` CSS is defined in the `<style>` section
   - Verify the color values are correct

2. **Verify the HTML structure**
   - Gradient text should be wrapped in a `<span>`:
   - `<span class="gradient-text">Your Text</span>`

3. **Check for conflicting classes**
   - Don't mix gradient-text with other text color classes
   - Wrong: `<span class="gradient-text text-blue-600">Text</span>`
   - Right: `<span class="gradient-text">Text</span>`

### Problem: Footer Links Point to Wrong Pages

**Symptoms**: Clicking footer links goes to wrong page or 404 error

**Solutions**:

1. **Verify file names**
   - Privacy page should be named `privacy.html` (not `privacy-policy.html`)
   - Terms page should be named `terms.html` (not `terms-of-service.html`)

2. **Check file location**
   - All files should be in the same folder
   - If in subfolders, update the href path

3. **Update all footer links**
   - Check all three footer sections have correct hrefs
   - Search for `privacy.html` and `terms.html` to find all instances

4. **Test each link**
   - Click every footer link to make sure they work
   - Test on both desktop and mobile

### Getting Help

If you're still stuck:

1. **Check the browser console**
   - Press F12 to open Developer Tools
   - Look for red error messages
   - These often indicate what's wrong

2. **Compare with the original**
   - If something broke, compare your version with the original
   - Look for missing tags or class names

3. **Validate your HTML**
   - Use [W3C Validator](https://validator.w3.org/)
   - Upload your HTML file to check for errors

4. **Search for solutions**
   - Copy error messages into Google
   - Check Stack Overflow for similar issues

---

## Best Practices for Maintenance

### Regular Maintenance Tasks

**Monthly**:
- Check all links still work
- Verify testimonials are current
- Update statistics (active users, ratings, etc.)
- Review and update content

**Quarterly**:
- Update privacy policy if needed
- Review terms of service
- Check for broken images
- Update company information

**Annually**:
- Review entire page design
- Update copyright year in footer
- Refresh testimonials
- Consider design improvements

### File Backup

Always keep backups of your files:

1. **Create a backup folder**
   ```
   project-folder/
   ├── index.html
   ├── privacy.html
   ├── terms.html
   ├── backups/
   │   ├── index-backup-2025-01.html
   │   ├── privacy-backup-2025-01.html
   │   └── terms-backup-2025-01.html
   ```

2. **Use version control (Git)**
   - Track changes over time
   - Easy to revert if something breaks
   - Learn Git basics from [GitHub](https://github.com)

### Performance Tips

1. **Optimize images**
   - Use compressed images
   - Use appropriate sizes
   - Consider using WebP format

2. **Minimize CSS**
   - Tailwind CSS is already optimized
   - Don't add unnecessary classes

3. **Test page speed**
   - Use Google PageSpeed Insights
   - Aim for score above 90

### Accessibility

Make sure your site is accessible to everyone:

1. **Alt text for images**
   - Every image should have descriptive alt text
   - Example: `alt="Dashboard showing analytics charts"`

2. **Color contrast**
   - Text should be readable on background
   - Use dark text on light backgrounds

3. **Keyboard navigation**
   - Users should be able to navigate with Tab key
   - All links and buttons should be keyboard accessible

---

## Summary

You now have a complete guide to maintaining and customizing your Test Product landing page. Here's a quick reference:

### Quick Links to Common Tasks

| Task | Section | Key Steps |
|------|---------|-----------|
| Change headline | [Updating Text Content](#hero-section---main-headline) | Find `<h1>`, replace text |
| Change button colors | [Modifying Tailwind CSS Classes](#changing-button-colors) | Edit `.btn-primary` in `<style>` |
| Fix signup links | [Fixing and Managing Links](#updating-external-links-buttons-to-sign-up) | Replace all `https://example.com` URLs |
| Add privacy page | [Adding Privacy and Terms Pages](#creating-the-privacy-policy-page) | Create `privacy.html` file |
| Add terms page | [Adding Privacy and Terms Pages](#creating-the-terms-of-service-page) | Create `terms.html` file |
| Change colors | [Modifying Tailwind CSS Classes](#understanding-tailwind-classes) | Replace color class names |
| Change logo | [Changing the Logo and Branding](#changing-the-logo-and-branding) | Replace icon or add image |
| Fix broken links | [Troubleshooting Guide](#problem-links-dont-work) | Check URLs and file names |

### Key Files to Remember

- `index.html` = Main landing page
- `privacy.html` = Privacy policy page (create this)
- `terms.html` = Terms of service page (create this)
- `<style>` section = CSS styling
- `<script>` section = JavaScript functionality

### Remember

- Always save your file after making changes
- Always refresh your browser to see changes
- Keep backups of your files
- Test all links and buttons
- Check both desktop and mobile versions
- When in doubt, compare with the original

Good luck with your landing page! Feel free to reference this guide whenever you need to make updates or customizations.