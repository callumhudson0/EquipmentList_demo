# Bandshop Equipment List Generator

An AI-powered internal tool that generates warehouse pick lists from event enquiry details. Built as a demo for client presentation.

---

## What it does

A staff member fills in the event details (event type, guest count, venue, entertainment requirements) and the tool instantly generates a formatted warehouse pick list — the same format as a manual pick list, but produced automatically in seconds.

The output can be copied directly into your quoting system or printed as a PDF.

---

## Files

| File | Description |
|---|---|
| `equipment-list-demo.html` | Demo version — no API key needed, works offline |
| `equipment-list-generator.html` | Full AI version — requires an Anthropic API key |

---

## How to run the demo (no API key needed)

### Option 1 — Open locally
Just download `equipment-list-demo.html` and open it in any browser. No internet connection required.

### Option 2 — Host on GitHub Pages (free, shareable link)

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click **+** → **New repository**
3. Name it e.g. `bandshop-demo` and set it to **Public**
4. Click **Create repository**
5. Click **uploading an existing file**
6. Drag and drop `equipment-list-demo.html` into the upload area
7. Click **Commit changes**
8. Go to **Settings** → **Pages** (left sidebar)
9. Under "Branch", select **main** and click **Save**
10. Wait about 60 seconds
11. Your demo is now live at:

```
https://yourusername.github.io/bandshop-demo/equipment-list-demo.html
```

Replace `yourusername` with your GitHub username and `bandshop-demo` with whatever you named the repository.

### Option 3 — Host on Netlify (even quicker)

1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop the HTML file onto the page
3. You'll get a live link instantly — no account needed

---

## How to run the full AI version

The full version (`equipment-list-generator.html`) uses the Claude API to generate smarter, more flexible pick lists that understand freeform notes and adapt to unusual event setups.

### Getting an API key

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up with your email and verify your phone number
3. You'll receive approximately $5 in free starter credits — enough for hundreds of pick list generations
4. Go to **Settings** → **API Keys** → **Create Key**
5. Copy the key (starts with `sk-ant-...`)

### Using the key

Open `equipment-list-generator.html` in a browser, paste your API key into the field at the top, and generate lists as normal. The key is never stored — you'll need to paste it each session.

### Cost at scale

Each pick list generation costs less than $0.01. At typical usage:

| Volume | Estimated monthly cost |
|---|---|
| 100 lists/month | ~$0.50 |
| 500 lists/month | ~$2.50 |
| 1,000 lists/month | ~$5.00 |

---

## Full system architecture (future build)

For a production-ready version integrated into the business, the full system would include:

- **Website enquiry form** — embedded on the client-facing website
- **Backend API server** — handles requests, manages the API key centrally
- **Claude API** — generates the pick list from event details + live inventory
- **Database** — stores quote history, user accounts, inventory
- **Live inventory sync** — connects to the existing hire management system
- **Staff internal tool** — pick list generator with login, history, and admin panel
- **Quote builder** — pulls pricing from the hire system to produce full quotes

### Phased rollout

| Phase | What's included | Estimated cost |
|---|---|---|
| Phase 1 — Now | Demo HTML file, Netlify/GitHub Pages hosting | ~£0/month |
| Phase 2 — Near term | Hosted backend, staff logins, quote history | £50–100/month + ~£3,000–5,000 build |
| Phase 3 — Full build | Live inventory sync, pricing integration, admin panel | £100–200/month + £3,000–8,000 build |

---

## Demo vs full AI version

| Feature | Demo | Full AI version |
|---|---|---|
| Generates pick list | ✅ | ✅ |
| No API key needed | ✅ | ❌ |
| Works offline | ✅ | ❌ |
| Understands freeform notes | ❌ | ✅ |
| Adapts to unusual setups | ❌ | ✅ |
| Copy to clipboard | ✅ | ✅ |
| Print / PDF | ✅ | ✅ |

---

## Built with

- Vanilla HTML, CSS, JavaScript — no frameworks, no dependencies
- [Claude API](https://anthropic.com) (full AI version only)
- Inventory based on Bandshop asset listing
