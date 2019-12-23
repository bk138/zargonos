# zargonos
Zargon's stuff

## Dependencies

`sudo apt-get install espeak sox expect pocketsphinx pocketsphinx-en-us pulseaudio`

## How To Setup Remote Client Pulseaudio via SSH

* If you get `pa_context_connect() failed: Connection refused`, run `pax11publish -r` once.
* `sudo apt install pulseaudio-module-zeroconf` and add `load-module module-zeroconf-discover`
  to `/etc/pulse/default.pa`.
* Run `pacmd list-sinks | grep name:` and note your favourite sink after `name:`, call
  `pacmd set-default-sink <sink name without brackets>` once.

