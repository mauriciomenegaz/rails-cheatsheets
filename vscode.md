# VS Code setup

## Extensions

Main ones:

- gitlens
- ruby LSP (Shopify)
- Standard Ruby (Test Double)

Nice to have

- drawio - https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio

## Other settings

- default formatter: `"[ruby]": {"editor.defaultFormatter": "testdouble.vscode-standard-ruby"}`
- After installing ruby LSP, disable diagnostics (by clicking on "{}" on the bottom bar)
- emmet settings: Preferences / search for "emmet: include languages" / add one item (erb -> html)
- configure titlebar: Preferenches / search for "title" / enter this: ${dirty}[${rootName}]${separator}VS Code
- tab close button on left (`"workbench.editor.tabActionLocation": "left"` on settings json)
- do not move the directory tree when closing a file: `"explorer.autoReveal": false`
- vertical ruler at 120 characters: `"[ruby]": {"editor.rulers": [120]}`


## Links

https://railsnotes.xyz/blog/vscode-rails-setup
