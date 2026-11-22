# E-Techniqa Website

A responsive static storefront for GitHub Pages. No build tools or frameworks required.

## Files
- `index.html` — main storefront
- `styles.css` — all layout and design
- `catalog.js` — **the main file to edit when adding products, prices and projects**
- `app.js` — search, category filters, cart and WhatsApp order behaviour
- `guide.html` — Student Hub landing page
- `assets/logo.svg` — editable vector brand mark

## Add a component
Open `catalog.js`, find `components`, and add an object:
```js
{id:"new-item",name:"New Sensor",category:"sensor",categoryLabel:"Sensors & Modules",symbol:"⌁",price:150,unit:"per module",desc:"Short description.",badge:"NEW"}
```
Use a unique `id`. Categories: `passive`, `semiconductor`, `sensor`, `development`, `power`.

## Add a smart product
Add an object inside `smartProducts`:
```js
{id:"smart-item",name:"Smart Device",categoryLabel:"Smart Home",symbol:"⌂",price:null,unit:"per unit",desc:"Product details.",badge:"NEW"}
```
Use `price:null` to show “Price on request”.

## Add a project
Add an object inside `projects`:
```js
{id:"new-project",icon:"⚙",name:"New Project",desc:"What the project does.",tag:"CUSTOM SOLUTION"}
```

## Important settings
At the top of `catalog.js`, update:
- `whatsappNumber`: replace `8801XXXXXXXXX` with your WhatsApp number, digits only.
- `facebookUrl`: paste your Facebook Page URL.

## Publish on GitHub Pages
1. Extract the ZIP.
2. Upload all files and the `assets` folder into the root of your GitHub repository.
3. In repository Settings → Pages, choose Deploy from a branch, select `main` and `/ (root)`.
4. Save and wait for GitHub Pages to publish.
5. Open the published HTTPS URL. Do not open `index.html` from a file manager preview to test the live site.

## QR codes
Create a QR code for the final published URL of a specific guide page, for example:
`https://YOUR-USERNAME.github.io/guides/arduino-uno.html`
Create that guide page in the repository first. The Student Hub currently provides a landing page and structure; individual product guides need to be added as content becomes available.

## Notes
- This is a static catalogue/cart. Checkout is sent to WhatsApp; there is no online payment gateway, customer account, inventory database or admin dashboard.
- Product prices and availability are examples/placeholders until you update them.
- Before selling mains-powered products or automation devices, verify ratings, protection, installation requirements and local compliance.
