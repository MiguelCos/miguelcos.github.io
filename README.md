# Miguel Cosenza Contreras - Personal Website

Quarto website for `https://miguelcos.github.io`.

## Structure

- `_quarto.yml`: Quarto site configuration, navigation, metadata, and theme setup.
- `styles.scss`: custom site styling.
- `index.qmd`: home page.
- `about.qmd`: narrative professional profile.
- `cv.qmd`: public HTML CV.
- `publications.qmd`: selected publications and profile links.
- `projects.qmd`: selected GitHub projects.
- `projects/*/index.qmd`: individual project pages.
- `posts.qmd`: future notes/blog listing.
- `posts/_template/index.qmd`: draft post template.
- `contact.qmd`: contact and professional links.
- `.github/workflows/publish.yml`: GitHub Actions workflow for Quarto rendering and Pages deployment.

## Preview Locally

Install Quarto, then run:

```bash
quarto preview
```

To render the static site:

```bash
quarto render
```

The rendered site is written to `_site/`.

## Add A New Post

1. Copy `posts/_template/` to a new folder under `posts/`, for example `posts/my-note/`.
2. Update the YAML front matter: `title`, `description`, `date`, and `categories`.
3. Set `draft: false` when the post is ready to publish.
4. Run `quarto render` and review the listing on `posts.qmd`.

## Update The CV

Edit `cv.qmd`. Keep the public HTML version privacy-conscious by default.

TODO: If you later want a private or extended CV version, add it deliberately, review it manually, and link it only where intended. Phone number, private address, nationality, residency/work-permit status, and other sensitive personal details are intentionally omitted from public pages.

## Update Publications

Edit `publications.qmd` and `cv.qmd`. Prefer verified DOI, ORCID, PubMed, Crossref, publisher, or Google Scholar metadata. Do not fabricate titles, dates, coauthor order, journal names, issue details, or DOI links.

## Update Projects

Edit `projects.qmd` and the relevant page under `projects/<slug>/index.qmd`. Prefer public GitHub repository metadata and README text. Keep descriptions short and factual.

## Privacy Notes

- Public pages do not include phone number, nationality, residency/work-permit status, private address, or private CV details.
- Contact is by email and professional profile links only.
- LinkedIn wording should be manually verified because public access may vary by session and geography.

## GitHub Pages

Manual setup may be required once:

1. Open the repository settings on GitHub.
2. Go to **Pages**.
3. Under **Build and deployment**, choose **GitHub Actions** as the source.
4. Ensure Actions are enabled for the repository.

After that, pushes to `main` should run `.github/workflows/publish.yml` and deploy the rendered Quarto site.
