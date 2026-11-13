# Camp Split 🏕️

A private camping expense calculator for friends. Equal shares, fuel, car-cleaning allowance, a group kitty, join dates, themes and a PIN lock.

- No server and no database to set up. Everything is saved in your own browser (IndexedDB plus local storage).
- Your data is never uploaded to GitHub. Only the app code is public.
- Use **Backup data** in Trip settings regularly and keep the file somewhere safe.

## Put it online with GitHub Pages

1. Create a new repository on GitHub (for example `camp-split`).
2. Upload `index.html`, `.nojekyll` and `README.md` to the repository root.
3. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then **Save**.
4. After a minute your app is live at `https://YOUR-USERNAME.github.io/camp-split/`.

## Keeping your trip safe

- **Send backup** shares a backup file to WhatsApp, Google Drive, email and more.
- **Copy restore link** creates a link that contains the whole trip. Save it in a WhatsApp chat with yourself. Opening it on any device offers to restore the trip. Anyone with the link can read the trip details, so keep it private.
- The restore link does not include your PIN or logo image.

## Google Drive sync (optional)

Keeps your trip in your own Google Drive folder so every device shows the same data.

1. In Google Drive, create a folder and copy its ID from the address bar (the text after `/folders/`).
2. Go to https://script.google.com, create a New project and paste the contents of `Code.gs`. Set `FOLDER_ID` and your own secret `ADMIN_CODE` at the top.
3. Deploy, New deployment, type **Web app**. Execute as **Me**, Who has access **Anyone**. Approve the permissions and copy the Web app URL (it ends with `/exec`).
4. In the app, open **Google Drive sync**, paste the URL and your code, then press **Connect**. Repeat on any other device.
5. To change the script later, create a new deployment version and use the new URL.

**Admin panel:** connect with your admin code, then use the **Admin panel** to add each friend by name and press **Copy link**. Each friend gets their own private view-only link. Opening it connects their device automatically. They can look at the trip settings, friends, money collected, expenses, summary, who pays whom and payments, but cannot change anything. They never see the Admin panel, backups or Drive settings. Press **Remove** to stop a link working straight away. View-only is enforced by the Google script, not just hidden in the page. Keep your admin code to yourself.

If you already deployed an older script, paste the new `Code.gs`, then use Deploy, Manage deployments, Edit, New version. The URL stays the same.

**Remove all data…** asks for your access code and shows a clear warning before it deletes the trip from Drive (the file goes to the Drive bin) and from this device.

## Good to know

- Open the app on the same phone and browser during the trip, since data lives in that browser.
- The PIN is a screen lock, not encryption. A forgotten PIN cannot be recovered, so keep backups.
- Clearing your browser’s site data erases the saved trip. Back up first.
