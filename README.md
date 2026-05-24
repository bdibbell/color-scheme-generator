# Algorithmic Theme Generator

An interactive, browser-based tool for generating mathematically-derived,
Solarized-inspired color schemes using **LCH (Lightness, Chroma, Hue)** color logic.

**[Live Demo](https://bdibbell.github.io/theme-generator/)**

## Overview

Traditional color scheme generation often relies on HSL (Hue, Saturation, Lightness),
which is computationally simple but perceptually inconsistent. This tool uses the
**LCH color space** to ensure that color steps are perceptually uniform.

The generator follows the "architecture" of the Solarized color palette, but
allows for powerful control over the base hue, contrast emphasis, saturation, and global
luminance. Using the tool, you can create a "solarized look" using your preferred base hue, or tweak the contrast/brightness of Solarized itself - entirely up to you!

## Features

- **Perceptual Uniformity:** Built on LCH logic to maintain consistent readability
across the entire color spectrum.
- **Dynamic Controls:**
  - **Base Hue:** Shift the entire theme's base color while maintaining structural
relationships. In other words, make Solarized but green, purple, red, whatever!
  - **Contrast Emphasis:** Scale the distance between background and foreground tones
for your preferred contrast ratio, balancing visibility and comfort.
  - **Saturation (Chroma):** Adjust from muted colors to intense.
  - **Luminance Scale:** Globally shift the brightness of the theme.
- **Developer-Focused Exports:**
  - **Copy JSON:** Get a structured object of all colors for easy integration into
custom scripts.
  - **iTerm2 Export:** One-click download of `.itermcolors` files.
  - **Multi-Format Display:** View and copy colors in **HEX**, **RGB**, or **HSL**.
- **Responsive Mockup:** Real-time syntax highlighting preview to see how your theme
looks in code.
- **Dark/Light Mode:** Seamlessly toggle between dark and light variants of your
generated theme.

## Technical Implementation

- **Canvas Color Resolver:** To overcome browser-specific variations in CSS `lch()`
support, the tool uses a hidden 1x1 canvas to resolve modern CSS color formats into
reliable sRGB values.
- **Dynamic Contrast Detection:** Swatch text colors (Black/White) are calculated
using relative luminance (WCAG standards) to ensure UI readability.
- **Zero Dependencies:** Pure Vanilla JS, HTML, and CSS. No build step, no frameworks,
no bloat.

## How to Use

1. **Set your foundation:** Use the **Base Hue** slider to find your primary color.
2. **Refine the feel:** Open **Advanced Controls** to tweak Contrast, Saturation, and
Luminance.
3. **Check the code:** Use the **Editor Mockup** to verify syntax highlighting
legibility.
4. **Export:** Choose your preferred format and click to copy or download.

## License

This project is released into the public domain under the
[Unlicense](https://unlicense.org/). You are free to copy, modify, publish, use,
compile, sell, or distribute this software, either in source code form or as a
compiled binary, for any purpose, commercial or non-commercial, and by any means.

## Contributions

Contributions are welcome. Any pull requests MUST have a description indicating the problem they are looking to solve. Contributions are permitted to include LLM-generated code, however, you must manually check the code BEFORE opening a pull request, and the code should not infringe on any rights.

---

Built for developers who care about color science and readability.
