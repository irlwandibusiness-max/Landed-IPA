LANDED for iOS: build an unsigned IPA (no Mac needed), then sign with KSign
===========================================================================

1. Create a free GitHub account and a NEW PRIVATE repository (e.g. "landed-ios").
   Private matters: your HTML may contain personal data.
2. Upload everything in this folder to it, keeping the .github folder.
   (On github.com: Add file > Upload files. The hidden .github folder must be included;
   if your file picker skips it, create the file manually at
   .github/workflows/build-ipa.yml and paste the contents.)
3. Go to the Actions tab > "Build unsigned IPA" > Run workflow.
4. After ~5-10 minutes, open the finished run and download the artifact
   "Landed-unsigned-ipa". Unzip it to get Landed.ipa.
5. Move Landed.ipa to your iPhone (AirDrop, Files, iCloud Drive) and open it in KSign.
6. Sign with your certificate + provisioning profile and install.

To update the app later: replace www/index.html in the repo and run the workflow again.

Notes
- The Anthropic API key is stored on the device only. Never bake a key into the HTML.
- Data does not sync with your PC version.
- Wiping/reinstalling the app can clear its local data, so export anything important first.
