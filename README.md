# 42 Dev Diaries

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Docs](docs)
- [Resources](resources)

## About <a name = "about"></a>

About a month ago I began my journey at [42 S Paulo](https://www.42sp.org.br/), and
I started writing daily updates on my progress and sharing them with my squad.
They're full of beginner-friendly tips on my current project and about coding in general.

A friend told me I should post these updates online for posterty's sake. I was
studying GO the other night and I came across a new static site generator
called [Hugo](https://gohugo.io/), so I thought I'd give it a shot.

## Getting Started <a name = "getting_started"></a>

### Prerequisites

All you need to get started is the latest version of Hugo in your `$PATH`.

- https://gohugo.io/getting-started/installing/

```bash
# macOS
$ brew install hugo
# Ubuntu/Debian
$ sudo apt-get install hugo
# Windows
$ choco install hugo-extended -confirm
```

### Installing

Clone the repo and start a development server:

```bash
$ git clone https://github.com/librity/ft_dev_diaries.git
$ cd ft_dev_diaries
$ hugo server -D
```

Open http://localhost:1313/ on your web browser.

## Usage <a name = "usage"></a>

Create new posts with:

```bash
$ hugo new posts/POST_NAME.md
```

## Docs <a name = "docs"></a>

- https://gohugo.io/getting-started/quick-start/
- https://themes.gohugo.io/tags/blog/
- https://github.com/theNewDynamic/gohugo-theme-ananke
- https://formspree.io/library

## Resources <a name = "resources"></a>

Themes I liked:

- https://themes.gohugo.io/gohugo-theme-ananke/
- https://themes.gohugo.io/anatole/
- https://themes.gohugo.io/hugo-theme-diary/
- https://themes.gohugo.io/hugo-researcher/
- https://github.com/formspree/blogophonic-hugo
