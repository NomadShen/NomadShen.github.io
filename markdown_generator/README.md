# Markdown Generator

This directory contains various ways of creating Markdown for your site. In general, filenames that end with `.ipynb` or `.py` are similar, but may contain different documentation or are intended to be run from with GitHub when deploying your site.

## Publication data

`publications.csv` and `publications.tsv` contain the same seven publications from
[Sirui Shen's Google Scholar profile](https://scholar.google.com/citations?user=lN6ZjaQAAAAJ&hl=en),
retrieved on September 17, 2026. Titles, author order, publication dates, venues,
volume/issue numbers, page ranges, and paper links follow the Scholar records.
Publication dates use Scholar's dates, which may precede the journal issue year.
Excerpts are short summaries of the descriptions, rather than complete abstracts.

To regenerate the website's publication pages from the CSV, run:

```sh
cd markdown_generator
python3 publications.py publications.csv
```

Keep the CSV and TSV in sync when editing. The `preprints` category is defined in
`_config.yml` so preprints appear separately from journal and conference papers.

## Python Scripts

The .py files are Python scripts that that can be run from the command line (ex., `python3 publications.py publications.csv`) with the objective of also ensuring that they have reduced requirements for packages, which may allow them to run when deploying your site from within GitHub.

## Jupyter Notebooks

These .ipynb files are Jupyter notebook files that convert a TSV containing structured data about talks (`talks.tsv`) or presentations (`presentations.tsv`) into individual markdown files that will be properly formatted for the academicpages template. The notebooks contain a lot of documentation about the process.
