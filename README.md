# Hi, I am @ampsauce – The AMP Project Sauce Labs bot.

I build pull requests against [AMP HTML](https://github.com/ampproject/amphtml) on Sauce Labs. See also the [Sauce Labs section](https://github.com/ampproject/amphtml/blob/master/DEVELOPING.md#saucelabs) in AMP's developers doc.

My builds are here: https://travis-ci.org/amphtml-savage/amphtml/builds

I am an instance of [Savage](https://github.com/twbs/savage).

## Configuration

I live on a Google Compute Engine instance owned by @cramforce on `savage.nonblocking.io`.

- my passwords are in Google's password store owned by malteubl@.
- started by `/home/malte_ubl/start_savage.sh`
- config in `savage/src/main/resources/application.conf`
- after change `cd savage`, `sbt assembly`, `cp target/scala-2.11/savage-assembly-1.0.jar ../`, restart

```
    default-port = 8080
    squelch-invalid-http-logging = true
    set-commit-status = true
    travis-timeout = 2 hours
    github-repo-to-watch = "ampproject/amphtml"
    github-test-repo = "ampsauce/amphtml"
    ignore-branches-from-watched-repo = true
    trusted-orgs = [ "ampproject" ]
    whitelist = [
        "**.md",
        "/3p/*",
        "/ads/*",
        "/builtins/*",
        "/css/*",
        "/examples/*",
        "/extensions/*",
        "/src/*",
        "/test/*",
        "/testing/*"
        "package.json"
    ]
    file-watchlist = [
        "**.js",
        "**.css",
        "**.html",
    ]
```
