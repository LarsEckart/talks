# Slidev Styling Guide

This document provides reusable CSS patterns for consistent styling across the presentation slides. Since Slidev uses scoped CSS per slide, these patterns should be copied into individual slide `<style>` blocks as needed.

## Color Palette

```css
/* Primary Colors */
--slide-blue: #2B90B6;
--slide-teal: #2aa198;
--slide-muted: #657b83;
--slide-subtle: #93a1a1;

/* Gradient Colors */
--gradient-start: #4EC5D4;
--gradient-mid: #146b8c;
--gradient-end: #4EC5D4;

/* Background Effects */
--backdrop-bg: rgba(253, 246, 227, 0.2);
--border-color: rgba(42, 161, 152, 0.3);
--shadow-color: rgba(88, 110, 117, 0.3);
```

## Common CSS Patterns

### 1. Standard Title Styling

```css
h1 {
  color: #2B90B6;
  margin-bottom: 2rem;
}
```

### 2. Animated Gradient Title

```css
h1 {
  background: linear-gradient(90deg, #4EC5D4, #146b8c, #4EC5D4);
  background-size: 200% 100%;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: gradientShift 3s ease-in-out infinite;
  margin-bottom: 2rem;
  text-align: center;
  font-weight: 700;
}

@keyframes gradientShift {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}
```

### 3. Centered Image Container

```css
.slide-image-center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 400px;
  margin: 2rem auto;
}

.slide-image-center img {
  max-height: 100%;
  max-width: 100%;
  object-fit: contain;
  border-radius: 8px;
  box-shadow: 0 8px 32px rgba(88, 110, 117, 0.3);
}
```

### 4. Large Image Container (500px height)

```css
.slide-image-center-large {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 500px;
  margin: 2rem auto;
  padding: 2rem;
  width: 100%;
}

.slide-image-center-large img {
  max-height: 100%;
  max-width: 100%;
  object-fit: contain;
  border-radius: 12px;
  box-shadow: 0 8px 32px rgba(88, 110, 117, 0.3);
}
```

### 5. Content Container

```css
.slide-content-container {
  max-width: 700px;
  margin: 0 auto;
  padding: 2rem;
}

/* Wide variant */
.slide-content-container-wide {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
}
```

### 6. Interactive Content Items

```css
.slide-content-item {
  margin: 2rem 0;
  padding: 1.5rem;
  background: rgba(253, 246, 227, 0.2);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
  transform: translateY(0);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.slide-content-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 40px rgba(88, 110, 117, 0.4);
  background: rgba(253, 246, 227, 0.3);
}

.slide-content-item h3 {
  color: #2aa198;
  margin-bottom: 0.8rem;
  font-size: 1.3em;
  font-weight: 600;
}

.slide-content-item p {
  color: #657b83;
  line-height: 1.6;
  margin: 0;
}
```

### 7. Backdrop Content Styling

```css
.slide-backdrop-content {
  background: rgba(253, 246, 227, 0.1);
  border-radius: 12px;
  padding: 2rem;
  margin: 1.5rem 0;
  backdrop-filter: blur(10px);
}

.slide-backdrop-content h3 {
  color: #2aa198;
  margin-bottom: 1rem;
}

.slide-backdrop-content ul {
  color: #657b83;
  margin: 0;
}

.slide-backdrop-content li {
  margin: 0.5rem 0;
  line-height: 1.5;
}
```

## Usage Examples

### Basic Title Slide

```html
<h1>My Slide Title</h1>

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 2rem;
}
</style>
```

### Animated Title with Content Items

```html
<h1>Interactive Content</h1>

<div class="slide-content-container">
  <div class="slide-content-item" v-click>
    <h3>First Point</h3>
    <p>Description of the first point</p>
  </div>
  
  <div class="slide-content-item" v-click>
    <h3>Second Point</h3>
    <p>Description of the second point</p>
  </div>
</div>

<style>
h1 {
  background: linear-gradient(90deg, #4EC5D4, #146b8c, #4EC5D4);
  background-size: 200% 100%;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: gradientShift 3s ease-in-out infinite;
  margin-bottom: 2rem;
  text-align: center;
  font-weight: 700;
}

@keyframes gradientShift {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

.slide-content-container {
  max-width: 700px;
  margin: 0 auto;
  padding: 2rem;
}

.slide-content-item {
  margin: 2rem 0;
  padding: 1.5rem;
  background: rgba(253, 246, 227, 0.2);
  border-radius: 12px;
  border-left: 4px solid #2aa198;
  backdrop-filter: blur(10px);
  transform: translateY(0);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.slide-content-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 40px rgba(88, 110, 117, 0.4);
  background: rgba(253, 246, 227, 0.3);
}

.slide-content-item h3 {
  color: #2aa198;
  margin-bottom: 0.8rem;
  font-size: 1.3em;
  font-weight: 600;
}

.slide-content-item p {
  color: #657b83;
  line-height: 1.6;
  margin: 0;
}
</style>
```

### Image Slide

```html
<h1>Visual Content</h1>

<div class="slide-image-center">
  <img src="/image.png" alt="Description" />
</div>

<style>
h1 {
  color: #2B90B6;
  margin-bottom: 2rem;
}

.slide-image-center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 400px;
  margin: 2rem auto;
}

.slide-image-center img {
  max-height: 100%;
  max-width: 100%;
  object-fit: contain;
  border-radius: 8px;
  box-shadow: 0 8px 32px rgba(88, 110, 117, 0.3);
}
</style>
```

## Design Principles

1. **Consistent Color Scheme**: All slides use the blue-teal gradient palette
2. **Smooth Animations**: 3-second gradient animations with easing
3. **Backdrop Effects**: Subtle blur and transparency for depth
4. **Hover Interactions**: Gentle lift effects on interactive elements  
5. **Typography Hierarchy**: Clear distinction between titles, headings, and body text
6. **Responsive Scaling**: All elements scale appropriately for presentation display

## Why Not Import Shared CSS?

Slidev uses per-slide scoped CSS which doesn't work well with external imports. The `@import '../styles/shared.css'` approach causes build errors. Copy-pasting these patterns ensures compatibility with Slidev's architecture while maintaining consistency.