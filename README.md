# scream-install

## FOR WINDOWS SIDE:

- https://github.com/duncanthrax/scream/releases/

## FOR LINUX SIDE:

- yay -S scream

- sudo nano /usr/lib/systemd/user/scream_start.service
```
[Unit]
Description=Start scream
After=default.target

[Service]
Type=simple
ExecStart=scream -v -i virbr1
Restart=always

[Install]
WantedBy=default.target
```

- systemctl --user enable scream_start.service
- systemctl --user start scream_start.service
- systemctl --user status scream_start.service
  
## Firewall

- Allow port 4010 in ufw

## Git note set editor with before commit

- export GIT_EDITOR=nano
