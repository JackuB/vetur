# Contribution

**If you are reporting an issue, refer to [FAQ](https://github.com/vuejs/vetur/blob/master/docs/FAQ.md) instead.**

Contribution is welcome! There are many ways you could help Vetur's development:

- Writing Code
- Improving Doc
- Managing Issues

## Code

Comment on feature requests that you'd like to contribute before sending PR.

#### Coding Style

- Prettier with 120 print-width
- TSLint
- `const` over `let` whenever possible

#### Code Dev Guide

Vetur consists of 2 parts
- Language Client as a normal VS Code extension
- Vue Language Server

The language client launches Vue Language Server on port 6005 whenever a Vue file is opened.

To compile:

```bash
yarn
cd server && yarn && yarn compile
cd ../client && yarn
```

To debug:

- The extension has 2 configurations for debugging i.e client and server. 
- Run the client configurtion first. 
- As the client launches the language server lazily, open any .vue file so that the server is started. 
- Run the server configuration which binds the server code to port 6005 to enable debugging.
- At this point breakpoints in both server and client code should work. 

It should look like this:

![VScode Debugging](https://vuejs.github.io/vetur/images/debug.png)

#### Grammar Dev Guide

- Open the yaml files in `/syntax` with Sublime Text
- Install [PackageDev](https://github.com/SublimeText/PackageDev) if you haven't
- F7 to compile yaml grammar to tmLanguage files
- Run the `client` debug target in vetur project root

> Tip: In VS Code, use F1 -> Inspect TM Scopes:

![scope](https://github.com/vuejs/vetur/blob/master/asset/scope.png)

## Doc

PR that fixes grammar & typo or clarify & illustrate usage is welcome.

## Issues

- Answer other people's questions
- Make & ask for repro cases