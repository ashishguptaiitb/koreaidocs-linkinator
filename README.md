# linkinator configuration and other files

This repository contains linkinator information for Kore.ai docs check, including but not limited to the config file.

# Linkinator for docs

[Linkinator](https://github.com/JustinBeckwith/linkinator/blob/main/README.md) is a command-line link checker. We use it to periodically check the link health of entire doc site on [docs.kore.ai](https://docs.kore.ai).

## How to install

Use the npm command in PowerShell.

`npm install linkinator`

## How to configure

Create a configuration file that suits your needs. I use this [custom config file](linkinator.config.json).

The tool looks for `linkinator.config.json` by default, so you may keep that name for your config file as well. If you choose to have a different file name, then use the `config` parameter to provide the path of your config file.

## Useful commands

| Command | Check what | Formatting | Output destination |
|------------|------------|------------|------------|
| `asd` | One article | Default |  Console  |
| `asd` | One article | CSV |  Console  |
| `asd` | One article | CSV |  Local file  |


Check all html pages in a folder, format the output as CSV, and save it to a local file.

`npx linkinator "**/*.html" --html --format CSV > C:\Users\Ashish.Gupta\Desktop\linkchk.txt`

Check all links on page.html, format the output as CSV, and save it to a local file.

`npx linkinator https://docs.kore.ai/ --format CSV > C:\Users\Ashish.Gupta\Desktop\linkchk.txt`

❗Check all links on the docs website and show results on the console. Don't use this option as it is not possible to process thousands of rows of results on a console.

`npx linkinator https://docs.kore.ai/ --recurse`

Check all links on the docs website and show results on the console.

`npx linkinator https://docs.kore.ai/ --recurse`

## More commands

Use cases:

* Check all links in *a few* help articles and collect the output in a local file. Supply a list of articles via a .txt file.
* Check all links in all files in a folder. Supply the folder path on the command line or run it in the folder itself.
* Throttle link checking to avoid hammering the docs server. Supply time delay between two link checks or number of pings to make per minute.


<br />
Credits to,

* [Justin Beckwith](https://github.com/JustinBeckwith)
