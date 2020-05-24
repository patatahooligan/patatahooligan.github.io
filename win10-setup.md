These are my notes on getting a default windows 10 to behave like I want it.
Mostly, this means getting rid of bloat, changing insane default settings to
sane ones, and removing as many privacy & security liabilities as possible.

For now these are raw notes of my in-progress work. Expect more TODOs than
actual info, but we'll get there eventually. I'll probably want to script this
in the future, so it's better to look for solutions through Powershell rather
than gui-based. If enough steps are scriptable I'll probably set up a separate
git repo with helper scripts.

# TODOs

* Disable telemetry (to the extent that it's possible). During installation, we
  are only presented with the choices basic/full. But even basic contains a
  shitload of info we'd rather not share. Find a way to minimize/eliminate that.

* Sift through the services and bundled software and remove everything
  unnecessary.

* Try out the new package manager (winget) and decide whether it serves a
  purpose and should be part of our default installation.

# Set hardware clock to UTC

It makes sense to have it at an international standard time and apply
modifications such as timezones and daylight savings on the software level. This
is what gnu/linux does by default and therefore it makes dual-booting smoother.
Apply this change to the registry by saving the following into a .reg file and
running it.

```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation]
"RealTimeIsUniversal"=dword:00000001
``` 
