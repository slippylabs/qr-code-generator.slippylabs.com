# QR Code Generator

Turn text or a URL into a scannable QR code with a hand-built in-browser encoder. Runs entirely in your browser, PNG download included.

**Live:** <https://qr-code-generator.slippylabs.com/>

## What it does

- Encode text, a URL, or a WiFi network (WPA/WPA2, WEP or open) into a scannable code.
- All four error-correction levels — L (~7%), M (~15%), Q (~25%), H (~30%).
- Three output sizes, PNG download.

## How it works

The QR encoder is written from scratch in the page: mode selection and bit packing, Reed-Solomon error-correction blocks over GF(256), the module matrix with its finder, timing and alignment patterns, mask evaluation, and the format/version information. No library — the matrix you see is built byte by byte in your browser.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/qr-code-generator.slippylabs.com.git
cd qr-code-generator.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
