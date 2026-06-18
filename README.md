# lid-slides

Official Beamer presentation template for the **Laboratório de Inteligência de Dados (LID)** at UFPA.

This repository provides a LaTeX/Beamer template for academic and professional presentations produced by LID members. It defines a consistent visual identity, including colors, title page, frame headers, footer, section dividers, logos, and reusable slide commands.

## Preview and copy on Overleaf

An Overleaf version of this template is available for viewing and copying:

[Open the LID Slides template on Overleaf](https://www.overleaf.com/read/pvdnjssnxykj#1543f9)

Use this link if you want to quickly inspect the template, duplicate it into your own Overleaf account, or start a presentation without cloning the repository locally.

## Repository structure

```text
lid-slides/
├── assets/              # Logos and visual assets
├── sections/            # Example section files
├── LICENSE              # MIT license
├── README.md            # Project documentation
├── lid.sty              # Custom LID Beamer style
└── main.tex             # Main presentation file
```

## Main features

* LID/UFPA visual identity for Beamer presentations.
* Custom title page with institutional logos.
* Styled frame titles and section divider slides.
* Footer with author names, short title, date, slide number, and progress bar.
* Support for up to five authors using custom author commands.
* Reusable commands for:

  * final thank-you slide;
  * two-column layouts;
  * highlighted content boxes;
  * full-screen image slides.

## Basic usage

Clone this repository:

```bash
git clone https://github.com/lid-ufpa/lid-slides.git
cd lid-slides
```

Edit `main.tex` with your presentation information:

```latex
\title[Título curto]{Título da apresentação}

\authorone[Doe]{John Doe}
\authortwo[Doe]{Jane Doe}

\date{\today}
```

Add your content inside the files in the `sections/` directory, or create new section files and include them in `main.tex`:

```latex
\section{Introdução}
\input{sections/introducao}
```

Compile `main.tex` using your preferred LaTeX environment, such as Overleaf, TeX Live, or MiKTeX.

## Custom commands

### Thank-you slide

```latex
\lidthanks[
  Obrigado!
][
  \faEnvelope\ john.doe@lid.ufpa.br \\
  \faLinkedin\ linkedin.com/in/johndoe \\
  \faGithub\ github.com/johndoe
]
```

### Two-column layout

```latex
\begin{lidtwocol}
Left column content

\lidnextcol

Right column content
\end{lidtwocol}
```

### Highlight box

```latex
\lidhighlight{Important message or key result.}
```

### Full-screen image slide

```latex
\lidfullimage{assets/example-image.pdf}{Image caption}
```

You can also control the image scale:

```latex
\lidfullimage[0.85]{assets/example-image.pdf}{Image caption}
```

## Requirements

The template is based on LaTeX Beamer and uses packages such as:

* `beamer`
* `graphicx`
* `tikz`
* `montserrat`
* `fontawesome5`
* `adjustbox`
* `xargs`
* `etoolbox`

When using Overleaf, most required packages should already be available. For local compilation, make sure your LaTeX distribution is up to date.

## License

This project is distributed under the MIT License. See [`LICENSE`](LICENSE) for details.

## About LID

The **Laboratório de Inteligência de Dados (LID)** is a research laboratory at UFPA focused on data intelligence, machine learning, artificial intelligence, optimization, and applied computational research.
