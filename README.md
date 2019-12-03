# hugo-notepadium ![](https://img.shields.io/badge/license-MIT-blue.svg) [![Netlify Status](https://api.netlify.com/api/v1/badges/2f389751-e070-437b-9dbd-3773bd57322e/deploy-status)](https://lvv.me)

a fast [gohugo](https://gohugo.io) theme, HTML + CSS, 100% JavaScript-free.

- built-in `syntanx highlight`
- `MathJax` support
- custom `404 page`

![](https://lvv.me/posts/2019-11-24_a_simple_hugo_theme/01.png)

the core CSS is `core.css`, transferred size < 3KB.

preview this theme: https://lvv.me

## Quick Start

```shell
git submodule add https://github.com/cntrump/hugo-notepadium.git themes/hugo-notepadium
```

demo `config.toml`:

```toml
baseURL = "/"
languageCode = "zh-cn"
title = "Lvv's notepad"
theme = "hugo-notepadium"
copyright = "Copyright &copy;2019 lvv. All rights reserved."
hasCJKLanguage = true
enableRobotsTXT = true
paginate = 5

# Hugo v0.60+ new configuration
[markup.highlight]
  codeFences = true
  noClasses = false

# old Hugo version
pygmentsUseClasses = true
pygmentsCodeFences = true
pygmentsCodeFencesGuessSyntax = true
```

If you like syntax highlight with JS, both `hljs` and `prismjs` are builtin:

```toml

# Disable Hugo bultin syntax highlight

# Hugo v0.60+ new configuration
[markup.highlight]
  codeFences = false
  noClasses = false

# old Hugo version
# pygmentsUseClasses = true
# pygmentsCodeFences = true
# pygmentsCodeFencesGuessSyntax = true

# enable JS highlight
[params.syntax]
  use = "hljs"  # 1. prismjs 2. hljs 3. none
```

enable `MathJax` support

```toml
[params.MathJax]
    enable = true
```

Usage

```
When $a \ne 0$, there are two solutions to \(ax^2 + bx + c = 0\) and they are
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
```

You can custom nav items:

```toml
[params.nav]
  showCategories = true       # /categories/
  showTags = true             # /tags/
  customs = ["album","about"]  # /album/; /about/
```