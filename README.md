# hyperirc

Read IRC through hypercore.

## What is it?

Hyperirc is a bot that mirrors irc channels to a [hypercore](https;//github.com/mafintosh/hypercore) append-only log.
This allows you to read an IRC channel using the hypercore p2p network. Anyone who is reading the irc logs is also helping hosting them.

## Usage

```
npm install -g hyperirc
```

## Usage

First, somewhere, start a mirror.

``` sh
hyperirc --mirror=an-irc-channel
```

This will mirror `an-irc-channel` on freenode into a hyperdrive feed.
The feed key is printed out.

Then on a couple of other computers run this to tail the channel

``` sh
hyperirc --tail=the-key-printed-out-above
```

Thats it! Every peer tailing (and the peer mirroring) will join the p2p network and help eachother host the irc logs.

For more options run `hyperirc --help`.

## License

MIT