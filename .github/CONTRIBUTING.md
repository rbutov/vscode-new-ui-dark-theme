## How to contribute

1. Fork and clone this repo. `git clone https://github.com/<YOUR-USERNAME>/new-ui-dark-theme`
2. Create a branch for your changes. `git checkout -b my-new-feature`
3. Install dependencies. `npm install`
4. Open the *visual-studio-code* folder in vscode.
5. Hack away.
6. Build and examine your changes in an Extension Development Host.
    * Debug > Start Debugging or use F5 as a shortcut
7. Commit and push your changes.
8. Submit a PR for discussion, keeping in mind that not all suggestions can be accepted.

## Publishing

VS Code uses the Microsoft Marketplace. Cursor uses Open VSX, so the theme must be published to both registries under `butov-dev.new-ui-dark-theme`.

Before the first Open VSX publication:

1. Sign in to [Open VSX](https://open-vsx.org/) with GitHub, connect an Eclipse Foundation account, and accept the Open VSX Publisher Agreement.
2. Create the `butov-dev` namespace and an Open VSX publishing access token.
3. Add that token to this GitHub repository's Actions secrets as `OVSX_PAT`. Never commit the token or include it in logs.

Publishing a GitHub release runs the existing Microsoft Marketplace deployment and the separate **Publish to Open VSX** workflow. Open VSX receives the release's `theme.vsix` asset, with its identity and version checked before upload. An Open VSX publishing failure does not prevent the Microsoft Marketplace job from running.

To publish an existing release, run **Actions → Publish to Open VSX → Run workflow** and enter its tag, for example `1.3.2`. A version that already exists on Open VSX is skipped, so the same release can be retried.
