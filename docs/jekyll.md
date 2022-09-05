---
layout: default
title: JEKYLL Notes
ieuser: liks@smidk
---
# {{page.title}}

## Tips

### Start a new website

```bash
gem install bundler jekyll
jekyll new new-website
cd new-website
bundle exec jekyll serve --port 4500 --livereload 
```

### Start a new website using bundler

```bash
mkdir bundle-init-new-site
cd bundle-init-new-site
bundle init
bundle config set --local path 'vendor/bundle'
bundle add jekyll
bundle exec jekyll new --force --skip-bundle .
bundle install
```

