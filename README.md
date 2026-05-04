# 📚 Calibre Offline Library System (Linux Mint + Flatpak)

## What it is
A stable offline system for organizing ebooks, audiobooks, podcasts, and long-form audio using Calibre on Linux Mint with Flatpak.

## Problem it solves
- Calibre crashes during metadata editing on Linux Mint
- Virtual libraries cause confusion instead of separation
- File system becomes cluttered for mixed media (audiobooks, podcasts, talks)
- GPU/Qt conflicts cause segmentation faults

## How it works
- Uses Calibre Flatpak for isolated stability
- Separates content using physical libraries (not virtual filters)
- Uses tags for subcategories (OPSEC, spirituality, fitness, etc.)
- Disables GPU + forces stable Qt rendering
- Grants explicit filesystem access via Flatpak overrides

## Usage
1. Install Calibre via Flatpak
2. Create separate libraries for content types
3. Organize files into dedicated folders
4. Use tags for deeper classification
5. Disable GPU rendering if crashes occur

## Result
A fully offline, structured media library system that replaces messy file-based organization with searchable, tagged, and isolated libraries.
