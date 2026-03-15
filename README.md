# Bitsy Asset Injector 🎨👾

A lightweight, browser-based utility designed to seamlessly inject custom art (Sprites, Tiles, or Items) directly into Bitsy game files.

## ✨ Features

* **Smart Palette Mapping:** Choose to create a brand new palette for your uploaded asset, or dynamically append new colors to your game's existing `PAL 0` to keep your game data clean and organized.
* **Transparent PNG Support:** Fully supports images with transparent backgrounds. Transparent pixels are automatically assigned to `index 0` (your Bitsy background color), preventing ugly black squares around your sprites.
* **Dynamic Sizing (HD Mod Ready):** Supports standard `8x8` grids as well as `16x16` HD grids. The tool will downscale or format your image to match your chosen grid size.
* **Engine Compatibility:** Designed to output either `DRAW_FORMAT 1` comma-separated values (e.g., `a,0,b,1`) or standard unbroken strings (eg., `010101`), preventing rendering bugs in standard and modified engines.
* **Safe Injection:** Safely parses your `.html` file and appends data without overwriting your game title, version headers, or existing room data.

## 🚀 How to Use

1. **Open the Tool:** Open the `index.html` (or whatever you named the tool) in any modern web browser.
2. **Upload Game Data:** Select your current Bitsy game `.html` file. *(Note: Always keep a backup of your original file!)*
3. **Upload Image:** Select the image you want to convert into a Bitsy asset.
4. **Configure Asset:**
   * **Category:** Choose if it's a Tile (`TIL`), Sprite (`SPR`), or Item (`ITM`).
   * **Size:** Select `8x8` or `16x16` depending on your game's grid.
   * **Palette Mode:** Choose whether to add the extracted colors to your existing `PAL 0` or create a new palette.
   * **Name:** Give your asset a recognizable name (e.g., `magic_tree`).
5. **Inject:** Click **"Inject Asset & Colors"**. The tool will automatically download a new file prefixed with `HD_` containing your injected data.
6. **Play:** Open the newly downloaded `.html` file in your Bitsy editor. Your new asset and colors will be waiting for you in the Paint and Color tabs!

## 🛠️ Built With

* HTML5 / JavaScript
* HTML Canvas API (for pixel data extraction)
