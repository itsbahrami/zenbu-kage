# Kana Dikteh

- 仮名 + دیکته
- In English word order... 😂

## Project: Kana Dictation (Paper-First)

**Concept**
A minimal, deliberate-practice tool for learning to *write* Hiragana and Katakana from memory. The app acts solely as a prompter and error tracker. All writing is done on paper—no on-screen tapping or drawing. This forces true recall (retrieval practice) and builds motor memory.

**Core Philosophy**
- **Retrieval > Recognition**: Seeing the romaji and producing the kana on paper is far more effective than multiple-choice.
- **Track only failure**: The app doesn't log correct answers. It only stores a "pain counter" for each `{romaji}-{type}` pair. The higher the number, the more often you've gotten it wrong.
- **Weighted randomness**: Questions are pulled from the selected pool using a weighted random algorithm. High-pain items appear more frequently, driving deliberate practice at your exact weak spots.

**Workflow**
1. User selects included sets (Basic, Dakuten, Youon) and types (Hiragana/Katakana).
2. App shows a prompt: `{romaji} [{H/K}]` (or plays audio).
3. User writes the character on paper.
4. User clicks **Reveal** to see the correct kana.
5. User self-grades:
   - **Correct**: App does nothing.
   - **Wrong**: App increments the pain counter for that item by 1.
6. At the end of the session, the app displays the current "Weak List" (all items with pain > 0).

**Data Persistence**
- Uses `localStorage` for persistent tracking across sessions.
- Pain counter is a flat JSON object: `{ "shi-H": 5, "tsu-K": 3 }` (items not in the object are treated as 0).
- Supports **Import/Export** of the entire stats JSON, allowing users to backup their weak list or transfer it between devices.

**Target User**
Japanese beginners (pre-N5) who can already *read* kana but struggle to *write* them from memory. Also suitable for anyone who prefers physical handwriting and wants a focused, distraction-free practice tool.
