
https://github.com/user-attachments/assets/9bcf179e-1554-4b1f-98f6-5952d2e3f054

# Shopify Custom Sections

Custom sections built on top of the Shopify **Dawn** theme, using Liquid, vanilla JavaScript, and CSS.

<!-- Add a screenshot or GIF here: ![Quick view demo](assets/demo.gif) -->

## Sections

### 🛒 Product Grid with Quick View
A grid of up to 6 merchant-selected products. Each card opens a quick view popup where customers pick options and add the product to the cart without leaving the page.

**Features**
- Quick view popup with product image, title, price, and description
- Option selectors built dynamically from the product data: a button group for **Color** and a custom dropdown for other options (e.g. **Size**)
- Variant matching with a `Map` lookup and clear button states: *Select options*, *Add to Cart*, *Out of stock*, *Unavailable*
- Add to cart through Shopify's AJAX Cart API (`/cart/add.js`)
- **Promotion:** adding a Black + Medium variant also adds the Dark Winter Jacket
- Header cart icon refreshed through the Section Rendering API (no page reload)
- Popup is locked while a request is in flight, then closes automatically after success
- Theme editor support (`block.shopify_attributes`, placeholder for empty blocks)
- Scoped by `section.id`, so the section can be added more than once on a page

### 🎁 Full Banner
A responsive gift-guide banner with a header bar, hero area, and footer text. Everything is editable from the theme editor: logo, texts, links, and two pattern images, with fallback assets when nothing is uploaded.

**Features**
- Separate desktop and mobile texts
- Accessible burger menu on mobile (`aria-expanded`, keyboard support)
- Hover animations on the call-to-action buttons
- Scoped by `section.id`, so multiple instances don't conflict

## Tech
`Liquid` · `JavaScript (ES6+)` · `CSS` · `Shopify Dawn` · `Shopify CLI`

## Run locally
```bash
shopify theme dev --store your-store.myshopify.com
```

## Project structure
```
sections/
  product-grid.liquid   # Product grid + quick view popup + add to cart
  the-Banner.liquid     # Full banner section
templates/              # Page templates that use the sections
```

## Author
**Omar Khatab** — [GitHub](https://github.com/omar-khatab)
