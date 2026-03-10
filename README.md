# Sinners Testimony — Coming Soon Landing

Landing page with email + phone signup for Klaviyo (email & SMS marketing).

## Klaviyo setup (email + SMS)

### 1. Add onsite tracking

Replace `YOUR_PUBLIC_API_KEY` in `index.html` with your Klaviyo **Public API key**:

- Klaviyo → **Settings** → **API Keys** → **Create API Key**
- Choose **Public** (for onsite tracking)
- Copy the key and replace `YOUR_PUBLIC_API_KEY` in the script tag near the bottom of `index.html`

### 2. Create your embed form

1. Klaviyo → **Sign-up forms** → **Create form**
2. Choose **Embed**
3. Add blocks:
   - **Email** (required)
   - **Phone number** (for SMS)
   - **SMS consent** (required for SMS)
4. Add SMS disclosure (e.g. “Msg & data rates may apply”) and links to your Privacy Policy and Terms
5. **Publish** the form
6. Open **Targeting & behavior** → **Publish** and copy the **embed code**

### 3. Replace the form on the page

1. Open `index.html`
2. Find the `#klaviyo-form-container` div
3. Replace the entire `<form>` block inside it with your Klaviyo embed code (paste the full block they give you)

The page is styled so Klaviyo’s form will fit the existing design.

## Running locally

Open `index.html` in a browser or use a local server:

```bash
python -m http.server 8000
# or
npx serve .
```

Then visit `http://localhost:8000`.

## Customization

- **Privacy / Terms links** — Update `/privacy` and `/terms` in the disclosure to your real URLs
- **Brand text** — Edit the tagline “Be the first to know when we open” in `index.html`
- **Colors** — Use the CSS variables in `:root` to adjust theme
