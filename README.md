# Obsidian Autocomplete Plugin

> [!IMPORTANT]
> This plugin was created because I don't normally use chat in Obsidian; I only use it for inline suggestions. Also, the original plugin has an annoying bug when used with [Lazy Plugin](https://github.com/alangrainger/obsidian-lazy-plugins).

Use **AI Autocomplete** in the Obsidian editor. This plugin is a bridge between the Obsidian editor and AI services.

-   🤖 Get inline suggestions as you type

## 🗒️ Requirements

-   Network connection to send and receive data from the AI service
-   Node.js 22 or later

## ⚙️ Installation

1. Install the plugin via the Obsidian community plugins browser.
2. Activate the plugin in the settings. Make sure to configure any necessary options.
3. Configure the path to the Node +22 binary in the plugin settings (required for inline suggestions). You can find it by running `which node` in your terminal.

## 🤖 AI Autocomplete Inline

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
