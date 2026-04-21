# Bundle proof of concept for GitHub Pages

This folder is a simple proof of concept for **one bundle**:
**Tracer Pack: Fire Horse** (bundle ID **6366**)

## What to upload to your public GitHub repo

Upload **everything in this folder** to the root of your repository.

Required files:
- `index.html`
- `.nojekyll`
- `data/bundle_names.csv`
- `data/bundle_images.csv`
- `data/item_images.csv`

Optional helper file:
- `data/poc_bundle.json`

## What each file does

### `data/bundle_names.csv`
This is the bundle metadata file.

Use it to update:
- bundle name
- bundle ID
- title key
- price
- release date
- store page URL

### `data/bundle_images.csv`
This is the bundle hero image file.

Use it to update:
- the main bundle image shown at the top of the page

Important:
- In your source workbook, `bundle_image_link` is a **store page URL**, not a direct image.
- For this proof of concept, the display image uses `bundle_billboard_link`.

### `data/item_images.csv`
This is the item image file.

Use it to update:
- item names
- item types
- item image URLs
- add or remove items

## How to set up GitHub Pages

1. Create a new **public** GitHub repository.
2. Upload all files from this folder to the **root** of the repo.
3. In GitHub, open **Settings** -> **Pages**.
4. Under **Build and deployment**, choose:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Save.
6. Your site will publish at:

   `https://YOUR-USERNAME.github.io/YOUR-REPO/`

## How stakeholders can update this later

### Update the bundle name
Open `data/bundle_names.csv` and change the `bundle_name` value.

### Update the bundle hero image
Open `data/bundle_images.csv` and change the `bundle_hero_image_url` value.

### Update any item image
Open `data/item_images.csv` and change the `item_image_url` value for that row.

### Add an item
Add a new row to `data/item_images.csv` with:
- `bundle_id`
- `bundle_name`
- `item_id`
- `item_asset_name`
- `item_name`
- `item_type`
- `item_image_url`

### Remove an item
Delete that row from `data/item_images.csv`.

### Publish the change
After editing the file(s):
1. Commit the change in GitHub
2. Wait a few seconds
3. Refresh the GitHub Pages site

## Current proof-of-concept bundle contents

Bundle image row:
- `Tracer Pack: Fire Horse`

Item rows included:
- Regal Elegance
- Cool Off
- Lantern
- Lotus
- Outrider
- Firehoof
- Feeling Flaily
- Unbridled Blaze

## Note on the 200 KB image requirement

This proof of concept keeps the source image URLs exactly as they appear in your workbook.
It does **not** download and recompress the images locally.

If you want the next version to:
- download the images into the repo,
- recompress each image to below 200 KB,
- and publish GitHub-hosted image URLs for Tableau,

I can build that as the next step.
