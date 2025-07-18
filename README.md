

#  FileMaker Syntax Highlighting for VS Code

A syntax highlighter for **FileMaker custom functions** and expressions inside Visual Studio Code. Designed to highlight custom functions, user-defined variables, `Let` blocks, and nested expressions like `Case()` and `If()` 

---

##  Features

 Highlights:
- `Let ( [ x = 5 ; ... ] ; ... )` declarations  
- Variables `myValue`
- Built-in FileMaker functions (e.g., `Substitute`, `Evaluate`, `GetAsText`)
- User-defined function calls (e.g., `myCustomerFunction`)
- Nested expressions inside `Case()` and `If()` blocks
- Strings, numbers, operators, and comments (line `//` and block `/* ... */`)


---

##  Installation 

###  Option 1: From `.vsix` file

1. Download the latest `.vsix` release from the [Releases](https://github.com/craftyfm/filemaker-vscode-extension/releases) tab
2. Unzip 
2. In a VS Code terminal, run:

```bash
   code --install-extension path/to/filemaker-syntax-0.1.0.vsix
````

---

3. Open any `.fm`, `.fmfunc`, `.fmfn`, `.calc` or `.filemaker` file and select `FileMaker` as the language (bottom-right corner)

---

###  Option 2: From Source

```bash
git clone https://github.com/craftyfm/filemaker-vscode-extension.git
cd vscode-filemaker-syntax
npm install -g @vscode/vsce
vsce package
code --install-extension ./filemaker-syntax-0.1.0.vsix
```

---

##  Language Support

The extension targets the following file types:

* `.fmfunc`
* `.filemaker`
* `.fm`
* `.fmfn`
* `.calc`

You can manually set the language to `FileMaker` in VS Code if auto-detection does not occur.

---

##  Theme Compatibility

This extension is compatible with all VS Code themes. For best results, we recommend:

* **Dark+**
* **Monokai**
* **One Dark Pro**

To customize token colors, add `editor.tokenColorCustomizations` in your `settings.json`.

---

##  Sample Scopes

| Element               | Scope                               |
| --------------------- | ----------------------------------- |
| `Let` variables       | `variable.parameter.let.filemaker`  |
| `myVar` / `$$global`  | `variable.other.filemaker`          |
| Unscoped vars         | `variable.other.unscoped.filemaker` |
| Function calls        | `entity.name.function.filemaker`    |
| Built-in functions    | `support.function.filemaker`        |
| Case results          | `variable.result.case.filemaker`    |
| Strings               | `string.quoted.double.filemaker`    |
| Block comments        | `comment.block.filemaker`           |

Use `Developer: Inspect Editor Tokens and Scopes` to inspect live.

---

##  Development

To work on the extension:

1. Clone the repo
2. Run in development mode:

```bash
code .
F5 → Extension Development Host
```

Open test files like `sample.fm` to preview highlighting in real time.

---

##  License

MIT License
Copyright © 2025 Stuart Russell

---

##  Contributing

Pull requests are welcome! Please include test cases and follow the structure of the existing grammar.
Feel free to submit improvements to the scope coverage or styling. Start an issue or discussion.

---

##  Links

* [FileMaker Official Docs](https://help.claris.com/en/pro-help/)
* [TextMate Grammar Reference](https://macromates.com/manual/en/language_grammars)
* [VS Code Extension API](https://code.visualstudio.com/api)

---

*Built for FileMaker developers who want better tools.*

```

