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

## Embedding threads

You can insert balloons referencing threads by using the following code:

```html
{% raw %}{% include thread.html thread=ThreadId %}{% endraw %}
```

Please note that for this to work you have to ensure that entries in files `_data/users.yaml` and `_data/threads.yaml` are existent, like from the following examples:

```yaml
1: R.O.B. # UserId: Display name
```

```yaml
2: # Id of the thread
  title: "Rules" # Title of the thread
  author: 1 # Id of the thread author
```

If everything has been followed you'll see a balloon like this:

{% include thread.html thread=2 %}

**Caution:** Embedding balloons in Markdown lists doesn't work as it ends a list and starts it after the balloon, so it's only advised to use it in paragraphs.