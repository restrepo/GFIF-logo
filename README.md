[![gfif_path.svg](gfif_path.svg)](./gfif_path.svg)

The `_path_` versions does not require install new fonts.

To open with the proper fonts, use the inkscape of gfif or
install Good Times Font (included) in debian

```bash
# mkdir /usr/share/fonts/truetype/ttf-good-times/
# cp good-times.ttf /usr/share/fonts/truetype/ttf-good-times/
```

DEBIAN:
```bash
# fc-cache -fv
```

UBUNTU:

```bash
# defoma-hints -c --no-question truetype /usr/share/fonts/truetype/ttf-good-times/* > /etc/defoma/hints/ownfonts.hints
```

Now you register this file to defoma:

```bash
# defoma-font register-all /etc/defoma/hints/ownfonts.hints 
```

The last thing you have to do is to apply the new configuration. The quickest way is to call

```bash
# defoma-reconfigure
```

It updates the fonts database for all registered applications. To use the new fonts in your current X session, run

```bash
# xset fp rehash
```
