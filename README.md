# st

My build of [st](https://st.suckless.org/).

## Bindings

* **change transparency** with <kbd>alt-a</kbd>, <kbd>alt-s</kbd>.

## Patches and features

* [**alpha-0.8.5**](https://st.suckless.org/patches/alpha/st-alpha-20220206-0.8.5.diff) provides transparency -- make sure you have a composite manager (such as `xcompmgr` or `picom`) installed for this to work.
    * [This code](https://github.com/LukeSmithxyz/st/commit/73a6020865607018f6442317e7f94fb5d54a7016) lets you change transparency on the fly.
    * [This code](https://github.com/LukeSmithxyz/st/commit/ffcacfa98d1774cfa98d960e8c5244a38d09447e) makes windows completely transparent when set as so.
* [**anysize-20220718-baa9357**](https://st.suckless.org/patches/anysize/st-anysize-20220718-baa9357.diff) allows st to fill the entire space allocated to it.
* [**bold-is-not-bright-20190127-3be4cf1**](https://st.suckless.org/patches/bold-is-not-bright/st-bold-is-not-bright-20190127-3be4cf1.diff) is self-explanatory.
* [**boxdraw_v2-0.8.5**](https://st.suckless.org/patches/boxdraw/st-boxdraw_v2-0.8.5.diff) renders lines/blocks characters better.

## Installation

```sh
git clone https://github.com/thatguynoe/st
cd st
sudo make install
```
