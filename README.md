# pwrmgr

Simple script to suspend laptop when lid is closed

I use these with Ubuntu, I have no idea if these work elsewhere

## pwrmgr.py

Run as root (no, this is not optimal) because normal user isn't authorized to access Upower without Xsession.
python -u => disable stdout buffering (glib mainloop brokes it or smth).
Logger can be used to write stdout into syslog

rc.local or similar:
```
python -u ./pwrmgr.py | logger -t "pwrmgr" &
```

## suspend.py

Suspend computer if

1. Using battery power
2. --force


```
suspend.py [--force]
```
