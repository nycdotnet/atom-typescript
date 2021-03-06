# Atom TypeScript

[![Join the chat at https://gitter.im/TypeStrong/atom-typescript](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/TypeStrong/atom-typescript?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

JavaScript developers can now just open a `.ts` file and start hacking away like they are used to. No `grunt` no `Visual Studio`. Just pure coding.

## Installation

1. Install [atom](https://atom.io).
2. `apm install atom-typescript` (`apm` needs `git` in your path)
3. Fire up atom. Wait for the message: `AtomTS: Dependencies installed correctly. Enjoy TypeScript ♥` **It may take up to 5 minutes for this message to appear. Be patient!**

**Additional Notes**: [Some packages we love](https://github.com/TypeStrong/atom-typescript/blob/master/docs/packages.md).

## Reviews
*Featured on the TypeScript home page under tools http://www.typescriptlang.org/*  
"I was shocked at how good it felt to poke around on the compiler with it." [Jonathan Turner](https://twitter.com/jntrnr)  
"And guess what, it worked perfectly. Like everything else! Faster than Visual Studio!" [Daniel Earwicker](http://stackoverflow.com/users/27423/daniel-earwicker)  
"It's a thing of beauty - they had me at '*Type information on hover*'. Discovering  `tsconfig.json` support as well was just an enormous bonus." [John Reilly](https://twitter.com/johnny_reilly)  
"This may be your best option for editing TypeScript at the moment - very nice!" [Rasmus Schultz](https://twitter.com/mindplaydk)

[*Add yours!*](https://github.com/TypeStrong/atom-typescript/issues/66)

# Features
* Autocomplete
* Live error analysis
* Type information on hover
* Compile on save
* Project Context Support (`tsconfig.json`)
* Project Build Support
* Format code
* Goto Declaration
* Find References
* Block comment and uncomment
* Goto history (goto next/previous error in open files, goto next/previous build)
* Auto indent for new lines
* TypeScript context menu
* Symbols in Project
* Symbols in File
* Rename refactoring
* Common Snippets
* `import` / `/// <reference` relative path resolution
* AST visualizer
* Dependency View

# Feature Details
## Auto Complete
Internally using AutoComplete+. Just start typing and hints will show up. Or you can explicitly trigger it using `ctrl+space` or `cmd+space`. Press `tab` to make a selection.

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/fastErrorCheckingAndAutoComplete2.gif)


## Type information on hover
Just hover

![you definitely get the point](https://raw.githubusercontent.com/TypeStrong/atom-typescript/master/docs/screens/hover.png)

## Compile on save
TypeScript files will be compiled on save. Different notifications are given if `emit` was successful or not. [Configuration driven by `tsconfig.json`](https://github.com/TypeStrong/atom-typescript/blob/master/docs/tsconfig.md)

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript/master/docs/screens/compile%20success.png)

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript/master/docs/screens/compile%20error.png)

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript/master/docs/screens/emit%20error.png)

## Project Support
Supported via `tsconfig.json` ([read more](https://github.com/TypeStrong/atom-typescript/blob/master/docs/tsconfig.md)) which is going to be the defacto Project file format for the next versions of TypeScript.

It also supports `filesGlob` which will expand `files` for you based on `minmatch|glob|regex` (similar to grunt).

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript/master/docs/screens/proj.png)

### Project Build Support
Shortcut: `F6`. If there are any errors they are shown as well.

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript/master/docs/screens/build%20success.png)

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript/master/docs/screens/build%20errors.png)

## Format Code
Shortcut : `ctrl+alt+l` or `cmd+alt+l`. Will format just the selection if you have something selected otherwise it will format the entire file.

## Go to Declaration
Shortcut : `F12`. Will open the *first* declaration of the said item for now. (Note: some people call it Go to Definition)

## Find References
Shortcut `shift+F12`. Also called *find usages*.

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/findReferences.png)

## Block Comment and Uncomment
`ctrl+/` or `cmd+/`. Does a block comment / uncomment of code.

## Go to Next / Go to Previous
`f8` and `shift+f8` respectively. This will go to next/previous *errors in open files* OR *build error* OR *references* based on which tab you have selected.

## Context menu
Quickly toggle the TypeScript panel OR select active TypeScript panel tab and other stuff using the context menu. `ctrl+;` or `cmd+;`.

## Symbols View
Integrates with atom's symbols view (`ctrl+r` or `cmd+r`) to provide you with a list of searchable symbols in the current file.

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/symbolsView.gif)

## Project Symbols View
Also called Go To Type in other IDEs. Integrates with atom's project level symbols (`ctrl+shift+r` or `cmd+shift+r`) to provide you with a list of searchable symbols in the *entire typescript project*.

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/projectSymbolView.png)

## Refactoring

### Rename
`f2` to initiate rename. `enter` to commit and `esc` to cancel.
![](https://raw.githubusercontent.com/TypeStrong/atom-typescript/master/docs/screens/renameRefactoring.png)

## tsconfig validation
![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/errorcases/invalidProjectOptions/invalidProjectOptions.gif)

## Snippets
### Relative Paths
Relative paths have traditionally been a pain, not anymore. Use `import` or `ref` and press `tab` to trigger snippet.

`ref`
![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/ref%20snippet.gif)

`import`
![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/import%20snippet.gif)

Note that within the path string you get autocomplete (`ctrl+space`/`cmd+space`) for all the files in the project by filename (works for both `ref` and `import`).

![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/pathChange.gif)

## AST Visualizer
Command : `Typescript: ast`. Useful when authoring new features.
![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/astVisualizer.gif)

## Dependency View
Command : `Typescript: Dependency View`. A dependency viewer for insight into the project. You can zoom, pan, drag points around and hover over nodes. ([more details](https://github.com/TypeStrong/atom-typescript/blob/master/docs/dependency-view.md))
![](https://raw.githubusercontent.com/TypeStrong/atom-typescript-examples/master/screens/dependencyView/teaser.png)


## Contributing

Look at [CONTRIBUTING.md](https://github.com/TypeStrong/atom-typescript/blob/master/CONTRIBUTING.md) for curiosity. We work hard to keep the code as approachable as possible and are highly keen on helping you help us.

## Changelog
Breaking changes [available online](https://github.com/TypeStrong/atom-typescript/blob/master/docs/CHANGELOG.md).
