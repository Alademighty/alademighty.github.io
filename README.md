# Academic site — Ambali Alade Odebowale

Four files, no build step, no dependencies. Open `index.html` in a browser to preview it locally.

```
index.html     the whole site
cv.pdf         linked by the "Download CV" button — replace with your latest
portrait.jpg   photo, extracted from your CV
README.md      this file
```

---

## Putting it online (GitHub Pages, free)

1. Sign in to GitHub and create a **new public repository** named exactly:

   ```
   Alademighty.github.io
   ```

   The name must match your username — that is what makes it a user site rather than a project site.

2. On the repository page choose **Add file → Upload files**, drag in `index.html`, `cv.pdf` and
   `portrait.jpg`, and commit.

3. Wait two or three minutes. Your site is live at:

   ```
   https://Alademighty.github.io
   ```

That URL is permanent and independent of any university account, which matters when you move
institutions. Put it in your CV header, your email signature and your Google Scholar profile.

### Optional: your own domain

A domain such as `odebowale.com` costs roughly AUD 20/year. Buy one, add a file named `CNAME`
to the repository containing just the domain name, then point the domain's DNS A records at
GitHub's addresses (listed in GitHub's custom-domain documentation). Nothing else changes.

---

## Keeping it current

Everything you will want to edit lives in one block near the bottom of `index.html`, marked:

```
/* ================= SITE DATA ================= */
```

Inside it are seven plain lists: `STATEMENT`, `THEMES`, `PUBLICATIONS`, `TEACHING`, `AWARDS`,
`REVIEWING`, `SERVICE`, `METHODS`, `TOOLS`. You do not need to touch the CSS or the layout.

**To add a publication**, copy one existing block and change the fields:

```js
{ year:2026, first:true, type:"article",
  title:"Your new paper title",
  authors:"Odebowale, A. A.; Co, A.; Author, B.",
  venue:"Journal Name", detail:"12(3), 456", doi:"10.xxxx/yyyyy" },
```

- `first: true` puts the red **1st** marker beside it and includes it in the "First author" filter
- `type: "review"` adds the Review tag; use `"article"` otherwise
- write your own name exactly as `Odebowale, A. A.` and it will be bolded automatically
- `doi:""` simply omits the DOI link

The year headings, the counter and the filters all rebuild themselves from the list. Sort order
is handled for you.

**To replace the CV**, overwrite `cv.pdf` with your new file, keeping the same filename.

---

## Before you publish — check these

- [ ] Rewrite the research statement in your own voice (it is currently my draft from your CV)
- [ ] Verify the two publication entries flagged in our conversation: the *Journal of Optics*
      metasurface filter (no DOI listed) and the *Nanophotonics* MoSe₂ paper (author order)
- [ ] Add any publications missing from the list — I built it from what is publicly indexed,
      and your Google Scholar profile may have more
- [ ] Add invited talks and conference presentations if you want a Talks section
- [ ] Check whether your PhD thesis is in the UNSW repository and link it
- [ ] Decide whether to publish your phone number — email alone is common and reduces spam

---

## A note on hosting paper PDFs

If you later add full-text PDFs, check the publisher's policy first. Most journals allow the
accepted manuscript but not the typeset version. SHERPA RoMEO lists the rules per journal.
Linking the DOI, as this site does, is always safe.
