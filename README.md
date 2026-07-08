# The `argumentation` LaTeX Package

A LaTeX package for drawing argumentation frameworks (AFs) via TikZ.
It provides a simple, high-level syntax for creating argument nodes and attack/support edges while retaining full TikZ compatibility and customisation options.

## Features

- `af` environment for creating labelled, referenceable argumentation frameworks
- Commands for attacks (`\attack`, `\dualattack`, `\selfattack`), supports (`\support`), and annotated edges
- Collective (hyperedge) attacks and supports via `\setattack` and `\setsupport`
- Every attack/support edge gets a referenceable, optionally-named coordinate for further positioning
- Five argument styles, three attack styles, and three support styles
- Size presets (`small`, `tiny`) for two-column layouts
- Automatic or manual argument indexing
- Full beamer overlay support for presentations
- Additional macros for consistent AF naming and referencing (`macros` option)

## Installation

The package is available on [CTAN](https://ctan.org/pkg/argumentation) and is included in TeX Live and MiKTeX, so no manual installation is needed - simply load it in your preamble:

```latex
\usepackage{argumentation}
```

Alternatively, you can place `argumentation.sty` in the same directory as your `.tex` file to use it locally.

## Quick Start

```latex
\usepackage[namestyle=math]{argumentation}

\begin{af}
    \argument{a}
    \argument[right=of a1]{b}
    \argument[right=of a2]{c}

    \attack{a1}{a2}
    \dualattack{a2}{a3}
    \support{a1}{a3}
\end{af}
```

Arguments are automatically assigned identifiers `a1`, `a2`, `a3`, ... in order of creation.
Relative positioning (`right=of`, `below=of`, etc.) and absolute positioning (`at (x,y)`) are both supported.

## Documentation

See `argumentation-doc.pdf` for the full documentation including all commands, package options, and examples.

## Version

1.8 [2026/07/08]

## License

This package is subject to the LaTeX Project Public License 1.3c.

## Contact

Lars Bengel <lars.bengel@fernuni-hagen.de>

Please report issues at <https://github.com/aig-hagen/tikz_argumentation>
