# cmus-fzf

quick and dirty script to play a track from your cmus library using fzf


## setup

1. install [fzf](https://github.com/junegunn/fzf)
2. run `cmus-fzf`


## usage

### tmux popup

I run mine in a tmux popup when using `cmus`. [from my cmus rc](https://github.com/itsjfx/dotfiles/blob/master/.config/cmus/rc#L8):
* `bind -f library S shell tmux popup -e FZF_DEFAULT_OPTS="$FZF_DEFAULT_OPTS" -w 60% -h 60% -E /path/to/cmus-fzf/cmus-fzf`
* and press `S`

you could also bind this globally within tmux to do this from any application, e.g. to control your music within `vim` :)

### any regular terminal

you can spawn a lightweight terminal with a cmus keybind e.g.
* `bind -f library S shell st -e '/path/to/cmus-fzf/cmus-fzf'`


## shout outs

* [gavtory](https://github.com/gavtroy) for their help
* some fzf selection code from [lincheney/fzf-tab-completion](https://github.com/lincheney/fzf-tab-completion)
* and of course [fzf](https://github.com/junegunn/fzf)
