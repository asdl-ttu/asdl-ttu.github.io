# How to update the ASDL website

You can do everything in the browser on github.com. No software needed.

1. Open the repository on GitHub and click the file you want to change (for example `_data/members.yml`).
2. Click the **pencil icon** (Edit this file).
3. Make the change.
4. Click **Commit changes…**, write a short note (for example "Add new PhD student"), and click **Commit changes**.
5. Wait about a minute and refresh the website.

If the site doesn't update, open the **Actions** tab on GitHub. A red ✗ means there's a mistake in the file, usually indentation.

## Rules for the `.yml` files

- Indentation matters. Use **spaces, never tabs**, and line things up exactly like the existing entries.
- Each new item starts with `- ` (dash and space).
- If text contains a colon `:` followed by a space, put the whole text in double quotes: `text: "Poster at CINT: new results"`.
- Lines starting with `#` are comments and are ignored.

## Lab members

**Easiest:** use the Pages CMS editor (see `TEAM-EDITING-SETUP.md`). Click **Members**, pick a name, edit the form, upload a photo, and click **Save**.

**On GitHub directly:** each person has their own file in the `_people` folder, e.g. `_people/eftekhar-sadiq.md`. To add someone, copy an existing file, rename it, and change the details between the `---` lines:

```yaml
---
name: Full Name
initials: FN
group: phd          # pi, phd, ms, undergrad or alumni
order: 60           # smaller numbers appear first
title: Graduate Research Assistant, Electrical Engineering (PhD)
topic: One sentence about their research.
photo: /assets/img/people/full-name.jpg   # optional
---
```

Upload photos to `assets/img/people/`. Any portrait works; it is cropped to a circle automatically. Without a photo, the initials are shown.

**When someone graduates:** change `group: phd` to `group: alumni` and update `topic` with their degree and new position.

## Add a publication

In `_data/publications.yml`, add a new entry at the **top** of the `list:` section (newest first):

```yaml
  - title: Paper title
    authors: A. Author, E. Sadiq, T. Kim
    venue: IEEE Transactions on Electron Devices, vol. 73, pp. 1-6
    year: 2027
    type: Journal      # Journal, Conference, Poster, Thesis or Patent
    link: https://doi.org/10.xxxx/xxxxx
```

Names listed under `highlight:` at the top of the file appear in bold. Add new lab members there too, written the same way as in author lists.

## Add news

In `_data/news.yml`, add at the **top**:

```yaml
- date: 2026 · Nov
  text: "Paper accepted at IEEE IRPS 2027."
```

The home page shows the five newest items.

## Change the website address

The site is served from `https://<account>.github.io/<repository>/`.
- If the repository is named `<account>.github.io`, set `baseurl: ""` in `_config.yml`.
- Otherwise set `baseurl: "/<repository>"`, e.g. `baseurl: "/asdl"`.

## Add a grant

In `_data/grants.yml`, add at the **top**:

```yaml
- title: Project title
  agency: National Science Foundation (NSF)
  amount: $300,000
  year: 2027
  status: Active
  investigators: Taewoo Kim (PI)
  summary: One or two sentences about the project.
  link: https://link-to-announcement
```

## Add gallery photos

Upload the photo to `assets/img/gallery/`, then in `_data/gallery.yml` replace `[]` with entries like:

```yaml
- file: probe-station.jpg
  caption: Cryogenic probe station in Room 252
  date: 2026 · Oct
```

## Change the background picture

Replace `assets/img/hero-bg.jpg` with another landscape image (about 1920 × 1080) using the same file name.
