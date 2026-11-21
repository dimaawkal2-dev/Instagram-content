# No Perfect Parents: Course Website (DRAFT)

A single-page, mobile-friendly sales page for the 8-week **No Perfect Parents** program.

- **Status:** draft. It's not published and checkout isn't connected, so no one can be charged.
- **Preview:** open `index.html` in any browser.
- **No card data:** the Enroll buttons only *link out* to your payment provider's hosted checkout page. The site has no payment form and stores nothing.

## 1. Connect your Whish checkout

1. Log in to your **Whish business/merchant account** and look for **payment links** (or "request payment", or online checkout).
2. Create two links:
   - **Pay in full:** $297 USD, one-time
   - **Payment plan:** $109 USD. See the note below.
3. Open `index.html`, find `CHECKOUT_LINKS` near the bottom, and paste each link between the quotes:
   ```js
   const CHECKOUT_LINKS = {
     full: "https://your-whish-link-for-297",
     plan: "https://your-whish-link-for-109"
   };
   ```
4. Save and refresh. The grey buttons turn orange and go to Whish.

**Check with Whish before launching:**
- [ ] Your account can accept payments **online through a link** (not only in-app transfers between Whish users).
- [ ] Which payment methods buyers can use (Whish wallet only, or also Visa/Mastercard). If it's wallet only, buyers outside Lebanon may not be able to pay.
- [ ] Whether Whish supports **automatic monthly instalments**. If it doesn't, the 3 × $109 plan becomes 3 separate links or invoices you send each month. In that case, update the plan wording on the page.
- [ ] That the checkout page is **hosted by Whish** (`https://`), so the buyer types card details there, never on your site.
- [ ] Fees, payout timing, and whether you receive the buyer's email so you can send course access.

If Whish can't do card payments online, the page works the same with a **Stripe Payment Link**, **Gumroad**, **Lemon Squeezy**, or a course platform's checkout (Teachable, Thinkific, Podia). Just paste that link instead.

## 2. Fill in the placeholders

Placeholders are highlighted in yellow on the page:

- [ ] Your name, short bio and Instagram handle
- [ ] Access length and any bonus (the pricing cards)
- [ ] Weekly time commitment, how students get access after paying, co-parent policy, refund policy (the FAQ)
- [ ] Privacy policy, terms & refund policy, contact email (footer). You need these before taking payments.
- [ ] Optional: add real testimonials, with written permission, once you have them

## 3. Decide how students get the lessons

Payment and course delivery are separate. Choose one:
- A course platform (Teachable, Thinkific, Podia, Kajabi) that hosts the videos and logins, or
- Private video links plus a welcome email you send after each payment.

## 4. Before going live

- [ ] Test each checkout link with a small or test payment, then refund it
- [ ] Check the page on your phone
- [ ] Remove the dark "DRAFT PREVIEW" bar at the top of `index.html`
- [ ] Remove the `<meta name="robots" content="noindex, nofollow">` line so Google can find the page
- [ ] Publish with a static host (Netlify, GitHub Pages, Cloudflare Pages, Carrd or similar) and add the link to your Instagram bio

Nothing here has been published, and no one has been charged.
