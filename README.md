# d2coding-nerd-font
My own take to d2coding nerd font patch, based on Nerd Font v3.1.1

# Patch argument

`--xavgcharwidth --complete --has-no-italic`

Some characters of D2Coding overwraps with nerd font - like weather glyphs, and I just overwrited it.

# Preview
![스크린샷 2024-03-09 014314](https://github.com/dhnam/d2coding-nerd-font/assets/8546820/cd827f0d-49c3-43a2-af5b-620ebf42e944)

# Use it with Powerlevel10K

Looks like there's currently bug with battery icon, but it's almost compatable with "the official font for powerlevel10k" `MesloLGS NF`

...except it's based on v3.

Use `p10k configure` again, or if you customized yoru p10k so don't want to, edit `~/.zshrc`. If you used `MesloLGS NF` and want to change,

edit part:
```
 # Defines character set used by powerlevel10k. It's best to let `p10k configure` set it for you.
  typeset -g POWERLEVEL9K_MODE=nerdfont-v3
  # When set to `moderate`, some icons will have an extra space after them. This is meant to avoid
  # icon overlap when using non-monospace fonts. When set to `none`, spaces are not added.
  typeset -g POWERLEVEL9K_ICON_PADDING=moderate
```

accordingly, and it'll be almost good. (except battery part, which you have to edit `~/.zshrc` again, but I cannot make it right now.)

