## Jekyll site

### Setup

1. Install [Jekyll](https://jekyllrb.com/docs/installation/)

2. Clone this repo

3. Run:

    ```
    bundle install
    ```

    To install `jekyll-compose` to help write posts

### Making posts

Use the [jekyll-compose](https://github.com/jekyll/jekyll-compose) functions
to make and publish drafts.

If you have the `JEKYLL_EDITOR` variable set, new drafts will automatically 
open for editing.

While editing, run:

```bash
jekyll serve --drafts
```

So you can see the changes live.

To get the new version online, just merge changes into master. 
GitHub will rebuild the site and then serve it at [adamgil.es](https://adamgil.es).

### Making presentations

Presentations are a bit fiddlier. You make a post with just front matter in the
`_drafts` subdirectory, including the following properties:

```yaml
---
layout: presentation
title: Example Presentation
md_source: example-presentation.md
pdf_file: example-presentation.pdf #(optional)
---
```

Then you add the actual `remark.js` markdown content into the `assets` subdirectory
with whatever filename you used above.

This uses the `remark.js` `sourceUrl` argument to pass the location of the raw
markdown document, rather than trying to drop it in as the `text` field in the `html`
document that gets created.

When you're ready to publish the page on the site, you just "publish" the front matter 
above. Though, while editing the things you're saving into assets will be available online.

#### Making PDF versions of presentations

To make a pdf version of a presentation, the easiest thing is to use `decktape`.
To get that installed and working can be a bit of a pain. But once done, just
run `jekyll serve --drafts`, copy the link to your presentation `.html` file, and run
something like:

```
decktape http://127.0.0.1:4000/2020/05/28/example-presentation.html assets/example-presentation.pdf
```

Then commit and push everything, and it should work nicely.
