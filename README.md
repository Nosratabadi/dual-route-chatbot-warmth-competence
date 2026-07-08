# Conversational AI Warmth and Competence: Experimental Materials

This repository contains the experimental web interfaces and system prompts used in a three-study experimental series testing a dual-route model of chatbot warmth and competence effects on consumer purchase intention.

**Note on anonymization.** This repository is being shared as supplementary material during peer review. Author names, contact details, and institutional affiliation have been withheld from the informed consent text in the HTML files to preserve the anonymity of the review process. Full contact information will be restored once the associated manuscript has completed peer review.

## Files

- `Study1.html` — Web interface for Study 1 (competence manipulation; skincare product)
- `Study2.html` — Web interface for Study 2 (warmth manipulation; skincare product)
- `Study3.html` — Web interface for Study 3 (full 2 × 2 × 2 warmth × competence × product-type design)
- `System_Prompt_Repository_Studies1-3.md` — Complete, verbatim system prompts for every experimental condition across all three studies (12 conditions total), extracted directly from source, plus model and generation-parameter disclosure

## Running these files

Each HTML file calls the Google Gemini API and requires your own API key. Open the file, locate the line:

```
const API_KEY = "YOUR_GEMINI_API_KEY_HERE";
```

and replace the placeholder with your own key. Do not commit a real API key to this repository.

**Model availability.** Studies 1 and 2 were built against `gemini-2.5-flash-preview-09-2025`, which was Google's current preview-tier Gemini 2.5 Flash model at the time of data collection. Google has since shut this model down (as of February 17, 2026), so `Study1.html` and `Study2.html` will not return API responses as-is. To run them today, substitute a currently available model string (e.g., `gemini-2.5-flash`) for `MODEL_NAME`; note that responses will then reflect that replacement model's behavior rather than the model used in the original data collection. `Study3.html` uses `gemini-3.5-flash` and should still function normally with a valid key, subject to Google's ordinary API availability.

## Data collection

None of these files submit data to a live endpoint as shared here. Study 3 references a `GOOGLE_SHEET_URL` placeholder that must be replaced with your own endpoint if you wish to collect data. Studies 1 and 2 write completed session data to an on-page field for manual export.
