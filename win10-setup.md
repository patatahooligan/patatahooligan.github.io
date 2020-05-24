These are my notes on getting a default windows 10 to behave like I want it.
Mostly, this means getting rid of bloat, changing insane default settings to
sane ones, and removing as many privacy & security liabilities as possible.

For now these are raw notes of my in-progress work. Expect more TODOs than
actual info, but we'll get there eventually. I'll probably want to script this
in the future, so it's better to look for solutions through Powershell rather
than gui-based.

# TODOs

* Disable telemetry (to the extent that it's possible). During installation, we
  are only presented with the choices basic/full. But even basic contains a
  shitload of info we'd rather not share. Find a way to minimize/eliminate that.

* Set hardware clock to UTC. It makes more sense and it plays better with linux.

* Shift through the services and bundled software and remove everything
  unnecessary.
