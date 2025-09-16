Control a light with the IKEA Rodret 2-button dimmer.<br />
    - Hold UP/DOWN = dim continuously (direction saved in input_select)<br />
    - Release = stop dimming<br />
    - Single click ON/OFF = toggle light<br />

⚠️ Requirements:<br />
    ZHA (no support for zigbee2mqtt at the moment or ever if you want it and it works then do a pull I'll add it)<br />
    This blueprint requires two helper entities to be created manually:

1. `input_boolean.rodret_dimming_active`
2. `input_select.rodret_hold_direction` with options "up" and "down"

Add this to your `configuration.yaml`:

    input_boolean:
      rodret_dimming_active:
        name: Rodret Dimming Active
        initial: false

    input_select:
      rodret_hold_direction:
        name: Rodret Hold Direction
        options:
          - "up"
          - "down"
        initial: "up"


# 🛠️ Import this Blueprint into Home Assistant

Click the button below to import this blueprint directly into your Home Assistant instance:

<a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fmoimeme81%2Frodret-blueprint%2Fmain%2Fblueprints%2Fautomation%2Frodret_dimmer.yaml" rel="nofollow"><img src="https://camo.githubusercontent.com/ae0e2f3004fb8aef54281402f3cb09eb052c308596ad223fb133236f9ae87348/68747470733a2f2f6d792e686f6d652d617373697374616e742e696f2f6261646765732f626c75657072696e745f696d706f72742e737667" alt="Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled." data-canonical-src="https://my.home-assistant.io/badges/blueprint_import.svg" style="max-width: 100%;"></a>

# **To do:**
<li>clean up</li>
<li>double tap</li>
<li>add support for zigbee2mqtt</li>
