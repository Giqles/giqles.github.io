## Jekyll site

### Setup

1. Install [Jekyll](https://jekyllrb.com/docs/installation/)

2. Clone this repo

3. Run:

    ```
    bundle install
    ```

    To install `jekyll-compose` to help write posts

### Making edits

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
