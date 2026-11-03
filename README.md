# Vehicle Info

A static reference site for eight India-market cars and motorcycles, built as a student portfolio project. Plain HTML and CSS, no JavaScript, no analytics and no third-party embeds.

Live site: **https://arijitmondal-fs-dev.github.io/vehicle-info/**

## The line-up

| Cars | Motorcycles |
| --- | --- |
| Maruti Suzuki Swift | Hero Splendor Plus |
| Honda City | Royal Enfield Classic 350 |
| Hyundai Creta | KTM 390 Duke |
| Mahindra XUV400 | Royal Enfield Himalayan 450 |

There are two head-to-head comparisons, an about page and a full credits page. Each vehicle file records published specifications, prices, safety ratings and warranty terms, with its own source list. Where a manufacturer does not publish a figure, the page says so instead of substituting a secondary number. Where two official documents disagree, both values are shown.

## Data and images

Specifications and prices were checked against manufacturer websites, brochures, price lists and owner's manuals on 3 November 2026. Prices are ex-showroom Delhi and exclude insurance, registration, road tax and offers. This is a snapshot, not a live database.

Photographs are Creative Commons or public-domain images from Wikimedia Commons, cropped and resized for the web. Each is credited on the page where it appears and on the [credits page](site/credits.html). Diagrams are original SVG side elevations drawn for this project. Overpass and Overpass Mono are self-hosted under the SIL Open Font License.

## Local preview

The publishable site is the `site/` directory. Open `site/index.html` directly, or serve the folder:

```sh
python -m http.server 8000 --directory site
```

Then visit `http://localhost:8000`.

## Deployment

GitHub Actions publishes `site/` to GitHub Pages on every push to `main`. The workflow is [`.github/workflows/pages.yml`](.github/workflows/pages.yml). There is no build step in CI: the HTML, CSS, fonts and images in `site/` are the deployable artifact.

Before the first deployment, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions** in the repository. No branch or folder needs to be selected.

## Structure

```text
site/
  index.html
  cars/  bikes/  vehicles/  compare/
  about.html  credits.html  404.html
  assets/css/  assets/fonts/  assets/img/
  robots.txt  sitemap.xml  .nojekyll
.github/workflows/pages.yml
```

## Licence

Code and original diagrams are released under the MIT licence in [LICENSE](LICENSE). Photographs remain under the licences stated in the credits; CC BY-SA images stay under the same terms. Fonts remain under the SIL Open Font License.

Vehicle names and marks belong to their respective manufacturers. This is an independent student project with no affiliation or endorsement.
