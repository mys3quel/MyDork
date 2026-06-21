# MyDork

single html page that spits out recon links for bug bounty scopes. add your domains, optionally hook up a github org, and it generates a bunch of search links so you don't have to type dorks by hand.

## what you get

- **crt.sh / securitytrails** — subdomain discovery
- **github code search** — api keys, aws keys, .env files, terraform, ci/cd configs, k8s secrets
- **google dorks** — login panels, admin pages, dev/staging/uat/beta/sandbox/demo envs
- **info leaks** — exposed passwords, rsa keys, mongo uris, sentry dsns, stack traces, sql errors
- **shodan & censys** — hostname and ssl cert searches
- **wayback, builtwith, wappalyzer, grayhatwarfare, commoncrawl**

## how it works

open `index.html`, add a domain at the top, click the tab and all the links are generated. each one is clickable and opens the search in a new tab.

if you add a **github org** name, it also generates github code search dorks scoped to that org — handy for secret hunting.

data stays in your browser (localStorage). no server, no requests to anywhere, just a static html file.

wildcard checkbox covers `*.example.com` type scopes. you can add as many scopes as you want and switch between them with the tabs.

there's export/import in the sidebar if you want to back up your scope list or move it between machines.

## why

because typing `site:target.com inurl:admin` for the 50th time is boring.
