## Installation

* [Fork](https://github.com/cubxxw/resume/fork) the repository;
* Go to settings and set master branch as Github Pages source;
* Your new site should be ready at `https://<username>.github.io/resume/`;
* Printable version of the site can be found at `https://<username>.github.io/resume/print`. Use a third party link https://pdflayer.com/, https://www.web2pdfconvert.com/ etc to get the printable PDF.

Change all the details from one place: `_data/data.yml`.

### To preview/edit locally with docker

```sh
docker-compose up
```

*docker-compose.yml* file is used to create a container that is reachable under <http://localhost:4000>.
Changes *_data/data.yml* will be visible after a while.

### Local machine

* Get the repo into your machine 

```bash
git clone https://github.com/cubxxw/resume.git
```

* Install required ruby gems

```bash
bundle install
```

* Serve the site locally

```bash
bundle exec jekyll serve
```

* Navigate to `http://localhost:4000`


## Configuring Your Site with `_config.yml` 🛠️

In the `_config.yml` file, you can configure the core aspects of your Jekyll site. This YAML file serves as the heart of your site's settings, defining everything from the basic setup to advanced features.

Here's a breakdown of the configuration options provided:

```yaml
# Update all the sections by editing the data.yml file inside _data folder.

# Site Settings
title: My Resume                   # The title of your site
url: 'https://resume.nsddd.top'    # URL of your site

# Change it according to your repository name
# disabling since we are using a custom domain
#baseurl: '/online-cv'             # Base URL for your project if hosted in a subpath

description: A beautiful Jekyll theme for creating resume  # Description for SEO
# Style will be applied only after restarting the build or serve. Just choose one of the options.
theme_skin: green                 # Choose a color theme: blue, turquoise, green, berry, orange, ceramic
chrome_mobile_color:              # HEX color for Chrome mobile search bar (e.g., #1976d2)

# Tracker
analytics: UA-83979019-1          # Google Analytics tracking ID

# Sass/SCSS
sass:
  sass_dir: _sass                 # Directory for Sass files
  style: compressed               # Output style for CSS: nested, expanded, compact, compressed

# Build settings
compress-site: yes                # Enable/disable site compression

encoding: "utf-8"                 # Character encoding standard
compress_html:                    # HTML compression settings
  clippings: all
  ignore:
    envs: development             # Ignore HTML compression in development mode

# Development Settings
port: 4000                        # Port number to run Jekyll locally
host: 0.0.0.0                     # Host to bind to when running locally
safe: false                       # Disable custom plugins, safe mode
```

### Detailed Explanation:
- **Title & URL**: Define the title and the base URL of your site. These are crucial for your site’s identity and SEO.
- **Base URL**: Useful when your site is hosted in a subdirectory and not at the root of the domain.
- **Description & Theme Skin**: Set a site description and choose a theme color that aligns with your personal or brand style.
- **Google Analytics**: Track site visits by entering your Google Analytics tracking ID.
- **Sass/SCSS Configuration**: Manage the directory for Sass files and set the CSS output style.
- **Compression**: Opt to compress your site content for faster load times.
- **Encoding**: Ensure your site uses "utf-8" encoding to support international characters.
- **HTML Compression**: Configure detailed HTML compression settings to optimize site performance.
- **Development Settings**: Set the port and host for local development. Decide whether to enable Jekyll’s safe mode, which affects plugins.

By configuring `_config.yml` appropriately, you can greatly influence the functionality and appearance of your Jekyll site, tailoring it to meet your specific needs.