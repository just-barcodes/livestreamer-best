# livestreamer-best

Whenever I use [livestreamer](https://github.com/chrippa/livestreamer), I always
use `livestreamer http://stream best` (with the `best` option). This simple
script calls best automatically, so that I can copy the address of the stream
and just call `live` (and the adress will automatically be pasted to the
terminal using `xclip`).


### Installation

Give permission

```
chmod a+x intall
```

and then run the install with an optional name (default is `live`) for the
script (you will probably need to `sudo` that)

```
./install [name]
```


### Example Usage

Copy a stream-address to your clipboard (`Ctrl-C`), open a terminal and call

```
live
```

(or whatever name you chose)

You can also still specify a stream-address directly:

```
live http://www.twitch.tv/day9tv
```
