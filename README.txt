TOP HEROES: WHAT KIND OF PLAYER ARE YOU?
======================================
FILES
  index.html  - Complete mobile-friendly quiz for GitHub Pages
  Code.gs     - Google Sheets Apps Script backend

SET UP GOOGLE SHEETS (DO THIS FIRST)
1. Create a new Google Sheet, e.g. "Top Heroes Personality Results".
2. Open Extensions > Apps Script.
3. Replace the default Code.gs content with the provided Code.gs file.
4. Save the project.
5. Click Deploy > New deployment > Web app.
6. Set "Execute as" to "Me" and "Who has access" to "Anyone".
7. Deploy, grant requested permissions, and copy the Web app URL ending in /exec.
8. Open index.html in a text editor. Near the start of its script find:
      const SCRIPT_URL = '';
   Paste the URL between the quotes, e.g.:
      const SCRIPT_URL = 'https://script.google.com/macros/s/...../exec';
9. Save index.html.

PUBLISH ON GITHUB PAGES
1. Create a public GitHub repository.
2. Upload index.html into the repository root.
3. Go to Settings > Pages > Deploy from a branch > main / (root) > Save.
4. Wait for the published GitHub Pages URL and open it on your phone.

TEST
1. Enter an in-game name, complete all 18 questions, and reveal a result.
2. Verify that the Google Sheet has a new Responses row.
3. Open the guild dashboard and confirm the total increased.
4. Use "Save result card" to save a PNG, or "Copy result" to share text.

NOTES
- No consent checkbox, as requested. In-game name is mandatory.
- Dashboard shows only aggregated primary-personality counts, not individual names or answers.
- Results are stored in your Google Sheet, which should remain private.
- Apps Script web app access must be Anyone for anonymous guildmates to submit.
- A web app URL cannot be preconfigured until you create/deploy your own script.
- If you edit Code.gs after deployment, deploy a NEW VERSION under Manage deployments.
- The front end uses a hidden-form POST to avoid cross-origin browser errors. Since Apps Script's
  response cannot be reliably read from a third-party website, the page confirms only that
  the submission was sent, not that it was saved. Check the sheet or dashboard to verify.
- A repeated manual retry may create a duplicate if the previous submission reached the server.
- This is a fun entertainment quiz, not a validated psychological assessment.
