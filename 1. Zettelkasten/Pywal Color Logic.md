Not sure if this will be helpful at all, but I can explain how I use pywal. I actually don't use wallpapers to generate my pywal themes, rather, I do them by hand. Pywal is just there to make changing the given colourschemes quick and easy (a custom rofi menu helps too). That said, I have a set of rules that I follow to make my themes consistent. I use [terminal.sexy](http://terminal.sexy/) to help make the colourschemes with the following logic:

`$background` is the darkest colour overall  
`$color0` is still dark, but slightly brighter than `$background`  
`$color8` is slightly brighter than `$color0` (medium-dark)  
`$color7` is slightly brighter than `$color8` (medium-bright)  
`$color15` is slightly brighter than `$color7`  
`$foreground` is slightly brighter than `$color15`, and the brightest overall

That gives me a neutral set of shades, and the rest of the colours follow this logic:

`$color9` is the same as `$color1` but slightly brighter, and that continues up to `$color6` and `$color14`. `$cursor` is the only colour that doesn't follow any particular logic. Sometimes it's the same as one of the other colours, other times, it's something completely different. Depends how I feel it fits in.

From there, every application is set to use the neutral shades and colours accordingly in a way where it all makes sense. Some are low contrast, others not so much. It took a little trial and error, but I think I found a method where everything looks good regardless of the colourscheme.

Here's an example json of a colourscheme I created, which I call `boost`. [It looks like this](https://i.imgur.com/BXnkaZ7.png)
```
{
    "alpha": "100",
    "special": {
        "background": "#161616",
        "foreground": "#d0d0d0",
        "cursor": "#ffb300"
    },
    "colors": {
        "color0": "#282828",
        "color1": "#e63973",
        "color2": "#78a840",
        "color3": "#db6e00",
        "color4": "#21adbf",
        "color5": "#6e4ca8",
        "color6": "#0289cc",
        "color7": "#9e9e9e",
        "color8": "#5c5c5c",
        "color9": "#ff4081",
        "color10": "#8bc34a",
        "color11": "#f57c00",
        "color12": "#26c6da",
        "color13": "#7e57c2",
        "color14": "#039be5",
        "color15": "#b8b8b8"
    }
}
```


Oh, and for Firefox, I let GTK handle most of it with pywal's oomox theme. To make things a little more consistent, I also generate my `userChrome.css` during pywal's post-script. I created a SCSS which generates the colours for the top bar and address bar. I could explain how if you're interested.
