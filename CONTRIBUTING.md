# Contributing Guidelines

## Preview Documentation Locally

The `docs/` folder hosts the Jekyll site that powers celltune.org. To build or preview it on your machine:

### Prerequisites
- Ruby 3.x (2.7+ also works)
- Bundler (`gem install bundler` if you don’t already have it)

### Install dependencies
```bash
cd docs
bundle install
```

### Serve the site
```bash
bundle exec jekyll serve
```

The site will be available at `http://127.0.0.1:4000/` and will auto-reload when you save changes. Press `Ctrl+C` to stop the server. If Chrome shows stale videos while iterating, open DevTools → Network and enable “Disable cache” before refreshing.
