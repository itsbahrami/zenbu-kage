# Lyricist

## 1. Core Concept (The "Matrix")

- **Configurable columns**, not hardcoded languages.
  - You define the columns yourself: e.g., "Japanese", "English", "فارسی", "Romaji", "Korean"—anything.
  - Each column has its own **font** (e.g., Klee One for Japanese, Vazirmatn for Persian, Inter for English).
  - Each column has its own **text direction** (LTR or RTL).
- **Rows** are lyric lines. Each row has one cell per column.

---

## 2. Import / Input

- **Import from CSV/TSV** – you prepare the lyrics in Excel/Google Sheets, import them, and the app reads the columns automatically.
- **Manual entry** – you can add rows one by one inside the app.
- **Paste full lyrics** – paste a block of text, and the app splits it into rows (by newlines).

---

## 3. Editing (The 90% Modal)

- Click any cell in the table → opens a **huge modal** (takes up ~90% of the screen).
- Inside the modal, you can edit that one cell comfortably.
- The modal **respects the column's font and direction** while typing (so Persian feels native, Japanese looks correct).
- You can edit timestamps (start/end) for each line.

---

## 4. Furigana (Japanese Ruby Text)

- Special syntax: `[Kanji](Furigana)` → e.g., `[君](きみ)` becomes 君 with きみ on top.
- **Three display modes** (toggleable):
  - **Always on** – furigana is always visible.
  - **Hover only** – furigana appears when you hover over the kanji.
  - **Off** – no furigana shown.
- Furigana can be **colored** differently from the main text.

---

## 5. Playback & Sync

- **Load audio or video** (MP3, MP4, etc.) into the player.
- As the media plays, the **current lyric line is highlighted** in the table/player.
- You can **jump** to a specific line by clicking on it.

---

## 6. Player Modes (Templates)

The app has different **visual skins** depending on the content:

- **"Anime" mode** – background is the cover art (blurred), big Japanese lyrics with furigana centered.
- **"Music" mode** – cover art shown as a floating image, lyrics scroll on the side (like Spotify).
- **"Podcast" mode** – no cover art, full-width clean background, longer text blocks with bigger line-height.
- You can switch modes manually, or the app can auto-detect based on the content.

---

## 7. Audio Visualizer

- **Volume-reactive bars** – lines that go up and down based on the music's volume/frequency.
- Can be toggled on/off.

---

## 8. Export

Export your project to multiple formats:

- **CSV** – back to spreadsheet format (preserves all columns).
- **LRC** – standard lyric format (simple timestamps + text).
- **SRT** – subtitle format.
- **VTT** – web subtitle format.
- **Custom JSON** – exports everything (columns, fonts, directions, furigana data, settings).

---

## 9. Project Management

- **Save projects** locally (in your browser) – reopen them later.
- **Name your projects** and add **tags** (e.g., "anime", "j-pop", "podcast").
- **Delete** or **duplicate** projects.

---

## 10. UI/UX Polish

- **Dark / Light mode** toggle (optional).
- **Table view** shows all rows and columns at a glance.
- **Player view** is immersive – you switch between them via tabs.
- **Line visibility** – you can hide/show specific lines in the player (if you want to focus on certain parts).

---

## 11. (Optional) Collaboration / Cloud

- Save projects to the cloud (if you add a backend later).
- Share a project with a link (read-only or editable).
