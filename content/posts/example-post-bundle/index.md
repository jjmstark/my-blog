+++
date = '2025-11-20T16:08:55-05:00'
draft = false
title = 'How to Use Page Bundles'
description = 'A demonstration of Hugo page bundles with images and assets'
tags = ['hugo', 'tutorial', 'page-bundles']
categories = ['Tutorial']
+++

# How to Use Page Bundles

This post demonstrates how page bundles work in Hugo. With page bundles, you can organize your content and assets together in a single folder.

## Benefits of Page Bundles

- **Asset Organization**: Images and files stay with their related content
- **Easy References**: Reference images with just their filename
- **Portability**: Move entire posts easily by moving one folder
- **Clean Structure**: No more hunting for images in separate folders

## File Structure

This post bundle contains:
```
example-post-bundle/
├── index.md          # This content file
└── (any images or assets you add)
```

## Adding Images

To add an image to this post, simply:
1. Copy the image file to this directory
2. Reference it in markdown: `![Alt text](filename.jpg)`

That's it! Hugo will handle the rest.
