
# CONCEPT!!! Automations Dwains Dashboard Add-on (more_page)
Automations Dashboard for Home Assistant Dwains Dashboard
##### Created by [Léon van der Linden](https://github.com/LRvdLinden)
##### v1.0.0

![Automation](https://www.iotworldtoday.com/files/2019/11/GettyImages-1097894826-724x432.jpg)

### Prerequisite
- Make sure you have the automations placed in diverse [Groups](https://www.home-assistant.io/integrations/group/) otherwise see how to do that [Here!](https://www.home-assistant.io/integrations/group/) or the example below
```
  group:
    door_notify_group:
    name: Door Notify Group
    entities:
      - automation.achterdeur_open_2
      - automation.voordeur_open
```
- Make a calendar in Google with all the birthdays and sync the calendar with Home Assistant
- Make sure you have installed [fontawesome icons](https://github.com/thomasloven/hass-fontawesome). This can be done manually or directly via hacs.

### Installation Add-on
- Copy the `automation` folder in to the `dwains-dashboard/addons/more_page` directory.
- Open your `more_page.yaml` file in `dwains-dashboard/configs` and add the following;
 ```yaml
     - name: Automations
       main_menu: 'true' #Show this addon in the main navigation bar!
       icon: fas:robot
       path: 'dwains-dashboard/addons/more_page/automation/page.yaml'
```
- Reload the theme configuration via Theme Settings

### Replace the following
 ```yaml
            - type: custom:atomic-calendar-revive
              style: |
                ha-card {
                  border-radius: 5px;
                  background-color: var(--dwains-theme-primary);
                }
                .cal-titleContainer {
                  display: none;
                }
              showProgressBar: false
              eventBarColor: 'var(--dwains-theme-grey)'
              dayWrapperLineColor: 'var(--dwains-theme-grey)'
              timeColor: 'var(--dwains-theme-grey)'
              entities:
                - calendar.friends_birthdays
```
- on line 60: add the correct `entity` or `entities` to show


### Result

![IMG_0542](https://user-images.githubusercontent.com/77990847/114416033-8bfb8c80-9bb0-11eb-8c69-86e1fcfe5cc6.PNG)

