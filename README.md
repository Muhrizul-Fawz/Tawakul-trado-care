# Tawakkul TradoCares | OlyLife THZ Tera-P90+

A responsive React + Vite landing page for product information and WhatsApp enquiries. This is an enquiry website, not an online checkout.

## Requirements
- Node.js 20 or newer recommended
- npm

## Run locally

```bash
npm install
npm run dev
```

Open the local address printed by Vite (usually `http://localhost:5173`).

## Production build

```bash
npm run build
npm run preview
```

The deployable static site is generated in `dist/`.

## Deploy to Vercel
1. Upload this project to a GitHub repository.
2. Import the repository in Vercel.
3. Vercel should detect Vite automatically. Use `npm run build` as the build command and `dist` as the output directory.
4. Deploy. No backend or environment variables are required for the initial version.

## Contact details
The contact configuration is near the top of `src/App.jsx`:

```js
const CONTACT = {
  phone: '+2348128486620',
  wa: 'https://wa.link/k0mqmm',
  direct: '2348128486620'
};
```

`CONTACT.wa` is available for the supplied general contact link. Message-specific buttons use the direct `wa.me` URL with URL-encoded prefilled messages. Update the number and links in this single configuration before publishing if the business details change.

## Add authentic product photographs

The website deliberately does not use the supplied full-page screenshot as a product image and does not fabricate photographs of the device. The current image areas show clear fallbacks until authentic images are added.

Place verified, appropriately licensed photographs in `public/assets/product/` using these exact filenames:

- `complete-system.jpg`
- `main-device.jpg`
- `foot-pedal-remote.jpg`
- `frost-age-beauty-device.jpg`
- `revitaluxe-massager.jpg`

Use real product photography from the manufacturer or images you have permission to use. Keep the subject centred with a clean background; WebP is also suitable if you update the filenames in `src/App.jsx`. The image component switches to a labelled fallback when a file is missing. Product images in the gallery and cards use `object-fit: contain` so the device is not cropped.

Official manufacturer product page for reference: https://www.olylife.com/Main/En/product.php?code=OLY-HCA002A&id=13&name=Olylife+THZ+Tera-P90+

## Edit page content
- Main sections, FAQs, feature text, product cards, contact and service area: `src/App.jsx`
- Colours, typography, breakpoints and responsive styles: `src/styles.css`
- SEO title and metadata: `index.html`
- Favicon: `public/favicon.svg`

Replace the Privacy Policy and Terms & Conditions alert placeholders with actual reviewed policy pages before public launch. Add a canonical URL and social sharing image once a domain and a suitable licensed image are available.

## Included interactions
- Responsive sticky navigation and mobile menu
- Section navigation with smooth scrolling
- WhatsApp CTAs and component-specific prefilled enquiry messages
- Interactive product gallery with thumbnail selection, previous/next controls and lightbox
- FAQ accordion
- Validated enquiry form that prepares a WhatsApp message; the user must press Send in WhatsApp
- Clickable telephone link and floating WhatsApp CTA
- Reduced-motion support, keyboard Escape handling for the menu/lightbox, accessible labels and focus styles

## Important publishing notes
- No price is displayed; customers are asked to request the current price.
- No testimonials, ratings, reseller authorization, delivery guarantees or regulatory approvals are claimed.
- Technology descriptions are presented as product information, not proof of clinical effectiveness.
- The product photographs remain placeholders until authentic images are supplied. Do not publish until those are replaced if product imagery is essential to the campaign.
