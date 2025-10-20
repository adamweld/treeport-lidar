# Treeport LIDAR Tiles

This repository contains LIDAR map tiles that can be used directly in CalTopo and other mapping applications via GitHub's raw content URLs.

## Usage in CalTopo

To add this tile layer to CalTopo:

1. Go to [CalTopo](https://caltopo.com)
2. Click on the **Map** menu
3. Select **Add Custom Source**
4. Use this URL format:
   ```
   https://raw.githubusercontent.com/adamweld/treeport-lidar/refs/heads/main/tiles/{Z}/{X}/{Y}.png
   ```

The tiles will be loaded directly from GitHub without needing any additional hosting setup.

## Repository Structure

```
treeport-lidar/
├── tiles/           # Map tiles organized as {z}/{x}/{y}.png
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
https://raw.githubusercontent.com/adamweld/treeport-lidar/refs/heads/main/tiles/{z}/{x}/{y}.png
```

Example:
```
https://raw.githubusercontent.com/adamweld/treeport-lidar/refs/heads/main/tiles/12/664/1415.png
```

## Notes

- No GitHub Pages setup required - tiles are served directly from the repository via raw.githubusercontent.com
- Make sure your repository is public for the tiles to be accessible
- GitHub has rate limits for raw content access, suitable for personal use

## License

Please specify your license for this data.
