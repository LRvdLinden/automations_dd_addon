<h1 align="center">Automations Dwains Dashboard Add-on (more_page)</h1>

<p align="center">
  <a href="https://dwainscheeren.github.io/dwains-lovelace-dashboard/">
    <img src="https://img.shields.io/badge/Dwains%20Dashboard-Default-299ec2.svg" />
  </a>
  <a href="https://github.com/custom-components/hacs">
    <img src="https://img.shields.io/badge/HACS-Default-orange.svg" />
  </a>
  <a href="https://github.com/LRvdLinden/automations_dd_addon">
    <img src="https://img.shields.io/github/v/release/LRvdLinden/automations_dd_addon" />
  </a>
    <a href="https://github.com/LRvdLinden/">
    <img src="https://img.shields.io/github/followers/LRvdLinden?style=social" />
  </a>
    </a>
    <a href="https://discord.gg/7yt64uX">
    <img src="https://img.shields.io/discord/688401603811999885" />
  </a>
</p>

<p align="center">A automations dashboard to display automations in a nice way.</p>

<p align="center">Created by <a href="https://github.com/LRvdLinden">Léon van der Linden</a>
</p> 

<p align="center">
  <img src="https://www.iotworldtoday.com/files/2019/11/GettyImages-1097894826-724x432.jpg" />
</p>


## Prerequisite
---
- Make sure you have the automations placed in diverse [Groups](https://www.home-assistant.io/integrations/group/), or see how to do that [Here!](https://www.home-assistant.io/integrations/group/) or the example below
```
  group:
    door_notify_group:
    name: Door Notify Group
    entities:
      - automation.backdoor_open
      - automation.frontdoor_open
```
- Make a calendar in Google with all the birthdays and sync the calendar with Home Assistant
- Make sure you have installed [fontawesome icons](https://github.com/thomasloven/hass-fontawesome). This can be done manually or directly via hacs.


## Installation Atomic Calendar Revive
---
HACS (recommended)
Install using HACS component:

- You need HACS installed and configured
- Go to plugins tab
- Search for Atomic Calendar Revive
- If you use the Lovelace Editor then first go to your user provile and enable Advanced Mode
- Now add the follwoing to Configuration -> Lovelace Dashboards -> Resources
 ```yaml
    /hacsfiles/atomic-calendar-revive/atomic-calendar-revive.js
 ```
 
 
## Installation Add-on
---
- Copy the `automation` folder in to the `dwains-dashboard/addons/more_page` directory.
- Open your `more_page.yaml` file in `dwains-dashboard/configs` and add the following;
 ```yaml
     - name: Automations
       main_menu: 'true' #Show this addon in the main navigation bar!
       icon: fas:robot
       path: 'dwains-dashboard/addons/more_page/automation/page.yaml'
```
- Reload the theme configuration via Theme Settings


## Replace the following
---
 ```yaml
     cards:
       - type: 'custom:fold-entity-row'
         head: group.1 #delete number 1 and fill in the correct group name
         entities:
           - automation.1 #delete number 1 and fill in the correct automation name
           - automation.2 #delete number 2 and fill in the correct automation name
       - type: 'custom:fold-entity-row'
         head: group.2 #delete number 2 and fill in the correct group name
         entities:
           - automation.3 #delete number 3 and fill in the correct automation name
           - automation.4 #delete number 4 and fill in the correct automation name
```
- replace all `head:` for the correct `group` name
- replace all `entities:` for the correct one

## add extra rows of automations groups
---

- If you want more entity rows, just add this pease of code
 ```yaml
       - type: 'custom:fold-entity-row'
         head: group.3 #delete number 3 and fill in the correct group name
         entities:
           - automation.5 #delete number 5 and fill in the correct automation name
           - automation.6 #delete number 6 and fill in the correct automation name
```

## Schedular Card
---
<img width="439" alt="image" src="https://user-images.githubusercontent.com/77990847/114762133-acb71400-9d61-11eb-9296-ae70ae510ad6.png">


## Result
---

![IMG_0542](https://user-images.githubusercontent.com/77990847/114416033-8bfb8c80-9bb0-11eb-8c69-86e1fcfe5cc6.PNG)

---
Enjoy my card? Help me out for a couple of :beers: or a :coffee:!

[![coffee](https://www.buymeacoffee.com/assets/img/custom_images/black_img.png)](https://www.buymeacoffee.com/LRvdLinden)
