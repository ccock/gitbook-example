## generate

### ebook converter

- download Calibre: https://calibre-ebook.com/download
- install Calibre
- config Calibre


MACOS:

```sh
sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

Or:

```sh
vi ~/.bash_profile

export EBOOK_PATH=/Applications/calibre.app/Contents/MacOS
export PATH=$PATH:$EBOOK_PATH 

source .bash_profile
```


### cmd

```sh
gitbook pdf

gitbook epub
```
