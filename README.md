# Claude Canvas for drawdy

Chat with Claude about your board, right inside drawdy. Claude can read your elements, look at the canvas, and draw directly on it to sketch, annotate, or answer questions.

## Before you start

You need two things:

1. **A drawdy account, signed in.** Signing in lets the extension remember your API key between sessions.
2. **An Anthropic API key.** Create one at [console.anthropic.com/settings/keys](https://console.anthropic.com/settings/keys). Usage is billed to your Anthropic account, not to drawdy.

## Step 1: Install the extension

Install the `drawdy-claude-canvas.drawdyx` file through drawdy's extensions manager. Once installed, an orange Claude icon appears in the side rail.

## Step 2: Open the panel

Click the orange Claude icon in the side rail. The chat panel slides open as a drawer. Closing and reopening it keeps your conversation.

## Step 3: Connect your API key

The first time you open the panel you'll see **Connect your Anthropic API key**.

1. Go to [console.anthropic.com/settings/keys](https://console.anthropic.com/settings/keys).
2. Click **Create Key** and copy it.
3. Paste it into the field. It should start with `sk-ant-`.
4. Press **Connect** or hit Enter.

Tips:

- Use the eye icon to show or hide the key while typing.
- If you see *This key doesn't look right*, check that you copied the whole key.
- To change the key later, click the **‹** back button at the top-left of the chat panel.
- If you're signed out of drawdy, the key is kept for this session only and a notice appears in the panel. Sign in to have it remembered.

## Step 4: Chat

Type in the box at the bottom and press **Enter** to send. **Shift+Enter** adds a new line.

While Claude works, a status line shows what it's doing: *Thinking…*, *Reading the board…*, *Looking at the board…*, *Drawing…*, *Pointing…* and so on. Press the **Stop** button (square icon) to interrupt. Anything Claude already said or drew stays.

Claude replies in whatever language you write in.

## Step 5: Attach files (optional)

Click the **+** button to attach files to your message. You can pick several at once.

| Type | Formats |
| --- | --- |
| Images | PNG, JPEG, WebP, GIF |
| Documents | PDF |
| Text and code | `.txt`, `.md`, `.csv`, `.json`, `.ts`, `.tsx`, `.js`, `.py` |

Up to 8 files per message, 10 MB each. Remove a file before sending with the **×** on its chip.

## Step 6: Pick a model (optional)

Use the pill next to the **+** button to switch models. Your choice is remembered.

| Model | Best for |
| --- | --- |
| Sonnet 5 (default) | Everyday board work, fast and capable |
| Fable 5 | The hardest reasoning and layout tasks |
| Opus 5 | Deep, careful work |
| Haiku 4.5 | Quick, low-cost answers |

## What Claude can do on your board

You don't need to name these. Just describe what you want and Claude picks the right action.

| Claude can | Example |
| --- | --- |
| Read the board | "What's on this board?" |
| Look at the board | "Does this layout look balanced?" |
| Read your selection | "Explain this" (with elements selected) |
| Create shapes, text, lines, arrows, frames and images | "Draw a login flow with three boxes" |
| Delete elements | "Remove the duplicate arrows" |
| Select elements | "Highlight everything that mentions pricing" |
| Move your camera | "Zoom to the diagram you just made" |
| Point with a laser | "Point at the part that's misaligned" |

The laser is a temporary red trail that fades after about a second. It leaves nothing on the board. For permanent marks, ask Claude to draw instead.

New elements use your theme's default colors unless you ask for specific ones.

## Example prompts

- "Summarize what's on this board."
- "Sketch a three-step signup flow to the right of the selected frame."
- "Turn these sticky-note ideas into a grouped mind map."
- "Point at anything on screen that looks misaligned."
- "Delete the duplicate arrows in the top-left."
- "Here's a screenshot of our old design (attached). Recreate the layout as wireframe boxes."
- "Draw a diamond decision node between the two rectangles and connect them with arrows."
- "Add a frame around everything and label it 'Sprint 12'."

## Privacy

- Your API key is sent only to `api.anthropic.com` and stored in drawdy's secure storage for this extension. It never goes to drawdy's servers.
- Board content Claude reads (element lists, screenshots) is sent to Anthropic as part of your conversation so it can answer. Screenshots are dropped from history after the turn they were taken in.
- Your chat history (last 200 messages) and model choice are stored in drawdy's storage for this extension.

## Troubleshooting

**"Add your Anthropic API key first."**
You sent a message before connecting a key. Click **‹** and connect one.

**"Invalid API key: …"**
Anthropic rejected the key. Check it's active and has credit at [console.anthropic.com](https://console.anthropic.com).

**"Permission to store the key is denied."**
Secure storage isn't available, usually because you're signed out. The key still works for this session.

**"I stopped after 16 steps."**
The task needed more actions than one turn allows. Reply "continue" and Claude picks up where it left off.

**The laser pointer doesn't show.**
The trail only paints where you're looking. Say "zoom in and point at it" so Claude moves the camera first.

**No Claude icon in the side rail.**
The extension didn't register. Reinstall the `.drawdyx` file.
