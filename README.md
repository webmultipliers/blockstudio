# Blockstudio Boilerplate
A deeply opinionated way to get started with WordPress and Blockstudio.

The project will be renamed at in the future. It's far more than a boilerplate.

## Requirements
As long as you're committed to WordPress and building blocks with Blockstudio, you'll find useful tidbits in this project. 
- [WordPress](https://wordpress.org/)
- [Blockstudio](https://blockstudio.dev/)

## Getting Started

## Theme
Includes an opinionated theme intended to be extended by a required companion plugin. 

### Root Files

- `theme.json` — The theme configuration file.
- `style.css` — The theme stylesheet.
- `functions.php` — The theme functions file. 
- `index.php` — The theme index file.
- `screenshot.png` — The theme screenshot.

### Template Files

I like to start with a minimal set of template files. I'll add more as needed. The template files have a hierarchy, and WordPress will use the fallback system to determine which template file to use. 

Everything fallsback to `index.php` so I essentially ignore it since anticipate having full coverate with other templates. In most cases, the default `archive.php` will suffice for all archives excerpt for `author.php`, and `search.php`, and `single.php` will suffice for all posts excerpt for `page.php`.

- `404.php` — The 404 template file.
- `archive.php` — The archive template file.
- `author.php` — The author archive template file.
- `front-page.php` — The front page template file.
- `index.php` — The fallback template file.
- `page.php` — The single page template file.
- `search.php` — The search results template file.
- `single.php` — The single post template file.

### Parts
Not all of these parts are required, but I follow this pattern to keep things organized. 

#### Primary Site Components
- `site-header.php` — The site header template part. It's usually just named `header` but I like to be explicit.
- `site-footer.php` — The site footer template part.

#### Main Components
- `main-*.php` — The main content template part.
- `main-*-article.php` —  The main content article template part.
- `main-*-aside.php` — The main content aside template part.
- `main-*-query.php` — The main content query template part.
- `main-*-comments.php` — The main content comments template part.

#### Modal, Collapse, and Off-Canvas
- `site-menu-collapsed.php` — The site menu template part.
- `site-search-collapsed.php` — The site sidebar template part.

### Patterns
Patterns are a way to create reusable blocks of content that can be used in multiple places. I don't really use them in this project, but I include the directory for future use. 

### Assets
The theme assets directory is normally where all assets for the site are stored, but I'm only using it for fonts in this project. The remaining assets compilied and enqueued from in the plugin, including scripts, styles, and icons. Many of the styles are added via the `theme.json` file there is even less of a need for this directory for styles.

#### Fonts
The fonts directory is where you should store all the fonts for the project that you intend to use in the theme.json file.

The create-block-theme plugin will include all the necessary fonts for the project when sync down your changes. It will also create the required entries in the `fonts` array in the `theme.json` file.

## Plugin

### 📁 Assets

#### 📁 Icons
I don't have any icons, but I would probably put them here.

#### 📁 Images
I don't have any images, but I would probably put them here.

#### 📁 Styles

#### 📁 Scripts

### 📁 Blocks

- Each block namespace has a directory in the `blocks` directory.
- Each is initialized as its own Blockstudio instance.
- Each block has its own directory in the block namespace directory.
- Extension folders can be added to each namespace directory to extend a block or blocks by name.

### 📁 Experiences
I use the term "experiences" to describe how users can interact with the site, from logged-out visitors to logged-in admins. 

Each directory in the `experiences` tends to represent a broad, encapsulating set of features that may span 0 or more post types, taxonomies, custom field groups, and more. 

Most projects will bundle these directories in an `includes` folder. You do you, though.

Directories I typically include:
- Reading
- Writing
- Editing
- Branding

### 📁 Plugins
The `Blockstudio\Build` class is initated in the `example/plugins/` directory to serve as the home for all code snippets extending any plugins installed on the site. Often plugins will require you to add code your theme's `functions.php` file or through a code snippet plugin. 

For any plugins you need to extend, create a subdirectory in the `plugins` directory using the plugin's slug. 

- `init-*.php` — The `.php` code you want to run. An `init.php` file is required any time you want any code in the directory to be included on the site, including styles and scripts.
- `README.md` — A brief description of the plugin and what you're doing with it.


### 📁 Vendors
The `Blockstudio\Build` class is initated in the `example/vendors/` directory to serve as the home for all code snippets related to a specific vendor. Like the `plugins` directory, you can create a subdirectory in the `vendors` directory using the vendor's name. and the recommended files.

The vendor directory is one the last places I look to add code to the site. I prefer to extend plugins or keep code with the block or experience it's related to.

When the code has no ties to anything other than the external service, it goes in the vendor directory. Blocks and other experiences may use functions from the vendor directory. 

## My Stack
I may use these solutions as representative services to build blocks to demonstrate capabilities.

If you don't like what I picked, you're on your own to find an alternative. If I don't use it, I'm not going to recommend it. And, I'm not going to add anything to the project that I can't personally provide support for.

### Hosting
- [InstaWP](https://app.instawp.io/register?ref=39TUWaLAzX) — Staging & Production Sites

### Building
- [Meta Box](https://metabox.sjv.io/XYbB05) — Custom Fields (Minus Blocks, Forms, and Views)
- [Blockstudio](https://blockstudio.dev/) — Custom Blocks & Snippets
- [Bootstrap](https://getbootstrap.com/) — Frontend Framework (Partially)

### Coding
- [VS Code](https://code.visualstudio.com/) — Code Editor
- [Github Codespaces](https://github.com/features/codespaces) — Cloud Development Environment
- [Github Repos](https://github.com/) — Code Repository / Version Control

### Misc
- 1Password — Password Manager
- Cloudflare — DNS & CDN
- Coda — Shared Docs
- Fathom Analytics — Web Analytics
- Iubenda — Web Compliance
- Klaviyo — Marketing Automation
- Mercury — Banking
- Oh Dear — Web Monitoring
- Shopify — Commerce

## Sponsorship
If you find this project helpful, give me money. No, seriously, pull out the ole wallet and fork over some cheddar. Time is money, and if I save you some time, you some should give me some money.

## Disclaimer
- It's amateur hour over here. All code here is for inspiration only.
- You should enlist someone else to review any code you ship to production.
- Some links contain affiliate codes. I may earn a commission if you take up my recommendations.