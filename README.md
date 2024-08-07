# libgenx - Library Genesis Explorer

**A simple GUI application to download content from [Library Genesis](https://libgen.is/).**

The application is...

- developed and maintained on [Manjaro Linux](https://manjaro.org/) and can be run on Linux systems
- utilizing the [libgen-api](https://github.com/harrison-broadbent/libgen-api) library
- usable in GUI and console mode

The [icons](https://store.kde.org/p/2068651) used in the project are open source.

## Installation

1. The following packages have to be installed from the package manager: git, python, python-pip, python-pipenv, qt6-base (most of these are pre-installed on many Linux systems)
2. Open a console somewhere in your home folder (e.g. ~/src) and clone the git repository: `git clone https://github.com/gaaldvd/libgenx.git`
3. cd to the downloaded folder: `cd libgenx`
4. Run the installation script: `sh install.sh`

## Usage

Both modes can be started from the libgenx folder (if the folder is not added to PATH) using console arguments: `./libgenx.sh [-c/-g] [-a 'author'] [-t 'title']`

The author and title arguments are optional. Searching based on both author and title is [not yet implemented](TODO.md#libgenx_common), as of now only one of the flags should be used (-a or -t).

The config.json file contains the default download directory and the pdf-only option. These can be changed manually or in the GUI app.

### GUI

The user interface is straightforward. The config pane can be opened from the toolbar. Search results are listed under the input fields. Any item can be downloaded by double-clicking on it. If the default download mirror doesn't work for some reason, alternate options are listed for every item in the right-click context menu.

### CLI

The console mode can be used with or without the optional arguments, [as mentioned above](#usage) in the beginning of the section.

### Updating

The update.sh file prompts the user, then updates the git repository and the Python packages: `./update.sh`

## Development

Feel free to clone or fork the repository. Most of the current issues are listed in the [TODO file](TODO.md).
