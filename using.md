# Linkinator for docs

[Linkinator](https://github.com/JustinBeckwith/linkinator/blob/main/README.md) is a command line link checker. We use it to periodically check the link health of entire entire doc site on [docs.kore.ai](https://docs.kore.ai).

## How to install

Use the npm command in a PowerShell.

`npm install linkinator`

## How to configure

Create a configuration file that suits your need. I use this [custom config file](linkinator.config.json).

## Useful commands

| Command | Check what | Formatting | Output destination |
|------------|------------|------------|------------|
| `asd` | One article | Default |  Console  |
| `asd` | One article | CSV |  Console  |
| `asd` | One article | CSV |  Local file  |


Check all links on page.html, format the output as CSV, and collect the output in a local file.

`npx linkinator https://docs.kore.ai/ --format CSV > C:\Users\Ashish.Gupta\Desktop\linkchk.txt`

❗Check all links on the docs website and show results on the console. Don't use this option as it is not possible to process thousands of rows of results on a console.

`npx linkinator https://docs.kore.ai/ --recurse`

Check all links on the docs website and show results on the console.

`npx linkinator https://docs.kore.ai/ --recurse`

## More commands

Use cases:

* Check all links in *a few* help articles and collect the output in a local file.
* Throttle link checking to avoid hammering the docs server.
