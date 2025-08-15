# Waybar- Privacy Dots
A privacy-first module for your Status bar. 
Determine the microphone, camera and Location status and render them with beautiful dots.

## Capabilities
**Mic Status:** The status of microphone(s), Show a green dot (<span style="color:#30D158;">●</span>) when any of them are in-use.  
**Cam Status:** The status of Camera(s), Similar to mic, but render in orange (<span style="color:#FF9F0A;">●</span>) by default.  
**Loc Status:** The Status of Location, but as a blue dot (<span style="color:#0A84FF;">●</span>).   
**Easy to Customize:** Do you want to add another status or change the colors? Easy-peasy. It's a simple bash script for functionality and CSS for Styling.

## Defaults
The backend script polls status info every 3 seconds by default.
This include **formatted text, tootltip and styling class**
then `waybar` render them via colored dots as shown bellow.
The Colors and interval can configured.

<table>
  <tr>
    <th>mic</th>
    <th>cam</th>
    <th>loc</th>
    <th>inactive</th>
    <th>interval</th>
  </tr>
<tr>
    <td><span style="color:#30D158;">●</span></td>
    <td><span style="color:#FF9F0A;">●</span></td>
    <td><span style="color:#0A84FF;">●</span></td>
    <td><span style="color:#555555;">●</span></td>
    <td>3 sec</td>
    
</tr>
</table>

