---
layout: "document"
title: "Formatting"
---

# Formatting

## Creating a table of contents

Adding a `toc` value in the page's [front matter](https://jekyllrb.com/docs/front-matter/) will create a new side panel with entries (not automatic yet).

```yaml
---
title: "My great page"
layout: "document"
toc:
- name: "Simple heading"
- name: "Very complicated heading with 20 numbers"
  link: "#complicated-heading"
---
```