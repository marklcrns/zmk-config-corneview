Corne 42-keys ZMK Layout with nice!nano v2.0 and nice!view support.

## Switching Between Shield Display Designs

### nice-view-gem

[M165437/nice-view-gem](https://github.com/M165437/nice-view-gem)

1. From `zephyr/module.yml`, set `name: "zmk-shield-nice!view-gem"`
2. Update `config/west.yaml`
  ```yaml
    remotes:
      - name: zmkfirmware
        url-base: https://github.com/zmkfirmware
      - name: m165437 #new entry
        url-base: https://github.com/M165437 #new entry
    projects:
      - name: zmk
        remote: zmkfirmware
        revision: main
        import: app/west.yml
      - name: nice-view-gem #new entry
        remote: m165437 #new entry
        revision: main #new entry
  ```
3. Update `build.yaml`
  ```yaml
  include:
    - board: nice_nano_v2
      shield: corne_left nice_view_adapter nice_luffy_gear_five #update entry
    - board: nice_nano_v2
      shield: corne_right nice_view_adapter nice_luffy_gear_five #update entry
  ```

### nice-luffy-gear-five

[whoop-t/nice-luffy-gear-five](https://github.com/whoop-t/nice-luffy-gear-five)

1. From `zephyr/module.yml`, set `name: "zmk-shield-nice!view-luffy-gear-five"`
2. Update `config/west.yaml`
  ```yaml
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: whoop-t #new entry
      url-base: https://github.com/whoop-t #new entry
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: nice-luffy-gear-five #new entry
      remote: whoop-t #new entry
      revision: main #new entry
  ```
3. Update `build.yaml`
  ```yaml
  include:
    - board: nice_nano_v2
      shield: corne_left nice_view_adapter nice_luffy_gear_five #update entry
    - board: nice_nano_v2
      shield: corne_right nice_view_adapter nice_luffy_gear_five #update entry
  ```
