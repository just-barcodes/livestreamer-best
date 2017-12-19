# livestreamer-best (now Streamlink)

Whenever I use [Streamlink](https://streamlink.github.io/index.html) (ex
[livestreamer](https://github.com/chrippa/livestreamer)), I always use
`streamlink https://stream best` (with the `best` option). This simple script
calls best automatically, so that I can copy the address of the stream and just
call `live` (and the adress will automatically be pasted to the terminal using
`xclip`).


### Installation

Give permission

```
$> chmod a+x intall
```

and then run the install with an optional name (default is `live`) for the
script (you will probably need to `sudo` that)

```
$> ./install [name]
```


### Example Usage

Copy a stream-address to your clipboard (`Ctrl-C`), open a terminal and call

```
$> live
```

(or whatever name you chose)

You can also still specify a stream-address directly:

```
$> live https://www.twitch.tv/day9tv
```

It will now also work with addresses like
```
$> live https://player.twitch.tv/?channel=day9tv
```
as it will automatically cut out the `?channel=` part. It will also
automatically try to convert `http` to `https` addresses.


### Options

To see options

```
$> live -h
usage: live [-h] [-c] [--no-edit] [--no-stream] [stream]

Livestreamer wrapper

positional arguments:
  stream       stream address

optional arguments:
  -h, --help   show this help message and exit
  -c           open chat in browser
  --no-edit    do not modify stream address
  --no-stream  does not start the stream (only opens chat, if the -c option is
               present)
```

* The `-c` option will try to open the twitch chat in a new private
`chromium-browser` window.
* The `--no-edit` option will prevent any modifications of the stream address.
* The `--no-stream` option will prevent the opening of the stream (in case you
only want to open the chat).
