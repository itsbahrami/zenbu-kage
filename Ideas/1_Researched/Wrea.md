# Wrea

- Stuff
  - https://glyph-md.github.io/
  - https://igorkha.github.io/markflow/
  - https://metaory.github.io/markon/

## Core Engine
- Markdown editor with live preview (split view)
- Simple configurable `<textarea />` as base
- Auto‑save to localStorage (debounced, every 500ms)

## Views
- Source view (raw text)
- Preview view (rendered Markdown)
- JSON Key:Value UI (edit structured data / RTL JSON)
- Split view (source + preview side‑by‑side)

## Controls (Toolbar)
- Font family switcher (monospace, Vazir/FA, Noto Sans/JP, sans‑serif)
- Font size slider/input
- Line wrap toggle (wrap / no‑wrap)
- Line height control
- Tab size selector (2, 4, 8)
- Show/hide line numbers

## Templates & Wizards
- Template system (Markdown skeletons with {{placeholders}})
- Conventional Commit wizard (type → scope → description → generate git command)
- Blog post wizard (title, tags, draft/publish, date)
- Letter wizard (recipient, purpose, tone → structured output)
- Code snippet wizard (language, description, tags → formatted block)

## File Operations
- Open file (File System API: showOpenFilePicker)
- Save to disk (File System API: showSaveFilePicker)
- Upload file (fallback input type="file")
- Download as: .md, .txt, .html, .json, .pdf
- Copy to clipboard
- Paste from clipboard

## Export / Import
- Export current document (MD, HTML, PDF, TXT, JSON)
- Import existing file (any supported format)
- Export/import Wrea settings (templates, font prefs, etc.)

## Statistics
- Word count
- Character count
- Line count
- Reading time estimate
- Language distribution (EN / FA / JA / etc.)
- Commit frequency (if connected to Azkhak)
- Daily writing streak

## Persistence & Sync
- localStorage (auto‑save draft)
- Manual save to disk (File System API)
- (Future) Sync across devices (via Zenbu backend)

## UI / UX
- Clean, minimal, distraction‑free UI
- Responsive (desktop + mobile)
- Dark / light mode toggle
- Keyboard shortcuts (Ctrl+S, Ctrl+Shift+P for preview, etc.)
