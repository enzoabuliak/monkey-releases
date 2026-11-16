# Monkey releases

Downloads and the update feed for **Monkey**, an Arc-style browser for macOS built on [Helium](https://github.com/imputnet/helium) (Chromium). Arc stops working on December 22, 2026; Monkey keeps its sidebar, Spaces, Command Bar, Split View, Peek, Little Arc, Boosts and the rest.

## Install

Monkey needs a Mac with Apple silicon (M1 or later) and macOS 13 or newer.

1. Download the newest `monkey_<version>_arm64-macos.dmg` and its `.sha256` from [Releases](../../releases).
2. Optional but recommended: check the download. In Terminal, in the folder with both files:
   `shasum -a 256 -c monkey_<version>_arm64-macos.dmg.sha256`
3. Open the `.dmg` and drag Monkey to Applications.

### The first launch

Monkey isn't signed with an Apple Developer ID yet, so macOS blocks it the first time:

1. Open Monkey. macOS says it can't verify it; click **Done** (not Move to Trash).
2. Open **System Settings → Privacy & Security**, scroll to "Monkey was blocked…", click **Open Anyway** and confirm with your password.

From Terminal instead: `xattr -dr com.apple.quarantine /Applications/Monkey.app`.

After an update, macOS may ask once for your login password when Monkey reads its saved passwords ("Monkey wants to use … Monkey Safe Storage"); choose **Always Allow**.

## Updates

Monkey checks this repo for updates when it starts and in the background, downloads them, and installs them the next time you quit. Each update is checked against an EdDSA signature before it's installed. To turn this off, switch off "Allow automatic browser updates" in Monkey's settings.

`mac/appcast-arm64.xml` is the feed it reads.

## Coming from Arc

Monkey can import your Arc sidebar (Spaces, pinned tabs, folders and Favorites) with "Import Arc Sidebar" in the Space menu. Your Arc data isn't changed.

## Source

Monkey is free software under the GNU GPL v3, like Helium and Chromium. Its source isn't public yet; if you have a copy of Monkey, ask the maintainer and you'll get the corresponding source.
