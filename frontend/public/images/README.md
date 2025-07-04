# Image Requirements and Guidelines

This directory contains optimized images for the application. Follow these guidelines when adding or updating images.

## Directory Structure

```
images/
├── subjects/     # Subject-related images
├── features/     # Feature showcase images
└── hero/         # Hero section images
```

## Image Specifications

### Dimensions
- Hero Images: 1920x1080px
- Feature Images: 800x600px
- Subject Images: 600x400px

### Format
- Photos: JPG format with quality 85-90%
- Graphics/Icons: PNG format with transparency
- All images should be web-optimized

### Responsive Sizes
- Mobile: 100vw
- Tablet: 50vw
- Desktop: 33vw

## Loading Strategy
- Hero and above-the-fold images: Priority loading
- Below-the-fold images: Lazy loading
- Use blur placeholder for better loading experience

## Optimization Guidelines
1. Compress images without visible quality loss
2. Use appropriate image dimensions
3. Implement responsive images with srcset
4. Add descriptive alt text
5. Use modern image formats (WebP with fallback)

## Naming Convention
- Use lowercase letters
- Separate words with hyphens
- Include dimensions in filename (e.g., `math-subject-600x400.jpg`)

## Example Usage
```tsx
<OptimizedImage
  src="/images/subjects/math-subject-600x400.jpg"
  alt="Mathematics subject illustration"
  fill
  quality={85}
  sizes="(max-width: 768px) 100vw, (max-width: 1200px) 50vw, 33vw"
  className="object-cover"
/>
```
