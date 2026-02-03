# Obsidian AI Assistant Plugin

Use **AI Assistant** in the Obsidian editor. This plugin is a bridge between the Obsidian editor and AI services.

-   🤖 Get inline suggestions as you type
-   💬 Use the AI Chat service to ask questions about your notes

## 🗒️ Requirements

-   Network connection to send and receive data from the AI service
-   Node.js 22 or later

## ⚙️ Installation

1. Install the plugin via the Obsidian community plugins browser.
2. Activate the plugin in the settings. Make sure to configure any necessary options.
3. Configure the path to the Node +22 binary in the plugin settings (required for inline suggestions). You can find it by running `which node` in your terminal.

## 🤖 AI Assistant Inline

### Usage

1. Open a note in Obsidian.
2. Write something in the editor.
3. After a small pause, the AI will suggest completions for your text.
4. Press `Tab` to accept a suggestion or `Esc` to dismiss it.

### Features

-   [x] Use AI completion in the Obsidian editor
-   [x] Configure the suggestion generation delay
-   [x] Configure your bindings to accept, dismiss, trigger or partially accept suggestions
-   [x] Configure if you want to see automatic suggestions or only trigger them manually
-   [x] Configure if you want to see suggestion only in code blocks or in the whole note
-   [x] Exclude folders and files from the suggestion generation

### Known issues

-   If you installed Obsidian with Flatpak, you might need to use NVM to handle Node.js versions as the default binary path is not accessible in the Flatpak sandbox.
-   "Tab" completion can be buggy in some cases (e.g. in bullet points in LateX Math mode for example). It depends on plugin priority over the keybindings.

## 💬 AI Assistant Chat

### Usage

-   Open the AI Chat in the right sidebar.
-   Choose a model to use.
-   Ask a question and link a note like you would do in the obsidian editor (e.g. `Can you summarize this note [[my note]]?`).

### Features

-   [x] Use AI Chat in the Obsidian editor
-   [x] Choose the model to use
-   [x] Implement a chat history
-   [x] Link notes with [[double bracket syntax]] in the chat
-   [x] Configure a custom prompt as a system message in the settings
-   [x] Let the user choose the default behavior of the enter key (send message or add a new line)
-   [x] **Mermaid diagram support** - Render Mermaid diagrams in chat responses

### Mermaid Diagrams

The chat supports rendering Mermaid diagrams when the AI responds with Mermaid code blocks. Simply ask the AI to create a diagram and it will render visually in the chat.

**Example usage:**

````
You: Can you create a flowchart showing the software development lifecycle?

AI: Here's a flowchart of the software development lifecycle:

```mermaid
flowchart TD
    A[Requirements Analysis] --> B[Design]
    B --> C[Implementation]
    C --> D[Testing]
    D --> E[Deployment]
    E --> F[Maintenance]
    F --> A
````

**Supported diagram types:**

-   Flowcharts
-   Sequence diagrams
-   Class diagrams
-   State diagrams
-   Gantt charts
-   Pie charts
-   And more...

The diagrams automatically adapt to your Obsidian theme (light/dark mode) and are fully integrated into the chat interface.
