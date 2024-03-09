# d2coding-nerd-font
My own take to d2coding nerd font patch, based on Nerd Font v3.1.1

# Patch argument

`--xavgcharwidth --complete --has-no-italic`

Some characters of D2Coding overwraps with nerd font - like weather glyphs, and I just overwrited it.

# Preview
![스크린샷 2024-03-09 014314](https://github.com/dhnam/d2coding-nerd-font/assets/8546820/cd827f0d-49c3-43a2-af5b-620ebf42e944)
![image](https://github.com/dhnam/d2coding-nerd-font/assets/8546820/dafec432-0836-447e-ba29-1d2876d03399)
![image](https://github.com/dhnam/d2coding-nerd-font/assets/8546820/26647527-d630-43da-8336-5dda02006e79)

Powerlime works well, too!

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
at line 112

and (if you're using `battery` module) part:
```
# Battery pictograms going from low to high level of charge.
  typeset -g POWERLEVEL9K_BATTERY_STAGES='\UF008E\UF007A\UF007B\UF007C\UF007D\UF007E\UF007F\UF0080\UF0081\UF0082\UF0079'
```
at line 1461

accordingly, and it'll be almost good.

