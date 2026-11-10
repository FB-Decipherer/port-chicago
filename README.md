# GYR-O Pages

A website format built on three columns: **plain answers**, **previewed sources**,
and **full technical detail** — so three different visitors each get what they
came for on one page, without wading through the other two.

Live: **https://__DOMAIN__**

## Why

Most sites serve one reader and make the others work for it. A customer scrolling
past technical specifications stops reading; a specialist scrolling past an
explanation of basic terms also stops reading.

The middle column is the part nobody else does. Every external source gets a card
that says what it is, who made it, what you would find there, and what it is doing
on this page — **with the link last**, deliberately. When the link came first,
readers clicked it and never read the preview, which defeated the whole column.

## What it costs, and what it can't do

The domain, and nothing else. Hosting is GitHub Pages; the certificate is issued
automatically. Nobody has promised free hosting forever, and the protection against
that is structural rather than contractual: this is a handful of plain files that
could be moved to any other static host in an afternoon, unchanged.

It is hard to compromise because there is nothing to attack — no database, no login,
no forms, no server code, no plugins, no cookies. Nothing in it has a version number,
so nothing in it can become an old version.

## The files

| file | what it is |
|---|---|
| `index.html` | the public page — columns A, B, C |
| `setup.html` | page D — the setup sheet. Unlinked, noindex. Not an admin panel: a form that produces text you paste into a file. |
| `domain.html` | page E — standing up a domain, step by step. Unlinked, noindex. |
| `links.json` | link-health status, written by a scheduled check. If absent, the page says nothing about link health — no file, no claim. |
| `phone-view.js` | Phone view, for whoever builds the page: shows it in a phone-sized frame. Hidden unless the address carries `?dev`, or the page's own button carries `data-public` (as on gyro-sites.online). |
| `top-button.js` | the round up-arrow button that returns to the top, once the reader has scrolled about a screen down |
| `back-link.js` | the Back button on a source card, returning to the numeral that opened it |
| `search.js` | the search box in the navigation bar: builds its index from the page itself at load, so it never goes stale, and finds words inside folded answers that a browser’s find bar can miss |
| `masthead.svg` | the picture at the head of the page — a placeholder, replaced by each new site |
| `social.png` `apple-touch-icon.png` | the share card and the home-screen icon |
| `favicon.svg` `robots.txt` `sitemap.xml` `404.html` | the usual furniture |

The three scripts are the same files on every site that carries them. Change one in
`Three Columns Tools/template/` first, then copy it out, so no copy drifts from the others.

## Publishing

Edit `index.html`, open GitHub Desktop, type one line saying what changed, click
**Commit**, then **Push**. Live in about a minute. Two words to learn; branches and
pull requests can be ignored indefinitely.

`domain.html` walks through the domain setup once, with every value filled in.

## Using it yourself

MIT licensed — copy it, change it, sell work built with it, no permission needed.
If you do something interesting with it, saying so is welcome and not required.

Walter Wilkinson · Worland · Washakie County · Wyoming
