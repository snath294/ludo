# Ludo Buddy - the easy, no-install way to build your game

You can build your Android app entirely from a web browser.
No Android Studio. No Flutter install. No Java. GitHub does the heavy work.

---

## What you need

- A free GitHub account (https://github.com/signup)
- Your phone (only at the very end, to install the game)

---

## Step 1 - Create your repository

1. Go to https://github.com and sign in.
2. Click the black **"+"** button in the top-right corner.
3. Choose **New repository**.
4. Repository name: `ludo-buddy`
5. Choose **Private** (recommended) or Public.
6. Leave everything else as-is and click **Create repository**.

---

## Step 2 - Upload the project

1. You should now see the empty repository page with the words "Quick setup".
2. Click the link **"uploading an existing file"**.
3. Drag every file and folder from this kit into the box:
   - the `lib` folder
   - `pubspec.yaml`
   - `analysis_options.yaml`
   - the `.github` folder (this holds the build recipe - very important)
   - `README.md`
   - `.gitignore`
4. Scroll down and click **Commit changes**.

Note: GitHub's browser upload may skip folders starting with a dot.
If the `.github` folder is missing afterwards, open **Add file -> Create new file**,
type `.github/workflows/build-apk.yml` in the filename box, paste in the contents
of the workflow file, and commit.

---

## Step 3 - Let GitHub build the app

1. Click the **Actions** tab at the top of your repository.
2. If asked, click **"I understand my workflows, go ahead and enable them"**.
3. In the left sidebar click **Build Android APK**.
4. Click the **Run workflow** dropdown on the right, then the green **Run workflow** button.
5. Wait about 3 to 5 minutes. Refresh the page until you see a green tick.

---

## Step 4 - Download your APK

1. Click the finished (green) run in the list.
2. Scroll to the very bottom, to the **Artifacts** box.
3. Click **ludo-buddy-apk** to download a zip file.
4. Unzip it. Inside is `app-release.apk` - your finished game!

---

## Step 5 - Put the game on your phone

1. Send `app-release.apk` to your phone in any easy way:
   - Email it to yourself and open the attachment on the phone, or
   - Upload it to Google Drive from your PC and download it on the phone, or
   - Send it to yourself in WhatsApp and tap the file.
2. Tap the downloaded file on your phone.
3. Android may say *"For your security, your phone is not allowed to install
   unknown apps from this source"*. Tap **Settings** and switch on
   **Allow from this source**, then tap **Install**.
4. Open the app and play.

---

## Step 6 - Publishing to the Google Play Store (later)

When you are ready to publish:

1. Download the **ludo-buddy-aab** artifact from the same run. That `.aab` file
   is the file Google Play wants.
2. Create a Google Play developer account ($25 one-time) at
   https://play.google.com/console/signup
3. Create the app, upload the `.aab`, and fill in the store listing.

Before your first public release you should sign the app with your own private
key instead of the default test key. Ask me and I will add a second workflow
that generates and uses a proper release key for you, still entirely in the
browser.

---

## Making changes later

- Quick text or colour change: open the file in GitHub, click the pencil icon,
  edit, and commit. GitHub rebuilds automatically.
- Bigger editing session in a real editor: press the **`.`** key on any page of
  your repository to open the browser editor (github.dev).
