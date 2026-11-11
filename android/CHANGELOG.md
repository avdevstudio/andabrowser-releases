# Anda Browser for Android: changelog

Newest first. Each version is a release tagged `android-v<version>`; its APK and `SHA256SUMS` are attached to the
release, and the checksums are also in `android/<version>/SHA256SUMS`.

## 1.0.0-beta.4 (2026-11-11)

The fourth public beta: bookmarks and saved passwords can now be brought in from another browser and taken out again,
sorted and undone; start-up and movement are noticeably smoother; switching users is faster. Users get profile pictures,
names, a new lock screen and biometric unlocking; wallpapers and search suggestions are renewed.
Includes GeckoView 159.0.20261022150525 by Mozilla (unchanged since beta.3); its exact source is attached to the release.

- `AndaBrowser-1.0.0-beta.4-arm64-v8a.apk` (arm64-v8a, Android 8.0 or newer)
- SHA-256: `94e8d9a2bf88ebdc96d3e8f760160c7c6180477adc46c49cf94b30dd1275e768`

### New

- **Biometric unlocking for Users.** If you switch it on, you can open your profile with biometrics (for example your fingerprint) instead
  of typing the password; the password always stays available. An administrator can turn it off in Anda Lock. Not for guests.
- **Bookmarks import and export** in the standard HTML format.
- **Saved passwords import and export** as CSV. After an import we warn that the file holds readable passwords and offer
  to delete it. Large files import quickly.
- **Sort bookmarks** by name, newest or oldest.
- **Undo** after deleting a bookmark, on the list or with the address bar star.
- **Bookmark nicknames:** type a short word in the address bar to open the page.
- **Add a password by hand**, and a **note** per password (stored encrypted; kept in CSV).
- **Strong password suggestion** when you sign up.
- **Weak and repeated passwords** are flagged, only on your device.

### Users

- **"Who is using this?"** If you switch it on, the browser asks who is using it at start-up and after Quit. Quit means a
  fresh start; a guest is cleared on quit according to its setting.
- **Profile pictures** on the lock screen, the picker and the lists: a letter, one of 12 symbols, or your own image.
- **Names:** profiles can be renamed and named when created; two profiles cannot share a name. On a new install the first
  profile is called "User 1".
- **New lock screen:** name and picture, Sign in under the password field (Enter signs in too), "Another user" at the bottom.
  Centred on tablets, two columns on a wide landscape screen; the page stays when you rotate.
- **Consistent look:** on the user and Anda Lock screens buttons are left-aligned rows with icons and input fields are filled
  bands; the user switcher in the menu follows the menu style; "Who is using this?" is centred.

### Wallpapers

- **Tabs:** its own wallpaper picker, separately for light and dark; by default the second image of the list (built in, shown
  without a download).
- **Sign-in:** the wallpaper of "Who is using this?" and the lock screen, separately for light and dark; shared by all users,
  and any of them can change it. By default the second image of the list.

### Search

- **Suggestions as you type:** the first time you type, the browser asks once whether you want suggestions from your search
  engine (what you type is then sent to it). Off by default; works with DuckDuckGo, Startpage and Qwant; never asked in private
  tabs or under the parental lock.
- No AI row among the suggestions in normal search; AI is one switch away.
- **"What was blocked?"** The ad blocker shows what it filtered by category; the rest is "Other blocked item".

### Motion and speed

- User switching happens in one window with a cross-fade.
- Faster start-up: one window, plus a Baseline Profile.
- Settings and Anda Security pages slide together with a spring; predictive back shows a preview.
- The address bar and focus panel move with the keyboard; light haptics at gesture thresholds.
- No flashes on the home page, a restored web tab or native pages; home icons no longer pop in.
- The switch screen shows the target user's name.
- New profiles start with a permissive Anda Lock (everything allowed, restrict later). Still locked: saved passwords, Safe
  Browsing, HTTPS-only, DoH, private-browsing protection, filter unlock.

### Smaller changes

- **Quit** is always the last row of the menu.
- An X on the recent AI questions, and on recent searches in the address bar.
- New order in Settings; bookmarks sit under Backup and restore.

### Fixes

- **Tabs (about:tabs):** closing a tab no longer closes the page, no jitter while dragging, the search field is visible
  with the keyboard open; only icons while searching on a phone.
- The delete-password dialog no longer slides under the card; no device check after a master password.
- One password prompt per visit.
- Case-insensitive name sorting.
- The system splash no longer sticks over the browser on cold start.

### Known limitations

- Bookmark folders are one level deep; a deeper tree does not round-trip with Anda Desktop.
- The password CSV is plain text: delete it after use.
- The Baseline Profile covers cold start only, not yet the browsing path.
- Biometric unlocking works only with strong (Class 3) biometrics; whether that is fingerprint, face or iris depends on the
  device. The unlock dialog belongs to the system, its look is not Anda's.
- On an existing install the first profile keeps its name; it can be renamed under Users.

## 1.0.0-beta.3 (2026-11-08)

The third public beta: Users (several profiles on one device, each with its own history, cookies, passwords and
settings, an optional password per user, and a guest mode); our own ad blocker built on Brave's adblock-rust engine
with the EasyList, EasyPrivacy and hufilter lists, including cosmetic filtering; smoother start-up and user switching.
Includes GeckoView 159.0.20261022150525 by Mozilla, the same as beta.2; its exact source is attached to the release.

- `AndaBrowser-1.0.0-beta.3-arm64-v8a.apk` (arm64-v8a, Android 8.0 or newer)
- SHA-256: `cc84480ce767dbb13201742770ced3855f2cb247939df786393008463ad3b291`

## 1.0.0-beta.2 (2026-11-03)

The second public beta: Anda Security in one place (Protection, Permissions, Sites and data, Passwords and autofill,
with Anda Lock on top); real tracking protection with a natively rebuilt shield panel; a tidy All sites list; notes with
pictures and folders; a saved passwords page; quieter translation offers; 40 languages for every new text.
Includes GeckoView 159.0.20261022150525 by Mozilla; its exact source is attached to the release.

- `AndaBrowser-1.0.0-beta.2-arm64-v8a.apk` (arm64-v8a, Android 8.0 or newer)
- SHA-256: `bf67574cfec8d53cde7e5b24ee2d9c54a3b8a6a07a5a86e9ea010de0c25d5e9b`

## 1.0.0-beta.1 (2026-10-24)

The first public beta: 40 languages; Anda Security (ad and tracker blocking, blocked sites, a lock that protects your
settings with a master password); Notes (quotes you can open on the page again, checklists, Markdown export,
sharing); moving the address bar and the tab strip by dragging; built-in wallpapers; custom colour palettes.
Includes GeckoView 158.0.20261021001945 by Mozilla; its exact source is attached to the release.

- `AndaBrowser-1.0.0-beta.1-arm64-v8a.apk` (arm64-v8a, Android 8.0 or newer)
- SHA-256: `c5d840e8cc64ee74cb31b4e10250545808239b1332ad8dd6de2f5ca5ec059667`
