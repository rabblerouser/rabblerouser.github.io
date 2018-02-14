# rabblerouser.team
_The public face of Rabble Rouser_

## The basics
This repository holds the HTML and Markdown source behind the content on https://rabblerouser.team. These files are used by [Jekyll](https://jekyllrb.com/), together with the [minimal-mistakes theme](https://github.com/mmistakes/minimal-mistakes) and configuration, to generate a static HTML site.

This site is continuously deployed to [Netlify](https://netlify.com), a free static site host.

## Content
Content is written in Markdown, with YAML "Front Matter" at the top of hte file providing metadata and configuration.

Content is divided into two categories - "pages" and "posts".

Pages are located in the `_pages` folder. Pages have a `permalink` set in their front matter to a relevant, short URL (e.g. `/contributors`), which is generally also used for the file name.

Posts are located in the `_posts` folder. Posts have a `date`, which is used by Jekyll to generate an appropriate blog-like URL, without a permalink. Posts use the format of `YYYY-DD-MM-my-post-name` for file names.

### Creating new content
#### Using Git
To create a new page or post, simply create a new Markdown file in the relevant folder, ensure it has correct Front Matter, and commit/push the file. This will trigger a site build, and within minutes your content will be live.

#### Using the 'Netlify CMS' frontend
rabblerouser.team uses the free "Netlify CMS" to enable a serverless frontend for content creation/editing.

Users must be created/invited from Netlify settings. They can then login at https://rabblerouser.team/admin, and create or edit content.

Changes are pushed to this repostiory by Netlify, which will trigger a site build and make the new content live.

## Theming and customisation
This site is based off the [minimal-mistakes theme](https://github.com/mmistakes/minimal-mistakes) Jekyll theme.

Theme files (layouts, includes, and styles) are included as a Ruby gem (in `Gemfile`. They files can be overridden locally, to customize or extend the base theme, by placing a file within this repository with the same name/path as the relevant file in the theme. It is usually advisable to copy the file from the minimal-mistakes theme, and then edit it.

Content and layout can be customized by editing _includes - partial snippets of HTML that are used for templating.

Styles can be customized by editing `assets/css/main.scss` in this repository, which is based off the theme SCSS. SASS variables used by the minimal-mistakes theme can be overridden by placing them above the main import directives. Custom CSS to extend or override existing styles should be placed after the directives.
