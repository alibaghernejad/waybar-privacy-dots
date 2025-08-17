# Waybar - Privacy Dots

A privacy-first module for your status bar.  
Displays the status of your microphone, camera, and location with beautiful colored dots.

![Status dots displayed in Waybar showing microphone, camera, and location indicators in green, orange, and blue](./assets/waybar-privacy-dots2.png)

## Capabilities

- **Mic Status:** Shows a green dot (<span style="color:#30D158;">●</span>) when any microphone is in use.
- **Cam Status:** Shows an orange dot (<span style="color:#FF9F0A;">●</span>) when any camera is active.
- **Loc Status:** Shows a blue dot (<span style="color:#0A84FF;">●</span>) when location services are in use.
- **Easy to Customize:** Add new statuses or change colors easily. The functionality is handled by a simple Bash script, and styling is managed with CSS.

## Defaults

The backend script polls status information every 3 seconds by default.  
It provides formatted text, tooltips, and styling classes, which `waybar` uses to render the colored dots as shown below.  
Colors and polling interval are configurable.

| mic | cam | loc | inactive | interval |
|-----|-----|-----|----------|----------|
| <span style="color:#30D158;">●</span> | <span style="color:#FF9F0A;">●</span> | <span style="color:#0A84FF;">●</span> | <span style="color:#555555;">●</span> | 3 sec |


## Installation

Make sure `waybar` is installed on your system, then follow these steps to set up the privacy dots module:

1. Create the scripts directory in your waybar config folder:
```shell
cd ~/.config/waybar 
mkdir scripts
```

2. Then download and locate the `privacydots.sh` script in the scripts folder:
```shell
curl -o ~/.config/waybar/scripts/privacydots.sh https://raw.githubusercontent.com/your-username/waybar-privacy-dots/main/privacydots.sh
chmod +x ~/.config/waybar/scripts/privacydots.sh
```
3. Add the `privacydots` module to your waybar configuration file (`~/.config/waybar/config`). Here's a sample configuration:

```jsonc
{
    "custom/privacydots": {
        "exec": "~/.config/waybar/scripts/privacydots.sh",
        "return-type": "json",
        "interval": 3,
        "format": "{text}",
        "tooltip": true,
        "escape": false,
        "markup": "pango"
    }
}
```

You can add this module to any section (`modules-left`, `modules-center`, or `modules-right`) according to your preference. For example, to add it to the center:

```jsonc
"modules-center": ["clock", "custom/privacydots"]
```

A complete example configuration might look like this [sample configuration](/config/waybar/config.jsonc).



## Optional Styling
