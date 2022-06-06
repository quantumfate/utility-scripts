# setnptrue as a systemd service

Make the script executable

`` chmod +x setntptrue ``

Create a systemd service to execute the script as sudo on startup.
**Don't** use dynamic variables for the home directory.

Paste the following into your terminal.

```bash
cat <<EOF >>/etc/systemd/system/setntp.service
[Unit]
Description=Set timedatectl to use ntp for clock synchronization

[Servive]
ExecStart=home/<username>/.script/Timesync/setntptrue

[Install]
WantedBy=multi-user.target
EOF
```

Enable the serice.

`` sudo systemctl enaable setntp.service``
