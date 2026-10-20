# psvoiceovers-preview

Preview builds of [psvoiceovers.com](https://psvoiceovers.com) — **not the live site.**

**Preview address:** https://pseager.github.io/psvoiceovers-preview/

## How it works

- The GitHub Actions workflow in `.github/workflows/preview.yml` checks out a
  branch of `pseager/PSVoiceovers`, builds it, and publishes the result here.
- Which branch gets built is named in the `PREVIEW_REF` file (currently
  `main`, i.e. identical to the live site). Changing that file and pushing
  triggers a fresh preview build. It can also be run manually from the
  Actions tab ("Preview build" → "Run workflow") with a branch name typed in.
- Preview builds are stripped of the live site's custom domain and are
  tagged `noindex` with a blocking robots.txt, so Google ignores this copy
  and it never competes with psvoiceovers.com in search results.

Set up 2026-10-20 by Rex (Muse) at Paul Seager's request, so website changes
on `rex/…` branches can be viewed in a browser before anything is merged to
the live site.
