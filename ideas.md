## `toned` - Tone Daemon

the destroyer of devices that duck audio when silent

When sinks are added or removed, checks against `/etc/toned.conf` to see if there is a match, if there is, plays a tone at a given frequency and volume

example `/etc/toned.conf`
```yaml
[[tones]]
  frequency= 20
  volume= 20
  [[tones.match]]
    object.path = "alsa:pcm:0:hdmi:0,2:playback"
```
