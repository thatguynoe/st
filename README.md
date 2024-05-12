# st

My build of [st](https://st.suckless.org/).

## Bindings

* **scroll** with <kbd>alt-j</kbd>, <kbd>alt-k</kbd> or <kbd>alt-pgup</kbd>, <kbd>alt-pgdn</kbd> or <kbd>alt-↑</kbd>, <kbd>alt-↓</kbd>. Scroll faster with <kbd>alt-u</kbd>, <kbd>alt-d</kbd>.
* **change font size** with the same bindings as above, but with holding down shift. Reset with <kbd>alt-home</kbd>.
* **change transparency** with <kbd>alt-a</kbd>, <kbd>alt-s</kbd>.
* **copy text** with <kbd>alt-y</kbd>, **paste** with <kbd>alt-p</kbd> or <kbd>shift-insert</kbd>.
* **copy command output** with <kbd>alt-o</kbd>, **open urls** with <kbd>alt-l</kbd>, and **copy urls** with <kbd>alt-i</kbd>.

## Patches and features

* [**alpha-0.8.5**](https://st.suckless.org/patches/alpha/st-alpha-20220206-0.8.5.diff) provides transparency -- make sure you have a composite manager (such as `xcompmgr` or `picom`) installed for this to work.
    * [This code](https://github.com/LukeSmithxyz/st/commit/73a6020865607018f6442317e7f94fb5d54a7016) lets you change transparency on the fly.
    * [This code](https://github.com/LukeSmithxyz/st/commit/ffcacfa98d1774cfa98d960e8c5244a38d09447e) makes windows completely transparent when set as so.
* [**anysize-20220718-baa9357**](https://st.suckless.org/patches/anysize/st-anysize-20220718-baa9357.diff) allows st to fill the entire space allocated to it.
* [**bold-is-not-bright-20190127-3be4cf1**](https://st.suckless.org/patches/bold-is-not-bright/st-bold-is-not-bright-20190127-3be4cf1.diff) is self-explanatory.
* [**boxdraw_v2-0.8.5**](https://st.suckless.org/patches/boxdraw/st-boxdraw_v2-0.8.5.diff) renders lines/blocks characters better.
* [This patch](https://github.com/nimaipatel/st/blob/master/patches/7672445bab01cb4e861651dc540566ac22e25812.diff) prevents cutting off text after resizing.
* [**csi_22_23-0.8.5**](https://st.suckless.org/patches/csi_22_23/st-csi_22_23-0.8.5.diff) saves and restores the window title (e.g. when opening and closing neovim).
* [**externalpipe-0.8.4**](https://st.suckless.org/patches/externalpipe/st-externalpipe-0.8.4.diff) provides functionality for opening and copying urls.
    * [**externalpipe-eternal-0.8.3**](https://st.suckless.org/patches/externalpipe/st-externalpipe-eternal-0.8.3.diff) lets externalpipe see the entire terminal history.
* [**font2-0.8.5**](https://st.suckless.org/patches/font2/st-font2-0.8.5.diff) adds support for multiple fonts.
* [**glyph-wide-support-boxdraw-20220411-ef05519**](https://st.suckless.org/patches/glyph_wide_support/st-glyph-wide-support-boxdraw-20220411-ef05519.diff) fixes wide glyphs truncation (e.g. italic text).
* [**gruvbox-dark-0.8.5**](https://st.suckless.org/patches/gruvbox/st-gruvbox-dark-0.8.5.diff) enables the gruvbox theme.
* [**scrollback-0.8.5**](https://st.suckless.org/patches/scrollback/st-scrollback-0.8.5.diff) along with the three patches below allows for scrolling in st using the keyboard and/or mouse.
    * [**scrollback-mouse-20220127-2c5edf2**](https://st.suckless.org/patches/scrollback/st-scrollback-mouse-20220127-2c5edf2.diff)
    * [**scrollback-mouse-altscreen-20220127-2c5edf2**](https://st.suckless.org/patches/scrollback/st-scrollback-mouse-altscreen-20220127-2c5edf2.diff)
    * [**scrollback-mouse-increment-0.8.2**](https://st.suckless.org/patches/scrollback/st-scrollback-mouse-increment-0.8.2.diff)
* [**vertcenter-20180320-6ac8c8a**](https://st.suckless.org/patches/vertcenter/st-vertcenter-20180320-6ac8c8a.diff) vertically centers lines.

## Installation

```sh
git clone https://github.com/thatguynoe/st
cd st
sudo make install
```

### Updates

The suckless st development branch is the `master` branch in this repo. Consequently, this makes updating st quite easy:

```sh
git clone https://github.com/thatguynoe/st
cd st

git switch master
git pull upstream master
git switch main
git merge master
```
