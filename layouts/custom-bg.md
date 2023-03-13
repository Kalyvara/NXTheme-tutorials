# Add or edit a custom background image to any theme

*Written by [Capybara](https://themezer.net/creators/382997176307154945), March 2023*

<div align="center">
<img src="https://avatars.githubusercontent.com/u/65415089?s=200&v=4" />
</div>

<br />
I've been receiving *a lot* of requests about that while the process is actually really simple. Once and for all, this short tutorial will describe how to customize a theme with the background image of your choice, whatever base layout you picked.

## Table of contents

- **[I. Choosing a background image](#i-choosing-a-background-image)**
- **[II. Picking a layout](#ii-picking-a-layout)**
- **[III. Building with Switch Theme Injector](#ii-building-with-switch-theme-injector)**

## Requirements

- Windows 10 or 11
- [Switch Theme Injector](https://github.com/exelix11/SwitchThemeInjector/releases)
- The layout of your choice if the default ones provided by Switch Theme Injector don't suit you
- Your image (duh)
- Probably a photo editor (e.g. Photoshop, paint.NET, GIMP, etc.)

## I. Choosing a background image

Pick whatever image you want, **as long as it meets these two requirements**:

- Properly sized: **1280x720**
- Properly formatted: `.jpg` with baseline/standard encoding **OR** `.dds` with DXT1 encoding

You will most likely need a photo editor for your image to fill these conditions, otherwise Switch Theme Injector won't compile your theme. The encoding part should be straightforward as you should be prompted by the software you are using to set that properly. To convert any image file to a DXT1 encoded `.dds`, I recommend using paint.NET.

*NB: while `.jpg` doesn't handle transparency at all, DXT1 `.dds` does it very poorly. I don't recommend getting fancy with transparency if using `.dds`. It should be fine if your image only contains areas at FULL transparency, but any intermediate opacity value in your image will cause ugly glitches.*

## II. Picking a layout

Layouts determine the position, size and colors (and animations in some themes) of the different UI elements, making them (the layouts, that is) the main part of a custom theme. They come as `.json` files and are used to patch the `.szs` files located in `themes/systemData` on your SD card to create themes. Each applet (e.g. home screen, lock screen, etc.) has its own layout.

In order to not affect readability, choose your image accordingly because colors from the layout you picked obviously won't adjust by themselves (in some cases, switching to either dark or light mode in your console settings might help though).

Switch Theme Injector provides default layouts. If they don't satisfy you, you can also download any layout off [Themezer](https://themezer.net/) and use your own image with it. A theme layout can be downloaded from any individual theme page. Note that you can also download a theme's background image from the same page.

*(screenshot to be provided)*

Alternatively, if you are in possession of a `.nxtheme` file and want to extract its assets, you can do so through Switch Theme Injector. Layouts as well as image files will be extracted during the process.

*(screenshot to be provided)*

Note that some home menu themes also provide a common layout (`common.json`) which will be needed to build our `.nxtheme`. In general, you can tell at first glance by seeing whether the footer section (containing buttons and controllers icons) has been altered or not.

*(screenshot to be provided)*

## III. Building with Switch Theme Injector

*(screenshot to be provided)*

Now for the final part. Open up Switch Theme Injector and you should be in the `NXTHEME BUILDER` tab. Select your applet (home screen in my example), browse your background image and the layout you chose and then confirm by clicking `BUILD NXTHEME`. Choose your preferred save location. If all done correctly, you won't be prompted by any error message and a `.nxtheme` file will be output. You can then proceed on installing your theme using NXTheme Installer after putting your compiled `.nxtheme` in the `themes` folder of your SD card.

*(screenshot to be provided)*