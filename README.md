# Homeassistant Lovelace Comfoair card

Use [https://github.com/svenar-iot/esphome-comfoair](https://github.com/svenar-iot/esphome-comfoair) to connect your ComfoAir to Homeassistant and then use this lovelace card to visualize your data!

![Image](https://raw.githubusercontent.com/wichers/lovelace-comfoair/master/result.png)

[![Install with HACS](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=wichers&repository=lovelace-comfoair)

# Manual installation

* Clone this repo into your `www` folder inside your configuration. So it will be: `config_folder/www/lovelace-comfoair`.
* Edit your lovelace-ui.yaml or use the flat configuration mode in lovelace and add to the top:
```
resources:
  - type: module
    url: /local/lovelace-comfoair/comfoair-card.js
```
* Add a card with `type: 'custom:comfoair-card'` and `entity: 'climate.put-your-comfoair-name-here'` to your UI.
* Restart home assistant
* ???
* Profit!

# HACS installation

If you prefer to manage the card via HACS:

1. Open HACS in Home Assistant and add `https://github.com/svenar-iot/lovelace-comfoair` as a **Custom Repository** in the **Dashboard** category.
2. Find **Comfoair ventilation lovelace component** in the list of custom repositories and install it.
3. Make sure the following resource is added to your configuration:
   ```yaml
   url: /hacsfiles/lovelace-comfoair/comfoair-card.js
   type: module
   ```
4. Use the card with `type: 'custom:comfoair-card'` and your climate entity as shown above.

