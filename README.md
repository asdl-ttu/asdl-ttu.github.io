# Advanced Semiconductor Device Laboratory — website

Website of the Advanced Semiconductor Device Laboratory (ASDL), Department of Electrical & Computer Engineering, Texas Tech University.

It is a [Jekyll](https://jekyllrb.com/) site hosted free on **GitHub Pages**. GitHub rebuilds it automatically every time a file is changed, usually within a minute.

## Updating the site

Team members can edit the site through a simple online editor (Pages CMS); see **[TEAM-EDITING-SETUP.md](TEAM-EDITING-SETUP.md)**. Otherwise, most updates only touch the files in `_people/` and `_data/`. See **[HOW-TO-EDIT.md](HOW-TO-EDIT.md)**.

| To change…                    | Edit                         |
|-------------------------------|------------------------------|
| Lab members (one file each)   | `_people/`                   |
| Publications                  | `_data/publications.yml`     |
| News on the home page         | `_data/news.yml`             |
| Facility page cards           | `_data/facilities.yml`       |
| Grants page                   | `_data/grants.yml`           |
| Gallery photos                | `_data/gallery.yml` + `assets/img/gallery/` |
| Research text                 | `research.html`              |
| Home page text                | `index.html`                 |
| Menu, address, site title     | `_config.yml`                |
| Colors and fonts              | `assets/css/style.css`       |

## Folder layout

```
_config.yml          site settings and menu
_people/             one profile file per lab member
_data/               publications, news, grants, gallery, facilities, icons
.pages.yml           settings for the Pages CMS editor (team editing)
_layouts/default.html  header, menu, sidebar, footer shared by every page
_includes/           reusable pieces (temperature graphic)
assets/css, js, img  styles, scripts, images (member photos in assets/img/people/)
*.html               one file per page
```

## Preview on your own computer (optional)

Needs Ruby. Then:

```
bundle install
bundle exec jekyll serve
```

and open http://localhost:4000.
