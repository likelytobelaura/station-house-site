# station-house.net

The Stationhouse website. Static HTML, no build step, deployed with GitHub Pages.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole site. One page: nav, hero, projects, app band, footer. |
| `style.css` | All styling. Colours and fonts are CSS variables in the `:root` block at the top. |
| `404.html` | Not-found page. |
| `assets/station-house-hero.jpg` | Hero painting. |
| `favicon.svg` | Favicon. |
| `CNAME` | Tells GitHub Pages the custom domain is `station-house.net`. Do not delete. |
| `robots.txt` | Lets search engines index everything. |
| `.nojekyll` | Stops GitHub running the files through Jekyll. |

## Editing

Open `index.html` and change the text. There is no framework and nothing to compile.
Push to `main` and the live site updates within a minute or two.

To change the look, edit the variables at the top of `style.css`:

```css
--cream:  #F4EEE0;  /* page background */
--ink:    #24262A;  /* headings */
--accent: #8A4B33;  /* clay: rules, links, primary button */
--brown:  #5E2F22;  /* the dark band near the bottom */
```

Type is Fraunces (display) over Hanken Grotesk (body), both loaded from Google Fonts
in the `<head>` of each page.

## Local preview

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deployment

GitHub Pages serves `main` from the repository root.

DNS for the apex domain:

```
A     @     185.199.108.153
A     @     185.199.109.153
A     @     185.199.110.153
A     @     185.199.111.153
CNAME www   <username>.github.io
```

The domain is registered through Squarespace, so those records go in the Squarespace
DNS panel. Disconnect the domain from the Squarespace site first or its own records
take precedence.

## Design

Direction is "Horizon", picked from four options. Cream ground, Fraunces over Hanken
Grotesk, clay accent, steam locomotive painting behind the headline. The hero gradient
is deliberately stronger than the original mockup because cream text over the pale sky
was failing contrast at phone width.
