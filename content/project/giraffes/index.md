---
title: "Outside the Sweet Spot"
subtitle: "An initial analysis into outlier home runs"
excerpt: ""
date: 2023-05-12
author: "Evan Howard"
draft: false
tags:
  - hugo-site
categories:
  - Baseball
  - Home Runs
  - R
# layout options: single or single-sidebar
layout: single
editor_options: 
  markdown: 
    wrap: 72
---

------------------------------------------------------------------------

This project is focusing on all home runs that were hit between the 2015
season and April 9,2023. It is intended to focus on home runs within
different ballparks to see what constitutes an "outlier" home run. I
worked on this project with [Annabel Judd]() and [Julian Coleman](). The
data collected was from [Basbeall Savant]().

When collecting the data we wanted to view all home runs at certain
ballparks. At Baseball Savant we selected Batter as Player Type,
Statcast for Season, Home Run for PA Result. For Season Type we chose
regular season, playoffs, wildcard, division series, league
championship, world series, and all star. Since we wanted to collect all
Home Run data for ballparks we chose to include the all star games.

Once we obtained this data we chose to keep only metrics that we thought
might be useful to our analysis. We kept: pitch type, game date, release
speed, player name, batter id, pitcher id, events, zone, game type,
stand, p throws, home team, away team, bb type, pfx x, pfx z, plate x,
plate z, hc x, hcy, all v 0, all a, sz top, sz bot, hit distance, launch
speed, launch angle, effective speed, release spin rate, release
extension, game pk, estimated ba using speed anlge, estimated woba using
speed anlge, launch speed angle, pitch name, spin axis, delta home win
exp, and delta run exp. Definitions for all column names can be found at
Statcase Search CSV Documention.

In the following strike zone and heatmap plots below, remember that the
view is from the Catcher's per- spective. A Right handed hitter would be
to the left of the strike zone, and a Left handed hitter would be to the
right.

![All home runs by pitch type from 2015-April 9,
2023.](allHRStrikeZone.png)

One of the best features of Tachyons is the exhaustive [component
library](https://www.tachyonstemplates.com/components/?selectedKind=AboutPages&selectedStory=AboutUs&full=0&down=0&left=1&panelRight=0)
contributed by the community. All those components are built to work
with the Tachyons classes, so they will work in this theme too! You can
copy/paste components in order to quickly block out a page, then fill in
your content.

### Taste the Rainbow

We've leveraged the [accessible color
combinations](http://tachyons.io/docs/themes/skins/) included with
Tachyons to offer an easy way for you to setup your site using your
favorite colors. In the site configuration file (`config.toml`), there
is a full set of color parameters giving you control over the theme
color scheme. For an option like `siteBgColor` for example, you can just
type one of the predefined color names from Tachyons and save the file.
You can totally customize the theme colors within minutes of installing
the theme.

``` toml
# basic color options: use only color names as shown in the
# "Color Palette" section of http://tachyons.io/docs/themes/skins/
siteBgColor = "near-white"
sidebarBgColor = "light-gray"
headingColor = "black"
textColor = "dark-gray"
sidebarTextColor = "mid-gray"
bodyLinkColor = "blue"
navLinkColor = "near-black"
sidebarLinkColor = "near-black"
footerTextColor = "silver"
buttonTextColor = "near-white"
buttonBgColor = "black"
buttonHoverTextColor = "white"
buttonHoverBgColor = "blue"
borderColor = "moon-gray"
```

### Dig Deeper

Let's say you have a style guide to follow and `washed-blue` just won't
cut the mustard. We built Blogophonic for you, too. There is a bypass of
these predefined colors built in, you just need to dig a little deeper.
In the theme assets, locate and open the main SCSS file
(`/assets/main.scss`). After the crazy looking variables you probably
don't recognize and directly following the Tachyons import
(`@import 'tachyons';`) you'll see a comment that looks just like this:

``` scss
// uncomment the import below to activate custom-colors
// add your own colors at the top of the imported file
// @import 'custom-colors';
```

Once you uncomment the `custom-colors` import, it will look like this:

``` scss
// uncomment the import below to activate custom-colors
// add your own colors at the top of the imported file
@import "custom-colors";
```

Save that change, and now the color options in the `config.toml` are no
longer active -- they've been bypassed. To customize the colors, locate
and open the `custom-colors` file found in the theme assets
(`/assets/custom-colors.scss`). At the top of that file, you'll find a
whole new set of variables for all the same color options, but this time
you get to assign your own HEX codes.

``` scss
// set your custom colors here
$siteBgColorCustom: #e3e3da;
$sidebarBgColorCustom: #dbdbd2;
$textColorCustom: #666260;
$sidebarTextColorCustom: #666260;
$headingColorCustom: #103742;
$bodyLinkColorCustom: #c4001a;
$navLinkColorCustom: #c4001a;
$sidebarLinkColorCustom: #c4001a;
$footerTextColorCustom: #918f8d;
$buttonTextColorCustom: #f7f7f4;
$buttonHoverTextColorCustom: #f9f9f8;
$buttonBgColorCustom: #103742;
$buttonHoverBgColorCustom: #c4001a;
$borderColorCustom: #c4beb9;
```
