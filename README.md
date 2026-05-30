# Fashion Trend Analysis

## Overview

This project looks at runway fashion trends from Spring/Summer 2025 collections using computer vision techniques.

I collected runway images from NowFashion, separated clothing areas from the background using segmentation models, and extracted dominant clothing colors with K-Means clustering. The goal was to see whether computer vision could help summarize visual fashion trends across many designer collections.

---

## Dataset

The runway collection links and images were collected from:

- NowFashion Spring/Summer 2025 Ready-to-Wear collections

The dataset includes over 230 runway collections from different designer brands. Due to dataset size limitations, the raw image files are not included in this repository.

Project structure:

```
FashionDataset/
│
├── fashion_runway_cv_project.ipynb
├── designer_collections.csv
├── RunwayImages/
├── RunwayImagesMasks/
```
---

## Main Steps

### 1. Web Scraping
- Used Selenium to collect designer collection links
- Downloaded runway images and organized them by brand

### 2. Clothing Segmentation
- Used SegFormer models to separate clothing from runway backgrounds
- Generated binary clothing masks for runway looks

### 3. Color Extraction
- Applied K-Means clustering to clothing pixels
- Extracted dominant RGB colors from each outfit

### 4. Trend Visualization
- Visualized masks and dominant color palettes
- Compared color usage across multiple brands

---

## Results

The Spring/Summer 2025 runway collections showed many neutral and muted color palettes. Black, white, gray, beige, brown, and dark red tones appeared frequently across the sampled brands.

The project showed that computer vision methods can help organize and summarize large fashion image datasets while still keeping visual trends interpretable.

---

## Limitations

This project mainly focused on color analysis, so it does not fully capture other fashion details such as texture, fabric material, silhouette, or layering.

The segmentation model also does not perfectly detect every item. Smaller accessories, shoes, and detailed clothing regions may sometimes be partially missed during mask generation.

In addition, the project mainly focused on Spring/Summer 2025 collections, so long-term seasonal comparisons were limited.

---

## Future Improvements

Possible future improvements include:

- comparing multiple runway seasons
- texture/material classification
- silhouette analysis
- accessory detection
- clustering runway styles by aesthetic category

