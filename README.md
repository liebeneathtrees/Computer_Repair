# Laptop repair & maintenance

Step-by-step repair, upgrade and maintenance guides for:

- **HP Envy 17 (17-cr0xxx)**: screen, hinges, battery, thermal paste, fans and bottom case
- **Toshiba Satellite U845W**: SSD and memory upgrade, battery, sticky coating removal, hinge care, Linux Mint
- **External drives**: turning old laptop drives into USB drives

Everything is in a single file, `index.html`, plus an optional `images/` folder for photos. It needs no build step or server and works offline.

## Photos

Put photos in `images/` using the file names listed in `images/README.md`. Each photo appears under its step automatically, and steps without a photo show nothing. Crop out serial numbers and personal details before uploading.

## Printing

- **Print checklist** (next to each progress bar) prints a compact checklist of the whole project.
- **Print** on each phase heading prints just that phase.

Ticked steps print as ☑ and open steps as ☐, so you can work from paper at the bench.

## Publish on GitHub Pages

1. Create a repository and add `index.html` (and this README) to the root.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/ (root)`, and save.
4. After a minute or two, the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Progress checkboxes

- Ticked steps are saved in the browser you tick them in (localStorage), not in the repository.
- To carry progress to another device or browser, use **Overview → Export progress**, then **Import progress** on the other device.
- Each step is identified by its text. Adding, removing or reordering steps won't move existing ticks onto the wrong step. Editing a step's wording clears the tick on that one step.

## Adding a project

1. In `index.html`, copy an existing `<section class="project" id="..." data-project="..." data-label="...">` block. Give it a new, unique `id` and `data-project` (lowercase, no spaces). Put the IDs and in-page links inside it under the same prefix, for example `id="newproj-parts"` and `href="#newproj-parts"`.
2. Add a tab link to the `<nav class="sitenav">` list, for example `<a href="#newproj">New project</a>`.
3. Add a one-line summary for the overview card to the `SUMMARY` object in the script at the bottom.
4. Steps go in `<ul class="steps">` lists inside `<section class="phase">` blocks. Each project needs one progress bar (copy the `<div class="progress">` block).

## Overview tables

The **Overview** tab has four tables you edit directly in `index.html`:

- **Devices at a glance:** specs, key part numbers and current status for each device.
- **Parts tracker:** every part across the projects. Change a part's status tag as it moves along, for example from `<span class="tag t-maybe">Ordered</span>` to `<span class="tag t-have">Received</span>`. Use `t-no` for parts still to buy.
- **Maintenance schedule:** recurring tasks, such as backups, battery checks and fan cleaning.
- **Maintenance log:** a dated record of work done. Copy a row to add an entry, newest first.

Each phase heading shows a count of its ticked steps. The **Hide done** switch beside each progress bar hides finished steps and phases.

## Privacy

This page is public once published. Never add serial numbers, BitLocker recovery keys, passwords or personal addresses.
