# Waybar - Privacy Dots

A privacy-first module for your status bar.  
Displays the status of your microphone, camera, and location with beautiful colored dots.

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

