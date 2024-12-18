<img align="right" src="https://github.com/jafarlihi/file-hosting/blob/master/rssnix-logo.png?raw=true">

## TOC

* [Demonstration](#demonstration)
* [Installation](#installation)
* [Packages](#packages)
* [Flags](#flags)
* [Config](#config)

## Demonstration

![Demo](https://raw.githubusercontent.com/jafarlihi/file-hosting/master/rssnix-demo.gif?raw=true)

## Installation

You need to have Go >=1.19 installed.

`git clone https://github.com/jafarlihi/rssnix --depth=1 && cd rssnix && go install`

## Packages

<a href="https://aur.archlinux.org/packages/rssnix-git">Arch Linux AUR Package</a>

## Flags

`config`
- Opens config file with `$EDITOR`

`update [feed name]`
- If [feed name] argument is given and is space-delimited list of feeds, then these feeds are updated
- If no [feed name] argument is given then all feeds are updated

`open [feed name]`
- If [feed name] argument is given then the said feed's directory is opened with the configured viewer
- If no [feed name] argument is given then the root feeds directory is opened with the configured viewer

`add [feed name] [feed url]`
- Adds a new feed to the config file

`import [OPML URL or file path]`
- Imports feeds from OPML file

`version`
- Prints the rssnix version

## Config

Config file is expected to be at `~/.config/rssnix/config.ini`.

Sample config file:

```
[settings]
viewer = vim
feed_directory = ~/rssnix

[feeds]
CNN-Tech = http://rss.cnn.com/rss/edition_technology.rss
HackerNews = https://news.ycombinator.com/rss
```
(Tip: `ranger` is another great candidate for `viewer`)
