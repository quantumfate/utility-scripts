# Change the brightness level of your laptops display

## Install Brillo

For non arch users:

Install and follow the steps over at the [brillo repository](https://gitlab.com/cameronnemo/brillo).

For arch users:

`` yay -S brillo ``

## Install dunst

If you want to use the notification install [dunst](https://wiki.archlinux.org/title/Dunst#Installation).

For arch users:

`` yay -S dunst ``

Make the script executable.

`` chmod +x changebrightness ``

Add your user to the video group

`` usermod -aG video $USER ``

## Bind the script to your favorite shortcut utility

Make the script globally executable.

`` sudo ln changebrightness /usr/local/bin/changebrightness ``

For awesome Users:

```lua
globalkeys = gears.table.join(
	
	
)
```
