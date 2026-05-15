# zed-nsis-extension

> NSIS language support for the [Zed](https://zed.dev) editor.

![GitHub Release](https://img.shields.io/github/v/release/idleberg/zed-nsis-extension?style=for-the-badge)
[![CI](https://img.shields.io/github/actions/workflow/status/idleberg/ardent/ci.yml?style=for-the-badge)](https://github.com/idleberg/ardent/actions)

![Screenshot](https://raw.githubusercontent.com/idleberg/zed-nsis-extension/main/resources/screenshot.png)

## Features

- Syntax highlighting of NSIS files
- Formatting via the `ardent` formatter
- Code completions
- Diagnostics mode
- Go to definition

## Installation

### Manual Installation

Until this extension is published to the Zed extension registry, you can install it manually as a dev extension:

1. Clone the repository:

   ```sh
   git clone https://github.com/idleberg/zed-nsis-extension.git nsis
   ```

2. Open Zed
3. Open the command palette (<kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>)
4. Search for "zed: install dev extension"
5. Select the cloned `nsis` directory

Zed will build the extension from source and install it. The extension will persist across restarts but won't auto-update — pull the latest changes and reinstall to update.

### Extension Registry

Once published, you can install from the Zed extension registry:

1. Open Zed
2. Open the command palette (<kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>)
3. Search for "zed: extensions"
4. Search for "NSIS" and install

## Configuration

Add the following to your Zed `settings.json` to enable format on save:

```json
{
	"languages": {
		"NSIS": {
			"format_on_save": "language_server"
		}
	}
}
```

### Formatting Options

The formatter respects Zed's built-in editor settings for the NSIS language:

| Setting     | Type   | Default | Description                                   |
| ----------- | ------ | ------- | --------------------------------------------- |
| `hard_tabs` | `bool` | `true`  | Indent with tabs instead of spaces            |
| `tab_size`  | `int`  | `2`     | Spaces per indent level (when not using tabs) |

Example with custom settings:

```json
{
	"languages": {
		"NSIS": {
			"format_on_save": "language_server",
			"hard_tabs": false,
			"tab_size": 4
		}
	}
}
```

## License

This work is licensed under the [Apache License, Version 2.0](LICENSE-APACHE) or [The MIT License](LICENSE-MIT).
