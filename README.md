# AI Page Rewriter

A Chrome extension that rewrites webpage copy using Claude AI. Turns vague, institutional marketing-speak into clear, conversion-focused text.
After
<img width="1856" height="1057" alt="Screenshot 2026-01-02 at 14 05 03" src="https://github.com/user-attachments/assets/f6530fd6-2f3a-4927-bee3-7384f5f926c5" />


## What it does

- Extracts visible text from any webpage
- Rewrites headlines, body copy, and CTAs for clarity and conversion
- Optionally researches the company to include verified stats
- Preserves DOM structure — see changes in place instantly
- Reset button to restore original text

## Modes

| Mode | Goal |
|------|------|
| **Conversion** | Maximize action-taking. Lead with outcomes. |
| **Clarity** | Maximize comprehension. Front-load information. |
| **Trust** | Maximize credibility. Specific beats impressive. |
| **Emotion** | Maximize resonance. Name the frustration or aspiration. |
| **Professional** | Maximize authority. Precise terminology, no hype. |

## Setup

### 1. Get a Claude API key

Go to [console.anthropic.com](https://console.anthropic.com) and create an API key.

### 2. Install the extension

1. Download or clone this repo
2. Open Chrome and go to `chrome://extensions`
3. Enable "Developer mode" (top right)
4. Click "Load unpacked" and select this folder

### 3. Add your API key

Click the extension icon, paste your API key in the field at the top, and click Save.

## Usage

1. Navigate to any webpage
2. Click the extension icon
3. Select a rewrite mode
4. (Optional) Add context like "Target audience: B2B SaaS buyers"
5. Click "Rewrite Page"
6. Review changes on the page
7. Click "Reset" to restore original text

### Skip Research

Check "Skip research" for faster rewrites without web search. Uncheck it to have Claude look up real company stats before rewriting.

## How it works

1. **Extract** — Content script pulls visible text elements from the page
2. **Research** (optional) — Claude searches the web for company facts
3. **Rewrite** — Claude rewrites each text block using conversion copywriting principles
4. **Apply** — Content script replaces text in the DOM

## Cost

Uses your own Claude API key. Typical rewrite costs $0.02-0.10 depending on page size and whether research is enabled.

- With research: ~15-25k tokens
- Without research: ~4-8k tokens

## Limitations

- Only rewrites visible text (not images, videos, or dynamically loaded content)
- Some sites with heavy JavaScript may not extract properly
- Rate limited to ~2 rewrites per minute on default API tier

## Files

```
├── manifest.json     # Chrome extension config
├── popup.html        # Extension popup UI
├── popup.js          # Main logic (API calls, prompt engineering)
├── content.js        # DOM extraction and text replacement
└── README.md
```

## Credits

Built by [Your Name]. Powered by [Claude](https://anthropic.com) by Anthropic.

## License

MIT — do whatever you want with it.
