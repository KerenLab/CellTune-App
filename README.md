# CellTune-App
CellTune is a desktop application for accurate cell classification in spatial proteomics data.

From this page, you can download CellTune [releases](https://github.com/KerenLab/CellTune-App/releases).

You can also submit bugs, issues, and feature requests [here](https://github.com/KerenLab/CellTune-App/issues).

For more info and documentation please visit [celltune.org](https://celltune.org)

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
