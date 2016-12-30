# iTerm, without Titlebar or borders, with increased margin

This repository is inspired by [jaredculp/iterm2-borderless-padding](https://github.com/jaredculp/iterm2-borderless-padding) but as his repository is no longer being maintained I figured I should take over.

## What is this?

This repository contains a small and simple patch that removes the titlebar and borders from the standard iTerm and also adds some margin on either side (currently a hardcoded 25px).

_Also: Work in progress._ I will add a better description and some configuration options later.

## How does it work?

It's as easy as pie: You check out the official __iTerm__ repository, jump to the currently supported release and apply the patch in this repository.

```bash
git clone https://github.com/feliix42/iterm2-no-titlebar
cd iterm2-no-titlebar
git clone https://github.com/gnachman/iTerm2
cd iTerm2

git checkout 3.0.14
git apply ../0001-NoTitleBar-extraSpace.patch
make
```

And: _You're done!_ :tada:

## Caveats

Please note that you won't be able to interact with your iTerm window as you used to. Dragging around and minimizing/maximizing will _not_ work anymore as there is no titlebar. It's intended to be used with something like [Spectacle](https://www.spectacleapp.com) or the wonderful [kwm](https://github.com/koekeishiya/kwm) who will take care of that for you.
