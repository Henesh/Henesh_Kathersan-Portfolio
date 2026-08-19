# Henesh Kathresan — AI Engineer Portfolio

Personal portfolio for Henesh Kathresan, an Artificial Intelligence student at Universiti Teknikal Malaysia Melaka (UTeM).

## Featured Project — SmartSave

SmartSave is a privacy-first AI financial advisory system for Malaysian university students. Users can log expenses through Telegram using text, receipt photos or PDF receipts. The system routes inputs through Activepieces to a FastAPI backend, performs OCR/PDF extraction and intelligent categorization, stores transactions in Firebase Firestore, and provides grounded saving recommendations using a locally hosted Mistral 7B model through Ollama.

The companion React + Recharts dashboard provides period-based spending summaries, category analytics, budget progress, transaction management and the latest AI advice.

### Architecture

`Telegram → Activepieces → FastAPI → OCR / PDF Parser / Categorizer / Validation → Firestore → React Dashboard`

### SmartSave results

- 86.7% categorization accuracy (macro F1: 0.868, n=158 labeled transactions)
- 100% amount + merchant/recipient extraction accuracy on Malaysian bank PDF receipts after the bidirectional-search parser fix
- ~0.57s average image OCR processing
- ~0.17s average PDF extraction
- ~2ms categorization
- ~4.89s average local Mistral tip generation

### Technology

Python · FastAPI · EasyOCR · PyMuPDF · Mistral 7B · Ollama · Firebase Firestore · React · Recharts · Telegram Bot API · Activepieces · Docker · Firebase Hosting

## Portfolio

The portfolio is a lightweight static site built with HTML, CSS and JavaScript. It is designed to work with GitHub Pages, Netlify or Firebase Hosting.

## Local preview

```bash
python -m http.server 5500
```

Then open `http://localhost:5500`.

## GitHub Pages deployment

1. Open **Settings → Pages** in the repository.
2. Select **Deploy from a branch**.
3. Select the `main` branch and `/ (root)`.
4. Save and wait for the Pages deployment to complete.

There is no Node.js build step or backend dependency, so the repository can be deployed directly as static files.

## Production checklist

- Replace placeholder project links with exact project repositories or live demos.
- Add `henesh.jpg` if a real profile image is desired; the current hero uses an initials fallback so the page remains functional without the image.
- Use HTTPS on the final domain.
- Verify external social links and email before publishing.
- Check the final site on desktop and mobile browsers.
