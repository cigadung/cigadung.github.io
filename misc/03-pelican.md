Title: Pelican-Install & Config
Category: Coding
Date: 2016-07-09
SubTitle: Configuration
Tags: Python, Pelican


```bash
# Check pip
$ pip install --upgrade pip
$ pip -V
pip 8.1.1 from /usr/lib/python2.7/dist-packages (python 2.7)

# Install virtualenv
$ sudo pip install virtualenv
```

```bash
# Install virtualenv
$ virtualenv cigadung-pelican
New python executable in /home/em/statik/cigadung-pelican/bin/python
...
# Activate
$ cd cigadung-pelican/
$ source bin/activate
(cigadung-pelican) em@g473:~/statik/cigadung-pelican$ 

# Install pelican + others
$ pip install pelican
$ pip install Markdown
$ pip install typogrify
$ pip install beautifulsoup4

# Clone pelican-plugins
$ git clone https://github.com/getpelican/pelican-plugins.git

# Clone pelican-themes (semua theme, hanya utk eksperimen)
$ git clone --recursive https://github.com/getpelican/pelican-themes ./pelican-themes

# Generator, QA
$ pelican-quickstart
```

```bash
# Makefile bawaan pelican-quickstart
$ make devserver
$ make stopserver
$ make clean
```

```python
#!/usr/bin/env python
# -*- coding: utf-8 -*- #
from __future__ import unicode_literals
import os

AUTHOR = 'CFC Admin'
SITENAME = 'Cigadung FC'
SITEURL = 'http://localhost:8000'

PATH = 'content'
TIMEZONE = 'Asia/Jakarta'
DEFAULT_LANG = 'en'

# Feed generation is usually not desired when developing
FEED_ALL_ATOM = None
CATEGORY_FEED_ATOM = None
TRANSLATION_FEED_ATOM = None
AUTHOR_FEED_ATOM = None
AUTHOR_FEED_RSS = None

DISPLAY_CATEGORIES_ON_MENU = True
DISPLAY_CATEGORIES_ON_SIDEBAR = False
DISPLAY_PAGES_ON_MENU = True
DISPLAY_TAGS_ON_SIDEBAR = True
TAG_CLOUD_MAX_ITEMS = 10

DISQUS_SITENAME = 'cigadung'

# Blogroll
LINKS = None

THEME = "themes/pelican-bootstrap3"
BOOTSTRAP_THEME = 'paper'
CUSTOM_CSS = 'static/custom.css'

STATIC_PATHS = ['images', 'extra/custom.css']

EXTRA_PATH_METADATA = {
    'extra/custom.css': {'path': 'static/custom.css'}
}

DEFAULT_PAGINATION = 5
BANNER = 'images/cfc2.jpg'
BANNER_SUBTITLE = 'Code, DevOps, Coffee & Fun'


PLUGIN_PATHS = [os.path.join(os.environ.get('HOME'),
                'statik/cigadung-pelican/pelican-plugins')]

PLUGINS = ['tipue_search',
           'tag_cloud']

DIRECT_TEMPLATES = ('index', 'categories', 'authors', 'archives', 'search')

ARCHIVES_SAVE_AS = 'archives.html'

PYGMENTS_STYLE = 'default'

DISPLAY_RECENT_POSTS_ON_SIDEBAR = True

# Social widget
SOCIAL = (('github', 'http://github.com/cigadung'),)
```


