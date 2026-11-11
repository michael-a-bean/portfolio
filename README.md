# Michael Bean's Portfolio

Hugo source for [michaelbean.org](https://michaelbean.org).

## Updating professional information

- `config.toml`: the shared sidebar bio, search description, contact links, and copyright text. `{year}` in the copyright is replaced with the build year.
- `content/about/_index.md`: the public résumé page.
- `content/portfolio/`: project descriptions and case studies.

`content/portfolio/current-research.md` adds the November 2026 research overview. Its six summaries draw on the original commodity-project throughline and October 12 reassessment, the enterprise recovery audit and October 26 progress record (including the later Python migration), the Tanzania reconstruction and feasibility synthesis, the Nigeria tenure study's completed descriptive results and manuscript outline, the September artificial-life/adaptive-network audit and reference reconstruction, and the Sugarscape source, archived experiments, and revised study design in `/srv/work/research/llm-emergence`. Each summary also reflects the project's recorded literature assessment. The Sugarscape section's Jev comparison is a proposed direction, informed by TypeSafe's introduction, rather than an implemented integration. Preserve the distinctions between completed analyses, unresolved defects, proposed model specifications, and future research when updating this page.

The Current Research card uses the original SVG illustration at `static/img/portfolio/current-research.svg`. Its right panel reproduces the resource pattern in `/srv/work/research/llm-emergence/sugar-map.csv`; the agent positions are illustrative, not an experimental result. The left panel is a conceptual illustration of household prices, resources, and choices. The SVG is editable source and has no external image dependencies. Card image descriptions use the optional `imagealt` frontmatter field.

The November 2026 bio and résumé refresh uses the June 2026 revision of `/srv/work/documents/resume/resume.qmd`, also available at `/srv/work/projects/resume/resume.qmd`. Use the Quarto source when reconciling future changes; the HTML résumé in that directory predates the June 2026 revision. The Selected Projects descriptions also summarize documented limitations and the corresponding revisions or proposed research directions.

## Preview and build

With Hugo installed, run `hugo server` from this directory and open the local URL it prints. Run `hugo` to generate the site in the ignored `public/` directory.

## Publishing

The configured production pipeline builds and deploys changes pushed to `main`. See `buildspec.yml` for the Hugo build, S3 deployment, and CloudFront cache invalidation commands.
