# jeanbilheux.github.io

Personal website for Jean Bilheux — published at <https://jeanbilheux.github.io/>.

Plain static HTML and CSS. No build step: edit, commit, push to `main`, and
GitHub Pages redeploys within a minute.

```
index.html   the whole page
css/home.css all styling
cv/          the CV the header's "CV" button downloads
fonts/       self-hosted Source Sans 3 (variable, woff2)
images/      header portrait + talk thumbnails
.nojekyll    serve every file verbatim, including dirs starting with "_"
```

## Updating the CV

Overwrite `cv/JeanBilheuxCV.pdf` and push. Keep the filename — it is what the
header and footer link to, and the `download` attribute means that name is also
what visitors get on disk.

## Adding a presentation

Decks live in a separate repository,
[`ornlneutronimaging/jean_presentations`](https://github.com/ornlneutronimaging/jean_presentations),
and are published at `https://ornlneutronimaging.github.io/jean_presentations/...`.

To list a new one here, copy the `<article class="talk-card">` block in
`index.html`, then update the conference pill, location/date, title, blurb, and
the "Open the slides" URL. Cards stack in document order.

Every off-site link carries `target="_blank" rel="noopener"` so it opens in a new
tab and leaves this page where the visitor left it — keep that on new links too.

For the hero image, grab the deck's first preview slide
(`_preview/s-01.jpg` in the presentations repo), drop it in `images/`, and point
`.hero-visual` at it.
