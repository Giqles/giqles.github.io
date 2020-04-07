## Jekyll site

### Setup

#### Local

Install [Jekyll](https://jekyllrb.com/docs/installation/ubuntu/).

Clone this repo.

Then from root dir:

```bash
jekyll serve --drafts
```

Edit until happy.

#### Live

Just merge changes into master. Github will rebuild the site and then serve
it at [adamgil.es](https://adamgil.es)

### Updates

Set the original repo as another remote, then merge the `upstream/gh-pages` 
branch into a new branch of this repo.