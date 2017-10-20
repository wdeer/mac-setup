Configuring Terminal

`ulimit -n 10240` - bumps the maximum number of file descriptors you can have open on your computer. There's no purpose for the default limit, especially on SSDs.

`export JOBS=max` - tells npm to compile and install all your native addons in parallel and not sequentially. This greatly increases installation times

`alias fuck='$(thefuck $(fc -ln -1))'`

or if you don't like foul language:

`alias frick='$(thefuck $(fc -ln -1))'`