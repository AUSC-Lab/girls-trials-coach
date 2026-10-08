# AUSC Girls Trials 2027 app

The installable phone app for the girls' trial coaches. It is separate from the boys' app:
its own Google Sheet, its own Apps Script, its own passcode and its own web address.
Player details stay in the girls' Google Sheet; these files are only the app screens.

## Set up (once)

1. **Sheet and script.** Upload "AUSC Girls Trials 2027 - Coach sheet.xlsx" to Google Drive, open it,
   File > Save as Google Sheets. Then Extensions > Apps Script, paste in Girls-Code.gs, save.
   Project Settings > Script Properties > add `PASSCODE` (use a different code from the boys').
   Deploy > New deployment > Web app, Execute as: Me, Who has access: Anyone. Copy the URL ending in `/exec`.
2. **Edit `config.js`.** Paste that URL between the quotes.
3. **Put the files on GitHub Pages.**
   - On github.com, create a new **public** repository, e.g. `ausc-girls`.
   - Add file > Upload files, drag in every file from this folder (not the folder itself), Commit.
   - Settings > Pages > Source: Deploy from a branch > Branch: `main`, folder `/ (root)` > Save.
   - After a minute or two the app is at `https://<your-username>.github.io/ausc-girls/`.
4. **Install it on a phone.** Open that link, enter the passcode and your name, then
   - iPhone (Safari): Share > Add to Home Screen
   - Android (Chrome): tap Install in the purple bar, or menu > Install app

## Good to know

- A coach can have both the boys' and girls' apps on one phone. Each keeps its own passcode and name.
- No player details are in these files. The data only comes back with the passcode.
- To change the passcode, edit the PASSCODE property. No redeploy needed.
- If you change the Apps Script code, redeploy as a **new version of the same deployment**
  (Deploy > Manage deployments > pencil icon) so the URL in `config.js` keeps working.
