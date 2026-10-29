# Let your team edit the website

The site uses **Pages CMS**, a free online editor that works with this GitHub repository.
Team members get a simple form for their own profile (name, title, research topic, photo, links),
plus pages for news, publications, grants and gallery photos. They **do not need a GitHub account**.
Every save is recorded in the repository history, so any change can be undone.

## One-time setup (site owner, about 15 minutes)

1. **Put the site on GitHub** (if it isn't already).
   Create a repository (e.g. `asdl`), click *uploading an existing file*, and drag in **everything inside**
   the `asdl-site` folder, including the `_people` folder and the `.pages.yml` file. Commit.
2. **Turn on the website.** Repository → *Settings → Pages* → *Deploy from a branch* → `main` / `(root)` → *Save*.
   If the repository is not named `<account>.github.io`, set `baseurl: "/asdl"` (your repository name) in `_config.yml`.
   The site appears at `https://<account>.github.io/asdl/` within a few minutes.
3. **Connect Pages CMS.** Go to <https://app.pagescms.org>, sign in with GitHub, and install the
   Pages CMS GitHub App on this repository when asked.
4. **Invite your team.** Open the repository in Pages CMS → *Collaborators* → add each person's email.
   They receive an email invitation and can sign in without a GitHub account.

## What to send your team

- **Website:** `https://<account>.github.io/asdl/`
- **Editor:** <https://app.pagescms.org> (sign in with the email you were invited with)

## Instructions for team members

1. Open the invitation email and sign in to Pages CMS.
2. Click **Members** and open your name (or click **Add** to create your profile).
3. Fill in your title, research topic and links. Under **Photo**, upload a portrait; it is cropped to a circle automatically.
4. Click **Save**. The live website updates about a minute later.

Please edit only your own profile. News, publications, grants and gallery photos can be added from the menu on the left.

## Good to know

- Everyone invited can edit every page. Changes are tracked; the site owner can undo any change from the
  repository's *History*.
- Removing a person: in Pages CMS open their profile and delete it, or set **Group** to *Alumni*.
- If a save breaks the site, GitHub shows a red ✗ under the repository's *Actions* tab. Undo the last change there.
