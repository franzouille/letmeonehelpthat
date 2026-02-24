# Let Me One Help That 💡

A friendly [LMGTFY](https://letmegooglethat.com/)-style page for [Mirakl One Help](https://help.mirakl.com/).

Paste a question in the URL, share the link, and watch the magic happen.

## Demo

```
https://<username>.github.io/let-me-onehelp-that/?q=How+to+configure+price+rules
```

The page will:
1. Display a faithful replica of the Mirakl One Help interface
2. Animate a cursor moving to the search input
3. Type the question character by character
4. Click the Send button
5. Show a friendly message with a link to the real One Help

## Usage

Simply append your question as a `q` query parameter:

```
https://<username>.github.io/let-me-onehelp-that/?q=Your+question+here
```

### Examples

- `?q=How+to+configure+price+rules+for+a+specific+seller`
- `?q=What+is+the+getOrders+API`
- `?q=How+to+set+up+Mirakl+Connect`

### URL Encoding

Spaces can be `+` or `%20`. Special characters should be URL-encoded.

## Project Structure

```
let-me-onehelp-that/
├── index.html      ← Self-contained app (HTML + CSS + JS, references onehelp assets)
├── onehelp/        ← Downloaded assets from help.mirakl.com (HTML, CSS, images, fonts)
└── README.md       ← This file
```

## Deploy on GitHub Pages

1. Create a new repo named `let-me-onehelp-that`
2. Clone it locally:
   ```bash
   git clone https://github.com/<username>/let-me-onehelp-that.git
   cd let-me-onehelp-that
   ```
3. Add all files (`index.html`, `onehelp/` folder, `README.md`)
4. Push:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```
5. Go to **Settings → Pages → Source**: select `main` branch, click **Save**
6. Your site is live at `https://<username>.github.io/let-me-onehelp-that/`

## Local Development

```bash
# Simple HTTP server (needed for asset loading)
python -m http.server 8000
# Then open http://localhost:8000/?q=test+question
```

## Configuration

No configuration needed. Everything is self-contained.

## Future Ideas

- [ ] Slack shortcut integration (message shortcut → generates LMOHT link → posts in thread)
- [ ] `&autoredirect=true` param to auto-redirect to real One Help after animation
- [ ] Analytics to track most asked questions
- [ ] Dark mode support

## License

Internal Mirakl tool. Not for external distribution.
