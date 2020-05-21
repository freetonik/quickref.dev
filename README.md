# Quickref.dev Community Sources

This repo contains data sources for Quickref.dev — a community-driven search engine for software developers. `sites` contains lists of sites to index, grouped by category. `cards` contains reference cards ([example in action](https://quickref.dev/search?q=clojure&type=all)).

## Contributing

Please, create a pull request to:

- add a site to the index
- add or modify a reference card.

I you want to add a new bang operator (`!foo`), please, create an issue.

Thank you.

## Sites

There are 5 categories of search on Quickref.dev. Each corresponds to a .txt-file of indexed sites:

- All (`all.txt`)
- Docs (`docs.txt`)
- Forums / Q&A (`forums_qa.txt`)
- Blogs (`blogs.txt`)
- Repositories (`repositories.txt`)

Category "All" is compiled automatically by combining all other categories. Quickref.dev searches in all subdomains. For example, if `https://abc.com` is specified, any subdomain of arbitrary depth (`https://x.abc.com`, `https://y.x.abc.com`, etc) are indexed and searched.

## Cards

Each card is structured as follows:

``` yaml
"list of words":
  name: "Name"
  description: "Short one sentence description."
  links:
    website: "https://official_website.com"
    quickstart: "https://official_website.com/getting_started"
    "community docs": "https://clojuredocs.org/"
    "Mailing list": "https://groups.google.com/forum/..."
    subreddit: "https://reddit.com/r/..."
    ...
```

The `"list of words"` is used to match cards to queries. A card is displayed if the user's query contains at least one of the specified words (case insensitive). For example, requests `clojure`, `clj`, `clj list` or `clojure map` will all match this card:

``` yaml
"clojure clj":
  name: "Clojure"
  description: "Dynamically typed, functional dialect of Lisp. Immutable values, strong typing, hosted on JVM and other platforms."
  links:
    website: "https://clojure.org/"
    quickstart: "https://clojure.org/guides/getting_started"
    "community docs": "https://clojuredocs.org/"
    "Learn in Y minutes": "https://learnxinyminutes.com/docs/clojure/"
    "Q&A forum": "https://ask.clojure.org/"
    "Clojurians Slack": "https://clojurians.herokuapp.com/"
    "Mailing list": "https://groups.google.com/forum/#!forum/clojure"
    subreddit: "https://old.reddit.com/r/Clojure/"
```
