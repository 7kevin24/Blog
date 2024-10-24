﻿# Current Configuration
This is a reminder to record the current configuration of the mkdocs.
### Set up envrioment

```
pip install mkdocs
```
```
pip install mkdocs-material
```
```
pip install mkdocs-video
```
```
pip install mkdocs-jupyter
```
```
pip install leafmap
```
```
pip install mkdocs-git-revision-date-localized-plugin
```

### Mkdocs.yml
```yaml
site_name: Kevin's Blog
markdown_extensions:
  - pymdownx.superfences
  - pymdownx.highlight:
      anchor_linenums: true
      line_spans: __span
      pygments_lang_class: true
  - pymdownx.inlinehilite
  - pymdownx.emoji:
      emoji_index: !!python/name:material.extensions.emoji.twemoji
      emoji_generator: !!python/name:material.extensions.emoji.to_svg
  - attr_list
  - md_in_html
# below is for the admonition extension
  - admonition
  - pymdownx.details
  - pymdownx.superfences
  - pymdownx.arithmatex:
      generic: true
plugins:
  - glightbox
  - search
  - git-revision-date-localized:
      enable_creation_date: true  # Show when the file was created
      locale: 'en'
      fallback_to_build_date: true  # Use build date if no commit info is found
  - mkdocs-video:
      # mark: "video"
      video_autoplay: false
      video_loop: false
      video_muted: true
  - mkdocs-jupyter  
theme:
  name: 'material'
  font:
    text: 'Georgia'
    # text: 'Bookman-Old-Style'
    code: 'Roboto Mono'
  icon:
    logo: simple/keras
    menu: fontawesome/solid/left-long
    admonition:
      note: material/notebook
      abstract: material/format-list-bulleted
      info: octicons/info-16
      tip: material/lightbulb-on
      success: octicons/check-16
      question: octicons/question-16
      warning: octicons/alert-16
      failure: octicons/x-circle-16
      danger: octicons/zap-16
      bug: octicons/bug-16
      example: material/pencil-outline
      quote: fontawesome/solid/quote-right
  features: 
    - content.code.copy
    - content.code.annotate
    - content.code.select
  palette: 
    # Palette toggle for light mode
    - scheme: default
      primary: orange
      toggle:
        icon: material/brightness-7 
        name: Switch to dark mode

    # Palette toggle for dark mode
    - scheme: slate
      primary: orange
      toggle: 
        icon: material/brightness-4
        name: Switch to light mode
extra_javascript:
  - https://unpkg.com/leaflet@1.7.1/dist/leaflet.js
  - javascripts/mathjax.js
  # - https://polyfill.io/v3/polyfill.min.js?features=es6
  - javascripts/tex-mml-chtml.js
  - https://cdn.jsdelivr.net/npm/brython@3.9.5/brython.min.js


extra_css:
  - https://unpkg.com/leaflet@1.7.1/dist/leaflet.css
  - stylesheets/extra.css
  - https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.7/katex.min.css
  - https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css
```