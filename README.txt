ROYAL PRESTIGE — WEDDING INVITATION TEMPLATE

A single-page, self-contained invitation (index.html) inspired by the
"royal prestige" style: blush/rose palette, envelope-open splash screen,
animated hero, a scratch-to-reveal card, a photo carousel, a live countdown,
an event timeline, venue/dress-code/pre-wedding/accommodation/gifts sections,
and an RSVP form.

HOW TO USE
1. Open index.html in a browser to preview.
2. Edit the text directly in index.html (names, dates, venue, etc.) — search
   for "Vishal", "Kajal", "Jun 30, 2026" and similar placeholders and replace them.
3. Countdown target date: edit CONFIG.weddingDateISO near the bottom of the
   <script> block.
4. Photos: the #gallery carousel already ships with three neutral,
   license-clear placeholder photos (bouquet / table décor / floral detail)
   in the img/ folder — see img/CREDITS.txt for attribution. Swap them for
   your own by replacing the <img src="img/..."> paths in the three
   <div class="slide"> blocks, e.g.
     <div class="slide"><img src="img/photo1.jpg" alt=""></div>
   Delete img/CREDITS.txt once you've replaced all three placeholder photos.
5. Music: set the #bg-audio element's src="your-track.mp3" to enable the
   music toggle button (top-right). No audio file is included by default.
6. RSVP form: by default, submitting opens the visitor's email app with a
   pre-filled message (edit RSVP_TO_EMAIL near the bottom of the script).
   To collect responses automatically without a backend, create a free
   form endpoint at https://formspree.io, then set FORM_ENDPOINT to that
   URL — submissions will POST there instead.
7. Venue map link: replace the "https://maps.google.com" href in the
   #venue section with your actual Google Maps link.
8. Opening screen background video: plays muted and on loop behind the
   Ganesh ji + marigold toran cover, with a semi-transparent blush/rose
   wash on top (.envelope-bg-overlay) so the text and flowers stay legible
   over any footage. Two versions are used, picked by screen width at
   load (matches the site's existing 520px mobile breakpoint):
     - media/opening-desktop.mp4  -> screens wider than 520px
     - media/opening-mobile.mp4   -> screens 520px and narrower
   Swap either file (keep the same name) or edit the <source> elements
   inside the #envelope <video> tag to change them. The browser picks the
   video once at page load based on screen width — it won't hot-swap if
   you resize an already-open desktop browser window past the breakpoint.
   If a video looks too dark/light/busy under the overlay, adjust the
   colors/opacity in the .envelope-bg-overlay CSS rule.
   The cover has no button: it opens automatically when the opening video
   ends (videos are ~10s). If the video fails or hasn't started within 8s
   (slow network / autoplay blocked), it opens anyway; hard cap 25s.
9. Hero (first page after the cover opens) background video, same
   desktop/mobile switching:
     - media/hero-desktop.mp4  -> screens wider than 520px
     - media/hero-mobile.mp4   -> screens 520px and narrower
   A dark gradient (.hero-overlay) keeps the white names readable.

NOTES
- No external images or fonts are hotlinked from any other wedding site;
  only Google Fonts (Great Vibes / Cormorant Garamond / Playfair Display)
  are loaded from fonts.googleapis.com.
- This is an original build — layout/section order and mood are inspired
  by a reference template, but all code, copy, and assets here are new.
