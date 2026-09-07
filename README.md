# Zed Datastar Snippets

A collection of [Datastar](https:/data-star.dev/) `data-*` attribute snippets for [Zed editor](https://zed.dev/), designed to speed up hypermedia-driven frontend development with intelligent autocomplete and placeholder support.

## ✨ Features

- **Full Attribute Coverage**: Snippets for all core and pro Datastar `data-*` attributes
- **Smart Placeholders**: Tab-navigable placeholders for signal names, expressions, and event names
- **Reactive Signals**: Snippets for `data-signals`, `data-bind`, `data-computed`, and more
- **Backend Actions**: Quick scaffolding for `data-on:click`, `data-on-intersect`, `data-on-signal-patch`
- **Pro Attributes Included**: `data-animate`, `data-persist`, `data-match-media`, `data-view-transition`, and others

## 📦 Installation

### Via Zed Extensions (Recommended)

1. Open Zed editor
2. Press `Cmd/Ctrl + Shift + P` to open the command palette
3. Type "extensions" and select `zed: extensions`
4. Search for "Datastar Snippets"
5. Click "Install"

### Manual / Dev Installation

1. Clone this repository:
```bash
   git clone https://github.com/sumit/zed-datastar-snippets
```

2. In Zed, open the command palette and run `zed: install dev extension`

3. Select the cloned folder (the one containing `extension.toml`)

## 🚀 Usage

Start typing any Datastar attribute prefix inside an HTML (or supported template) file, and matching snippets will appear in the autocomplete menu.

### Quick Start Examples

| Prefix | Output | Description |
|--------|--------|-------------|
| `data-bind` | `data-bind="$1"` | Two-way bind a signal to an element |
| `data-on:click` | `data-on:click="$1"` | Run an expression when clicked |
| `data-signals` | `data-signals="{$1: $2}"` | Merge one or more signals |
| `data-text` | `data-text="$1"` | Set element text to an expression |
| `data-show` | `data-show="$1"` | Show/hide based on an expression |

## 📋 Available Snippets

### Reactivity & Signals
- `data-signals` / `data-signals:*` - Declare or merge signals
- `data-bind` / `data-bind:*` - Two-way signal binding
- `data-computed` / `data-computed:*` - Derived/computed signals
- `data-ref` / `data-ref:*` - Signal referencing an element
- `data-indicator` / `data-indicator:*` - Track in-flight requests

### Events & Actions
- `data-on:*` - Generic event listener
- `data-on:click` - Click handler
- `data-on:keydown` - Keydown handler
- `data-on-intersect` - Viewport intersection
- `data-on-interval` - Recurring interval
- `data-on-signal-patch` / `data-on-signal-patch-filter` - React to signal changes

### DOM & Styling
- `data-attr` / `data-attr:*` - Set attribute values
- `data-class` / `data-class:*` - Conditional classes
- `data-style` / `data-style:*` - Conditional inline styles
- `data-text` - Reactive text content
- `data-show` - Conditional visibility

### Lifecycle & Behavior
- `data-init` - Run on initialization
- `data-effect` - Run on load and signal change
- `data-ignore` / `data-ignore-morph` - Exclude from processing/morphing
- `data-preserve-attr` - Preserve attribute across patches

### Pro Attributes
- `data-animate:*` - Animate attributes over time
- `data-persist` / `data-persist:*` - Persist signals to local storage
- `data-match-media:*` - Sync a signal to a media query
- `data-view-transition` - View Transition API integration
- `data-on-raf` / `data-on-resize` - RAF and resize hooks
- `data-query-string` - Sync signals with query string
- `data-replace-url` - Replace browser URL
- `data-scroll-into-view` - Scroll element into view
- `data-custom-validity` - Custom form validity
- `data-json-signals` - Reactive JSON dump of signals
- `data-nonce` - CSP nonce support

## 🎯 Smart Placeholders

Snippets use numbered placeholders (`$1`, `$2`, etc.) you can tab through:

```html
<!-- Typing 'data-signals' + Tab -->
data-signals="{$1: $2}"
<!-- Tab to $1 for signal name, Tab to $2 for expression -->
```

## 🛠️ Customization

You can modify or extend snippets by editing `snippets/html.json`. Each entry follows this structure:

```json
{
  "Snippet Name": {
    "prefix": "trigger-text",
    "body": "data-example:${1:name}=\"${2:expression}\"",
    "description": "What this attribute does."
  }
}
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup

1. Fork the repository
2. Clone your fork
3. Make your changes to `snippets/html.json`
4. Test via `zed: install dev extension` in Zed
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Datastar](https://data-star.dev/) team for the framework and reference docs
- [Zed Team](https://zed.dev/) for creating an extensible editor
- Community feedback and contributions

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/sumit/zed-datastar-snippets/issues)
- **Datastar Discord**: [Datastar Discord](https://discord.gg/bnRNgZjgPh)
- **Zed Documentation**: [Zed Documentation](https://zed.dev/docs)

---

**Happy hacking with Datastar + Zed! 🚀**
