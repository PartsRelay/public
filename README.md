# Parts Relay public

The files every Parts Relay web app serves from its root as they are, kept in one place. [PartsRelay/ui](https://github.com/PartsRelay/ui) and [PartsRelay/site](https://github.com/PartsRelay/site) mount this repository as the git submodule `public`, their public directory.

## Files

- `favicon.png`: the icon of the browser tab, 512 by 512.
- `og.png`: the image of a shared link, 1200 by 630. Each app points `og:image` and `twitter:image` at it.
- `robots.txt`: every crawler may read every page. An app keeps a page out of the search engines with its own `noindex` tag.

## Rules

- Every file here is published at the root of every app, this `README.md` included. Keep out what only one app needs, and anything private.
- To add or change a file, commit it here, then run `git submodule update --remote public` in each app and commit the new pointer.
