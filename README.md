# Multiline Entity Card
 A custom entity card modelled on the original Entity card for [Home Assistant](https://www.home-assistant.io/) that allows text to span multiple lines.

 <img src='card.png' />

 [![GitHub Release][releases-shield]][releases]
 [![License][license-shield]](LICENSE.md)
 ![Project Maintenance][maintenance-shield]
 [![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg?style=for-the-badge)](https://github.com/custom-components/hacs)


 Enjoying this? Help me out with a :beers: or :coffee:!

 [![coffee](https://www.buymeacoffee.com/assets/img/custom_images/black_img.png)](https://www.buymeacoffee.com/whenitworks)


 ## Installation through [HACS](https://github.com/custom-components/hacs)

 Use [HACS](https://github.com/custom-components/hacs) to install the **Multiline Entity Card** plugin.

 ## Configuration

 ```yaml
 type: 'custom:multiline-entity-card'
 ```

 ### Example:
 ```yaml
 type: 'custom:multiline-entity-card'
 name: "Master Bedroom"
 entity: sensor.master_bedroom_reminders
 attribute: next_reminder
 show_icon: true
 image: /local/image/file.png
 show_name: true
 unit_of_measurement: prefix / suffix

 tap_action:
   action: more-info
   #Optional entity_id to get more-info on another entity. Default is curent entity
   data:
     target:
       entity_id: input_boolean.toggle


  tap_action:
   action: call-service
   service: input_boolean.toggle
   data: {}
   target:
     entity_id: input_boolean.test_toggle

  tap_action:
   action: navigate
   navigation_path: /config

 ```

 [commits-shield]: https://img.shields.io/github/commit-activity/y/jampez77/multiline-entity-card.svg?style=for-the-badge
 [commits]: https://github.com/jampez77/multiline-entity-card/commits/master
 [license-shield]: https://img.shields.io/github/license/jampez77/multiline-entity-card.svg?style=for-the-badge
 [maintenance-shield]: https://img.shields.io/badge/Maintainer-Jamie%20Nandhra--Pezone-blue
 [releases-shield]: https://img.shields.io/github/release/jampez77/multiline-entity-card.svg?style=for-the-badge
 [releases]: https://github.com/jampez77/multiline-entity-card/releases
