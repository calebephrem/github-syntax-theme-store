<br />
<div align="center">

  <img src="https://github.com/calebephrem/github-syntax-themes/blob/main/public/icon-stroke.png?raw=true" alt="GitHub Syntax Theme Store" width="200" height="200" />

  <p align="center" style="margin-top: 12px;">
    <strong><small>GitHub Syntax Themes</small></strong>
  </p>

</div>

# GitHub Syntax Theme Store

A centralized repository of syntax highlighting themes for the [GitHub Syntax Themes](https://github.com/calebephrem/github-syntax-themes) browser extension.

This store provides a collection of JSON theme files that define consistent syntax colors for GitHub code blocks, markdown snippets, etc.

## What It Does

The theme store acts as a **registry of themes**. Each theme is defined in a simple JSON format and can be loaded by the extension.

Themes describe:

- **Name** → Human‑readable theme name
- **Author** → GitHub username of the contributor
- **Type** → `light` or `dark`
- **SyntaxHighlighting** → Token colors for keywords, strings, comments, functions, etc.
- **Optional icon** → Theme preview icon

## Example Theme File

```json
{
  "$schema": "https://raw.githubusercontent.com/calebephrem/github-syntax-theme-store/refs/heads/main/schema.json",
  "name": "Dracula",
  "author": "dracula",
  "type": "dark",
  "description": "Classic dark theme with vibrant syntax colors",
  "syntaxHighlighting": {
    "comment": "#ffffff70",
    "constant": "#ffdd70",
    "constantNumeric": "#00ddee",
    "constantBuiltin": "#ffdd70",
    "keyword": "#86ff72",
    "keywordControl": "#86ff72",
    "string": "#aaff4f",
    "stringRegexp": "#00ddee",
    "variable": "#c0c0ff"
  }
}
```

## How It Works

- The **extension** fetches themes from this repository.
- Each theme JSON is validated against the **GitHub Syntax Themer Schema** (`schema.json`).
- The extension maps these values to GitHub’s internal syntax system (`.pl-*` classes and PrettyLights CSS variables).
- Users can switch themes from the extension popup.

## Contributing

We welcome contributions of new themes or improvements to existing ones.

To contribute:

1. Fork this repository.
2. Add your theme JSON file under the `themes/` directory.
3. Ensure your file matches the schema (`schema.json`).
4. Submit a pull request.

> [!TIP]
> Just provide the [schema.json](./schema.json) file along with a VS Code theme file of your choice to an AI agent, and it will generate a fully compatible theme file for you automatically. No manual writing needed ✨

Please include:

- Theme name and description
- Author (your GitHub username)
- Theme type (`light` or `dark`)
- SyntaxHighlighting values
- Optional icon URL

## Features

- Centralized theme registry for the extension
- Schema‑validated JSON format
- Easy contribution workflow via pull requests
- Supports both **light** and **dark** themes
- Compatible with GitHub’s legacy and modern syntax systems

## License

MIT © Caleb Ephrem
