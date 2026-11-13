# Parts Relay public

The files every Parts Relay web app serves from its root as they are, kept in one place. [PartsRelay/ui](https://github.com/PartsRelay/ui) and [PartsRelay/site](https://github.com/PartsRelay/site) mount this repository as the git submodule `public`, and `public/static` is their public directory.

## Files

- `static/favicon.png`: the icon of the browser tab, 512 by 512.
- `static/og.png`: the image of a shared link, 1200 by 630. Each app points `og:image` and `twitter:image` at it.
- `static/robots.txt`: every crawler may read every page. An app keeps a page out of the search engines with its own `noindex` tag.

## Rules

- Every file of `static` is published at the root of every app. Keep out what only one app needs, and anything private.
- Nothing outside `static` is published, so this `README.md` and the git files of the submodule never reach a built site.
- To add or change a file, commit it here, then run `git submodule update --remote public` in each app and commit the new pointer.
