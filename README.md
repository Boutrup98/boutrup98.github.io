# Shibui-Inspired Hugo Site

A minimalist Hugo site inspired by the [Shibui theme](https://github.com/ntk148v/shibui) with dark theme and clean typography.

## Features

- **Minimalist Design**: Shibui (渋い) aesthetics
- **Dark Theme**: Custom hex color palette
- **Responsive**: Mobile-optimized layout
- **Zero JavaScript**: Pure CSS solutions
- **Customizable**: CSS variables for easy modification

## Quick Start

```bash
hugo server --buildDrafts
```

Visit `http://localhost:1313`

## Customization

Modify colors in `assets/css/main.css`:

```css
:root {
  --color-bg-primary: #100f0f;
  --color-text-primary: #cecdc3;
  --color-text-muted: #878580;
}
```

## Structure

- `content/` - Site content (posts, projects, about)
- `layouts/` - Custom templates
- `assets/css/main.css` - Optimized stylesheet
- `hugo.toml` - Configuration

## License

MIT 