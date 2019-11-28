# hugo-notepadium ![](https://img.shields.io/badge/license-MIT-blue.svg)

a fast [gohugo](https://gohugo.io) theme, HTML + CSS, 100% JavaScript-free.

- built-in `syntanx highlight`
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
pygmentsUseClasses = true
pygmentsCodeFences = true
pygmentsCodeFencesGuessSyntax = true
```

custom your `404 page`:

add `/* /404.html 404` to your `content/_redirects`

if `_redirects` not exists, you can create a new one.
