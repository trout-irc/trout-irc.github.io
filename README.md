# trout-irc.github.io

[gamja](https://codeberg.org/emersion/gamja), soju's web IRC client, built
unchanged at a pinned commit and published here so people who use
[trout](https://github.com/MaxRenaud/trout) can reach their own bouncer from
any browser:

    https://trout-irc.github.io/?server=wss://<bouncer>:8443/socket

trout's Tools > Connect a Phone shows the link. The bouncer needs a
certificate browsers trust (trout's Bouncers > Server > Certificate) and
`http-origin trout-irc.github.io` in its soju config, which trout's setup adds.
Nothing is stored here: gamja talks to the bouncer straight from your browser.

`goguma.html` is trout's own: Connect a Phone's QR code opens
`https://trout-irc.github.io/goguma#ircs://...`, since a phone's camera opens
any https link but does nothing with an ircs:// one unless Goguma is
installed. It shows a button that opens Goguma and where to get it.

gamja is AGPL-3.0 (see SOURCE.txt in the published site); the commit is in
`.github/workflows/pages.yml`.
