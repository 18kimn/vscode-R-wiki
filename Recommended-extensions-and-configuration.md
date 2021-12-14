Besides the recommended tools from the
[Getting Started](https://github.com/REditorSupport/vscode-R/wiki/Getting-Started)
page, we also recommend using the following to find features like those in
RStudio.

## Dots in variable/function names

Treat `names.like.this` as one word for selection.

In VSCode's `settings.json`, add the following:

```json
"[r]": {
    "editor.wordSeparators": "`~!@#%$^&*()-=+[{]}\\|;:'\",<>/?"
}
```

## C/C++

We recommend the
[C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
VSCode extension with the following settings to write Rcpp:

In `.vscode/c_cpp_properties.json`:

```json
{
  "configurations": [
    {
      "name": "Linux",
      "includePath": [
        "${workspaceFolder}/**",
        "${env:HOME}/R/x86_64-pc-linux-gnu-library/3.6/Rcpp/include",
        "/usr/share/R/include"
      ],
      "defines": [],
      "compilerPath": "/usr/bin/gcc",
      "cStandard": "c11",
      "cppStandard": "c++17",
      "intelliSenseMode": "clang-x64"
    }
  ],
  "version": 4
}
```

`.clang-format`:

```yaml
---
Language: Cpp
BasedOnStyle: LLVM
Standard: Cpp11
ReflowComments: false
---
```

In your `settings.json`:

```json
"C_Cpp.commentContinuationPatterns": [
    "/**",
    "//'"
]
```

See demonstration and more tooling at
[renkun-ken/vscode-rcpp-demo](https://github.com/renkun-ken/vscode-rcpp-demo)

## Path Autocomplete

We recommend the VSCode extension
[Path Autocomplete](https://marketplace.visualstudio.com/items?itemName=ionutvmi.path-autocomplete)
with the following configuration in `settings.json` to enable autocompletion for
file names:

```json
"path-autocomplete.pathMappings": {
    "/": "/",
    "./": "${folder}"
}
```

## Error Lens

You can use the
[Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
extension for more visible error messages.
