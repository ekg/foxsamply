# foxsamply

rendering algorithmic beats

## what is it?

This script wraps up the initialization and teardown of the environment required for FoxDot, pipes in a code snippet, and records the given number of seconds of the resulting audio.
It converts FoxDot code to recorded samples.

foxsamply is designed for use on headless servers.
It depends on Xvfb (supercollider panics without X11), jack (we'll use a dummy sound card), supercollider (it's run headless from a set script), and FoxDot (which eats our beat).

## Usage:

Running:

```
foxsamply -f beats.foxdot -s 10 -o beats
```

... will emit beats.mp3 and beats.wav.

A recording start delay can be configured to deal with latency causing silence at the beginning of the recorded audio.