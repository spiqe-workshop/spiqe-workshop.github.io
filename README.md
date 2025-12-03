# SPIQE Workshop Website

Website for the Workshop on Secure Protocol Implementations in the Quantum Era (SPIQE 2026), co-located with Euro S&P in Lisbon, Portugal, July 6-10, 2026.

## Tech Stack

- **Hugo** v0.152.2 - Static site generator
- **Bootstrap 5.3.3** - CSS framework (local/offline)
- **GitHub Pages** - Hosting with automated deployment via GitHub Actions

## Development

```bash
# Install Hugo (macOS)
brew install hugo

# Run local development server
hugo server

# Build for production
hugo --minify
```

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch. The GitHub Actions workflow builds the Hugo site and publishes it.

## Image Credits

- **Lisbon photo**: Photo by [Ekaterina Boltaga](https://unsplash.com/@shkipp?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/photos/jqkGK3ofxi8?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)

