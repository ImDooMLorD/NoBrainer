140420241502
Status: #idea
Tags: 

# Lf File Manger
#### - Terminal file manager
 normally icons can be integrated by coping some lines from github to bash or zsh config file.
 But for some reason its not working with fish so -

 ### To get icons in lf with fish shell
 1. Install fisher from [here](https://github.com/jorgebucaran/fisher)
```
$ curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher
```
2. Yes, this is one line. Now install the plugin via fisher:
```
fisher install joshmedeski/fish-lf-icons
```
3. Then make sure you set icons in your ~/.config/lf/lfrc file.
```
set icons true
```


___
## References
- Introduction - [youtube link](https://www.youtube.com/watch?v=2oWqD3JCXuI)
- Official github repo - [lf file manager](https://github.com/gokcehan/lf)
- [Eric murphy's lfrc](https://github.com/ericmurphyxyz/dotfiles/blob/master/.config/lf/lfrc)
- [icons for fish shell](https://parasurv.neocities.org/linux-wiki/how-to-lf-icons-with-fish-shell)