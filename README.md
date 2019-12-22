# zargonos
Zargon's stuff

## Dependencies

`sudo apt-get install espeak sox expect pocketsphinx pocketsphinx-en-us`

## HowTos
### Sending Sound To Remote

Basically not start a pulseaudio server on zargon's boxx, [but simply set the server via an environment variable](https://en.wikibooks.org/wiki/Configuring_Sound_on_Linux/Pulse_Audio/Remote_server).

### Changing The Default Recording Device

To use sound card 1 for recording instead of sound card 0, create a `/etc/asound.conf` with the following contents:

```
 pcm.!default {
         type asym
         playback.pcm {
                 type plug
                 slave.pcm "hw:0,0"
         }
         capture.pcm {
                 type plug
                 slave.pcm "hw:1,0"
         } 
 }
```

