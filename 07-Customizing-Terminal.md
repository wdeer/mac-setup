# Configuring Terminal
### ( ... this set of instructions is a work in progress)

## .YADR
.yadr does ALOT to make your terminal more *fun* but there are a number of things you can do to customize it to your preferences. 

## Default settings
Add some useful defaults to your ~/.zshrc

`ulimit -n 10240` - bumps the maximum number of file descriptors you can have open on your computer. There's no purpose for the default limit, especially on SSDs.

`export JOBS=max` - tells npm to compile and install all your native addons in parallel and not sequentially. This greatly increases installation times

## F**K

**thefuck** is a *nice* little utility that corrects your previous console command if you made a mistake

	brew install thefuck

Then add the following to your ~/.zshrc

`alias fuck='$(thefuck $(fc -ln -1))'`

or if you don't like foul language:

`alias frick='$(thefuck $(fc -ln -1))'`

ooorrr if you're a fan of Battlestar Galactica 

`alias frack='$(thefuck $(fc -ln -1))'`

Now if you goof up a command you can quickly just type **fuck** (or frick or frack) and it will try to correct the command for you (note: this improves over time) see [https://github.com/nvbn/thefuck](https://github.com/nvbn/thefuck) for more details.

