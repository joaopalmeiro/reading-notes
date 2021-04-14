# Install Google Fonts on Ubuntu

**Source**: Lighton Phiri's [Install Google Fonts](https://gist.github.com/lightonphiri/5811226a1fba0b3df3be73ff2d5b351c) gist.

## Download the relevant font (Roboto)

Go to `https://fonts.google.com/specimen/Roboto` and click on _Download family_

or

`curl -o Roboto.zip https://fonts.google.com/download?family=Roboto`

## Install the font on Ubuntu

- `cd /usr/share/fonts`
- `sudo mkdir googlefonts`
- `cd googlefonts`
- `sudo unzip -d . ~/Downloads/Roboto.zip`
- `sudo chmod -R --reference=/usr/share/fonts/opentype /usr/share/fonts/googlefonts`

## Register the font

`sudo fc-cache -fv`

## Check if the font is installed

```sh
$ fc-match Roboto
Roboto-Regular.ttf: "Roboto" "Regular"
```
