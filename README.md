# EV Charger Dynamic Current Control

A Home Assistant blueprint that dynamically adjusts EV charger current to keep your grid power close to a target value.

It works by stepping through predefined current levels (e.g. 6, 8, 10, 13, 16 A) based on real-time power usage.

### Features
- Supports custom current steps (comma-separated list)
- Works with any charger exposing a number entity
- Uses a power meter sensor for real-time grid power
- Configurable target power and tolerance
- Automatically increases or decreases charging current
- Simple and lightweight (runs every minute)


### How It Works
1. The automation runs every minute
2. It reads:
- Current charger amperage
- Net grid power from your meter
3. It compares grid power to the target:
- Below target → increase charging current
- Above target → decrease charging current
- Within tolerance → do nothing
4. The current is adjusted to the next valid step


<a href="https://buymeacoffee.com/nejcvidrihm" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
