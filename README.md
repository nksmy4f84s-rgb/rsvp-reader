RSVP PRO: LOGIC INTEGRATED EDITION
----------------------------------

1. OVERVIEW
RSVP Pro is a high-performance speed-reading tool that combines 
advanced PDF text extraction with dynamic linguistic weighting.
It is designed to solve common "dirty" text issues in PDFs while 
maintaining high comprehension at speeds up to 1500 WPM.

2. CORE LOGIC (Integrated from rsvp-reader-master)
This version utilizes a weighted-delay engine. Rather than a 
static WPM, the reader calculates time-per-word using:

   Delay = (60,000 / WPM) * Multiplier

   Multipliers applied:
   - Common Words (the, of, and): 0.8x (shown faster)
   - Long Words (>8 chars): 1.2x (hesitation delay)
   - Comma/Semicolon: 1.4x (pause for breath)
   - Full Stops (. ! ?): 1.8x (sentence transition)

3. PDF RECONSTRUCTION FEATURES
- Geometric Fusing: Uses X-coordinate and glyph-width math 
  to prevent words from being split (e.g., "mas ter" becomes "master").
- Artifact Correction: Automatically fixes common extraction 
  errors like "lhe" or "Ihe" into "the".
- NFKC Normalization: Resolves ligatures (fi, fl, etc.) into 
  standard searchable text.

4. CONTROLS
- [Spacebar]: Toggle Play/Pause
- [Up Arrow]: Increase speed by 50 WPM
- [Chapters Button]: Opens the Table of Contents (mapped to word indices)
- [Reset]: Returns to the beginning of the document

5. SETUP
Open the .html file in any modern web browser. An internet 
connection is required to load the pdf.js rendering engine via CDN.

----------------------------------
"Speed is the byproduct of efficiency."
