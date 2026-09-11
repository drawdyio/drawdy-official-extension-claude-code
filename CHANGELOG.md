# Changelog

## 1.0.1

### Added

- **Chat panel** opened from a Claude action button in the drawdy side rail, with drawer state preserved when closed and reopened.
- **API key connect screen** with `sk-ant-` format validation, show/hide toggle, and a back button to change the key later.
- **Secure key storage** via drawdy secure storage, with a session-only fallback and in-panel notice when storage is unavailable (e.g. signed out).
- **Model picker** for Sonnet 5 (default), Fable 5, Opus 5 and Haiku 4.5. Selection persists in kv storage.
- **Conversation persistence**: transcript (last 200 entries) saved to kv storage and restored on reopen.
- **File attachments** in the composer: PNG, JPEG, WebP, GIF images; PDF documents; text and code files (`.txt`, `.md`, `.csv`, `.json`, `.ts`, `.tsx`, `.js`, `.py`). Up to 8 files, 10 MB each, with image previews and removable chips.
- **Stop button** to abort a running turn while keeping whatever was already said or drawn.
- **Live status labels** during a turn (Thinking…, Reading the board…, Looking at the board…, Drawing…, Erasing…, Selecting…, Moving the camera…, Pointing…).
- **Board tools** available to Claude:
  - `read_board`: list elements with id, type, text, bounding rect and locked state (first 400).
  - `view_board`: screenshot the current viewport or a given world rect, with coordinate mapping in the result.
  - `get_selection`: describe the user's current selection.
  - `create_elements`: add shapes (rect, circle, diamond) with optional labels, text, lines, arrows, frames and URL images. Defaults to theme foreground color.
  - `delete_elements`: remove elements by id.
  - `select_elements`: set or clear the selection.
  - `zoom_to`: fly the camera to elements or a rect.
  - `annotate`: draw ephemeral laser-pointer strokes, then restore the user's previous tool.
- **Agent loop** with up to 16 tool rounds per turn, a 40-message context window that never opens mid tool-exchange, and history sanitization that drops dangling tool calls and turn-local screenshots.
- **Theme-aware UI**: drawdy styling injected as CSS variables and live-updated on theme change.
- **System prompt** tuned for canvas work: look before speaking, place new elements near related content, zoom to results, keep replies short, answer in the user's language.
- **Build tooling**: Rollup two-pass bundle (webview iframe app embedded into the driver), `.drawdyx` packing, and a Vite dev server on port 5173 serving `/built.drawdyx` and `/version` for live reload in drawdy.
