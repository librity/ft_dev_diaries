# 42 Dev Diaries

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Docs](docs)
- [Resources](resources)

## About <a name = "about"></a>

Ever since I started studying at 42 S Paulo I write daily updates on my
progress and share them with my squad. They usually contain beginner-friendly
tips about the project I'm currently doing and about programming in general.

A friend suggested I should post these updates online for posterty's sake. I was
also studying GO and I came across the static site generator
[Hugo](https://gohugo.io/), so I thought I'd give it a shot.

## Getting Started <a name = "getting_started"></a>

### Prerequisites

All you need to get started is the latetes Hugo executable somewhere in your path.

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

## Resources <a name = "resources"></a>

Themes I liked:

- https://themes.gohugo.io/gohugo-theme-ananke/
- https://themes.gohugo.io/anatole/
- https://themes.gohugo.io/hugo-theme-diary/
- https://themes.gohugo.io/hugo-researcher/
