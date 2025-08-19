# jbl design

My personal website published with GitHub Pages.

## Quick Start

```bash
hugo server --buildDrafts
```

Visit `http://localhost:1313`

## Deployment

This site is automatically deployed to GitHub Pages using GitHub Actions. The workflow:

1. Builds the Hugo site on every push to the `main` branch
2. Deploys the built site to GitHub Pages
3. Uses the latest Hugo extended version for building

To deploy manually, you can trigger the workflow from the Actions tab in GitHub.

## Customization

Modify colors in `assets/css/main.css`:

```css
:root {
  --color-bg-primary: #100f0f;
  --color-text-primary: #cecdc3;
  --color-text-muted: #878580;
}
```