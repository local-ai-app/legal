# Snipit Legal

Public Privacy Policy and Terms of Use for the Snipit iOS app.

## Pages

- `index.html` — landing
- `privacy.html` — Privacy Policy
- `terms.html` — Terms of Use
- `style.css` — shared styling

## Deploy to GitHub Pages

1. Create a new public repo. Suggested name: `legal` under a `snipit-app` org (or under your personal account).
2. Push the contents of this folder to `main`:

   ```bash
   cd /Users/zangoti/claudecode/clip-iOS/repo/.claude/worktrees/ai-tier-fix-v2/legal
   git init
   git add .
   git commit -m "Initial privacy policy and terms of use"
   git branch -M main
   git remote add origin https://github.com/local-ai-app/legal.git
   git push -u origin main
   ```

3. In the repo on github.com, open **Settings → Pages**.
4. Source: `Deploy from a branch`. Branch: `main`, folder: `/ (root)`. Save.
5. Wait ~1 minute. The pages will be live at:

   - `https://local-ai-app.github.io/legal/`
   - `https://local-ai-app.github.io/legal/privacy.html`
   - `https://local-ai-app.github.io/legal/terms.html`

## Enter in App Store Connect

Once the URLs are live:

- **App Information → Privacy Policy URL:** `https://local-ai-app.github.io/legal/privacy.html`
- **App Information → License Agreement / Terms of Use URL:** `https://local-ai-app.github.io/legal/terms.html`

When the paywall ships, also paste the Terms URL into the subscription group's **Review Information → License Agreement** field (or use Apple's Standard EULA if that's sufficient — but if you've defined a custom EULA here, link this one).

## Keeping content in sync

If/when the in-app Terms sheet is added to Snipit (`ios/Clip/Views/SettingsView.swift`), the in-app copy and `terms.html` must say the same thing. When you change one, update the other.

## Updating

When you change a policy:

1. Edit the relevant `.html` file
2. Update `Last updated: …` at the top
3. Commit and push — GitHub Pages rebuilds automatically within ~1 minute
4. If the change is material, also update the in-app version and bump the app version in App Store Connect
