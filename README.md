# Design System

A modular, CSS-based design system that provides consistent UI components for your applications.

## Getting Started

### Required Dependencies

Before using the design system, make sure to load these required dependencies:

**Font Family**:
  <link rel="preload" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" as="style">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" rel="stylesheet">

### Examples

Check out the `examples` directory for fully working HTML examples of each component. Each example shows proper usage and different variants of the components.

### Generated Designs

All new designs generated from the design system chat interface will be placed in the root folder for easy access.

## Usage

### Import Order

The design system follows a specific import order, which is handled by the main CSS file:

1. **Design Tokens** - Colors, typography, and variables
2. **Layout** - Basic layout utilities
3. **Components** - UI elements (buttons, inputs, cards, banners etc.)
4. **Assets** - Logos and other assets

You don't need to manage these imports manually - just include the main CSS file, and all components will be available.

### Using Components

Components are available as CSS classes that you can add to your HTML elements.

#### Button Example:

```html
<button class="btn btn-primary btn-medium">
  <span class="btn-text">BUTTON TEXT</span>
</button>
```

#### Button with Icon:

```html
<button class="btn btn-primary btn-medium">
  <div class="btn-icon">
    <i class="fas fa-plus"></i>
  </div>
  <span class="btn-text">BUTTON TEXT</span>
</button>
```

#### Banner Example:

```html
<div class="banner style-variant-warning">
  <div class="icon-container">
    <i class="fas fa-exclamation-triangle"></i>
  </div>
  <div class="content">
    <div class="title body-text-medium">Warning Title</div>
    <div class="text body-text">Warning message text goes here.</div>
  </div>
  <button class="button-close">
    <i class="fas fa-times"></i>
  </button>
</div>
```

## Development

### File Structure

```
design-system/
├── dist/
│   └── design-system.css      # Main CSS file to import
├── tokens/                    # Design tokens
│   ├── colors.css             # Color variables
│   ├── typography.css         # Typography styles
│   └── variables.css          # Spacing, sizing, etc.
├── components/                # UI components
│   ├── buttons.css            # Basic components
│   ├── text-input.css
│   ├── select.css
│   ├── card.css               # Advanced components
│   ├── banner.css
│   └── ...
├── styles/                    # General styles
│   └── layout.css
└── assets/                    # Assets
    └── logo.css
```

### Adding New Components

When creating new components:

1. Place all new design files in the root folder structure
2. Add component CSS files directly in the `components/` directory
3. Update the main CSS file to include your new component:
   ```css
   /* Components */
   @import '../components/your-new-component.css';
   ```