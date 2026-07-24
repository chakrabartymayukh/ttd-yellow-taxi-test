# Yellow Taxi Tray — Landing Page (Test)

Standalone test landing page for **The Traveller's Den**'s Yellow Taxi Tray
(₹1,350, live at https://thetravellersden.in/product/yellow-taxi-2/).

Hosted on GitHub Pages for testing before integration into the live
WooCommerce/Elementor site.

## Live versions

- **V2 (current)** — video hero: https://chakrabartymayukh.github.io/ttd-yellow-taxi-test/
- **V1 (archived)** — static photo hero: https://chakrabartymayukh.github.io/ttd-yellow-taxi-test/v1/

Both stay live permanently — V1 is not deleted when V2 ships.

## Structure

```
index.html          → V2, current version (video hero)
images/              → shared images (poster frame, tray close-up crop)
videos/              → hero video (ektara-scored, 10s)
v1/index.html        → V1 snapshot, frozen (static photo hero)
v1/images/           → V1's own copy of its images
```

## Notes for whoever edits this next

- **Price is NOT hardcoded.** A script at the bottom of `index.html` fetches
  the live price from WooCommerce's public Store API
  (`thetravellersden.in/wp-json/wc/store/v1/products?slug=yellow-taxi-2`)
  on page load. If the price changes on the real product page, this page
  updates itself automatically — no edit needed here. The number typed into
  the HTML is only a fallback shown if that fetch fails (e.g. before this
  is hosted on the real domain, where cross-origin fetches are blocked).
- **Tray "spotlight" effect**: the hero photo/video is desaturated via CSS
  filter; a separate sharp crop of just the tray (`images/tray-only.jpg`)
  sits on top with a soft mask, so it's visually clear the tray — not
  anything else in the scene — is the product for sale.
- **Buy button** links straight to `thetravellersden.in/product/yellow-taxi-2/`.
- Reviews and founder-note sections are placeholders — marked with HTML
  comments — waiting on real content, not filled with invented claims.

## Next step

Once tested and approved here, this gets integrated into the live
WooCommerce site via an Elementor HTML widget or standalone page template.
