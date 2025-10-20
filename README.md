# Treeport LIDAR Tiles

This repository contains LIDAR map tiles hosted via GitHub Pages.

## Live View

Once deployed, your tiles will be viewable at: `https://<your-username>.github.io/treeport-lidar/`

## Setup Instructions

### 1. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings**
3. Navigate to **Pages** in the left sidebar
4. Under **Source**, select **GitHub Actions**

### 2. Push Changes

Push this repository to GitHub:

```bash
git add .
git commit -m "Set up GitHub Pages for LIDAR tiles"
git push origin main
```

### 3. Wait for Deployment

The GitHub Actions workflow will automatically deploy your site. You can monitor the progress:

1. Go to the **Actions** tab in your repository
2. Watch the "Deploy to GitHub Pages" workflow
3. Once complete, your site will be live

## Repository Structure

```
treeport-lidar/
├── tiles/           # Map tiles organized as {z}/{x}/{y}.png
├── index.html       # Interactive map viewer using Leaflet.js
├── .github/
│   └── workflows/
│       └── deploy.yml  # GitHub Pages deployment workflow
└── README.md        # This file
```

## Tile Format

The tiles follow the standard web mapping tile format:
- Path: `tiles/{z}/{x}/{y}.png`
- Where:
  - `z` = zoom level (12-18 in this dataset)
  - `x` = tile column
  - `y` = tile row

## Accessing Individual Tiles

Tiles can be accessed directly via URL:
```
https://<your-username>.github.io/treeport-lidar/tiles/{z}/{x}/{y}.png
```

Example:
```
https://<your-username>.github.io/treeport-lidar/tiles/12/664/1415.png
```

## Local Development

To test locally:

1. Start a local web server in the repository directory:
   ```bash
   python -m http.server 8000
   # or
   npx serve
   ```

2. Open your browser to `http://localhost:8000`

## Technologies Used

- **Leaflet.js** - Interactive mapping library
- **GitHub Pages** - Static site hosting
- **GitHub Actions** - Automated deployment

## License

Please specify your license for this data.
