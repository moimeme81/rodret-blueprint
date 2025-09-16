Control a light with the IKEA Rodret 2-button dimmer.<br />
    - Hold UP/DOWN = dim continuously (direction saved in input_select)<br />
    - Release = stop dimming<br />
    - Single click ON/OFF = toggle light<br />

⚠️ Requirements:
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
