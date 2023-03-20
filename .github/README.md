<div align="center">
    <img src="https://st.suckless.org/st.svg" alt="st logo">
</div>
<div align="center">
Custom build of <a href="https://st.suckless.org">st</a>, a simple terminal emulator for <a href="https://www.x.org/wiki/">X</a>.
</div>
<p></p>
<div align="center">
    	<a href="https://github.com/kelvin-van-vuuren/st#about">About</a>
  <span> • </span>
       	<a href="https://github.com/kelvin-van-vuuren/st#features">Features</a>
  <span> • </span>
       	<a href="https://github.com/kelvin-van-vuuren/st#screenshots">Screenshots</a>
  <span> • </span>
	<a href="https://github.com/kelvin-van-vuuren/st#Install">Install</a>
  <span> • </span>
	<a href="https://github.com/kelvin-van-vuuren/st#Keybindings">Keybindings</a>
  <p></p>
</div>

![2023-03-20-212325_3840x2160_scrot](https://user-images.githubusercontent.com/54939625/226474564-86acbbb9-ad0f-4ad5-9f05-bed90fc8cf05.png)

### About
[st](https://st.suckless.org) is a simple [terminal emulator](https://en.wikipedia.org/wiki/Terminal_emulator) for [X](https://www.x.org/wiki/) from [suckless](https://suckless.org). The base distribution of this software adheres to the [suckless philosophy]("https://suckless.org/philosophy") and as a result comes with a very minimal set of features. This fork extends the functionality and appearance of the program through the use of [patches]("https://st.suckless.org/patches") and [other changes to the codebase](https://github.com/kelvin-van-vuuren/st/commits/main).

### Features
* [**Scrollback**](https://st.suckless.org/patches/scrollback/): scroll back / forward through terminal output with ``MOD k / j``.
* [**Column and row reflow**](https://st.suckless.org/patches/scrollback/): allow column and rows to reflow so output is not cut off after resizing.
* [**Mousewheel scrollback**](https://st.suckless.org/patches/scrollback/): scroll back / forward through terminal output with ``mousewheel``.
* [**Alpha**](https://st.suckless.org/patches/alpha/): change opacity of terminal background.
* [**Anysize**](https://st.suckless.org/patches/anysize/): allows st to resize to any pixel size, makes the inner border size dynamic, and centers the content of the terminal so that the left/right and top/bottom borders are balanced. With this patch, st on a tiling WM will always fill the entire space allocated to it.
* [**Blinking cursor**](https://st.suckless.org/patches/blinking_cursor/): change cursor style (currently set to blinking underline).
* [**Bold is not bright**](https://st.suckless.org/patches/bold-is-not-bright/): by default, bold text is rendered with a bold font in the bright variant of the current color. This patch makes bold text rendered simply as bold, leaving the color unaffected.
* [**External pipe**](https://st.suckless.org/patches/externalpipe/): read and write to st's screen with an external pipe. Can be used with the entire terminal history.
* [**Copy command output**](https://github.com/kelvin-van-vuuren/st/commit/016b4d4dbae4577baf8e51521544eedb1c2d567e): using dmenu to list and select previous commands, copy output to clipboard using ``MOD o``.
* [**Copy url**](https://github.com/kelvin-van-vuuren/st/commit/016b4d4dbae4577baf8e51521544eedb1c2d567e): using dmenu to list and select urls in terminal history, copy url using ``MOD y``.
* [**Open url**](https://github.com/kelvin-van-vuuren/st/commit/016b4d4dbae4577baf8e51521544eedb1c2d567e): using dmenu to list and select urls in terminal history, open url using ``MOD l``.
* [**Xresources**](https://st.suckless.org/patches/xresources-with-reload-signal/): configure st via [Xresources](https://en.wikipedia.org/wiki/X_resources). Pass a USR1 signal to all st processes after updating Xresources to reload the settings on the fly: ``pidof st | xargs kill -s USR1``.
* [**Ligatures**](https://st.suckless.org/patches/ligatures/): correct drawing of ligatures.
* [**Icon**](): set NET_WM_ICON with a png image. This can then be read in from another program such as a [window manager](https://github.com/kelvin-van-vuuren/dwm). The icon used is [``st.png``](https://github.com/kelvin-van-vuuren/st/blob/main/st.png).
* [**Right click paste**](https://st.suckless.org/patches/rightclickpaste/): pressing right click will paste to terminal.
* [**Undercurl**](https://st.suckless.org/patches/undercurl/): support for special underline styles.

### Install
Clone this repo and install with ``rm -rf config.h && sudo make clean install``. Configuration is done via [config.def.h](https://github.com/kelvin-van-vuuren/st/blob/main/config.def.h) so any changes will require the program to be recompiled and installed to take effect.

### Screenshots
![2023-03-21-092233_3840x2160_scrot](https://user-images.githubusercontent.com/54939625/226564286-437844a9-5fb0-4864-8780-eda2673c0577.png)
![2023-03-21-091026_3840x2160_scrot](https://user-images.githubusercontent.com/54939625/226564398-bbe04810-1a34-4ffe-ad37-70ac25221c41.png)
![2023-03-21-091003_3840x2160_scrot](https://user-images.githubusercontent.com/54939625/226564456-f01b4d52-d1ff-4c26-9400-8286eeacc365.png)


### Keybindings
These are set in [config.def.h](https://github.com/kelvin-van-vuuren/st/blob/main/config.def.h#L268). The ``MOD`` key is set to Mod1, which I have as ``alt`` on my system.
<div align="center">
<table>
<colgroup>
<col style="text-align:center;"/>
<col style="text-align:left;"/>
</colgroup>

<thead>
<tr>
	<th style="text-align:center;">Keys</th>
	<th style="text-align:left;">Function</th>
</tr>
</thead>

<tbody>
<tr>
	<td style="text-align:center;">MOD k</td>
	<td style="text-align:left;">Scroll up</td>
</tr>
<tr>
	<td style="text-align:center;">MOD j</td>
	<td style="text-align:left;">Scroll down</td>
</tr>
<tr>
	<td style="text-align:center;">MOD u</td>
	<td style="text-align:left;">Scroll up x10</td>
</tr>
<tr>
	<td style="text-align:center;">MOD d</td>
	<td style="text-align:left;">Scroll down x10</td>
</tr>
<tr>
	<td style="text-align:center;">MOD l</td>
	<td style="text-align:left;">Open URL</td>
</tr>
<tr>
	<td style="text-align:center;">MOD y</td>
	<td style="text-align:left;">Copy URL</td>
</tr>
<tr>
	<td style="text-align:center;">MOD o</td>
	<td style="text-align:left;">Copy command output</td>
</tr>
<tr>
	<td style="text-align:center;">Control Shift c</td>
	<td style="text-align:left;">Copy to clipboard</td>
</tr>
<tr>
	<td style="text-align:center;">Control Shift v</td>
	<td style="text-align:left;">Paste from clipboard</td>
</tr>
<tr>
	<td style="text-align:center;">Control Shift y</td>
	<td style="text-align:left;">Paste selected</td>
</tr>
<tr>
	<td style="text-align:center;">Control Shift k</td>
	<td style="text-align:left;">Zoom in</td>
</tr>
<tr>
	<td style="text-align:center;">Control Shift j</td>
	<td style="text-align:left;">Zoom out</td>
</tr>
</table>
</div>
