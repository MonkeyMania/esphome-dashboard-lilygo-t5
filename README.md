# ESPHome based dashboard using Lilygo T5 4,7" e-ink display + ESP32

![Sample](/sample.png)

This is my hobby project to create an information-dense kitchen countertop dashboard for my Home Assistant based smart home.

My work was inspired by geekuillaume, Plawasan, and Tolnai.

Disclaimer: I am a hack. 🙂

## Device

I used a LILYGO T5-4.7 inch E-Paper ESP32 V3 Version 16MB Flash 8MB PSRAM WiFi/Bluetooth for arduino 18650 Battery Holder Version ordered from Amazon.

## Getting started

Steps I needed to get this project up and running on Windows:

- install ESPHome addon and integration to Home Assistant
- follow the [ESPHome CLI guide](https://esphome.io/guides/getting_started_command_line.html)
- add passwords to `secrets.yaml` (not pushed to this repo)

## Custom solutions behind

My dashboard code may not be reusable directly for anyone else, but it might give some ideas, or perhaps a motivation that it is not that difficult to just create something like this from scratch. The layout is fully custom and tailored for my own needs. I tried to produce just a little bit better code than a 5 year old would do, but I'm not that proud of it (could use a lot of refactoring). Oh boy, I haven't used C++ in ages... 🙂

Date related things and some other stuff are localized in a perhaps ugly way, since strftime can't do that.

Data sources used behind:

- HA date and time
- `sun` and `moon` HA sensors
- google calendar to get today's Sunrise and Sunset
- 433 MHz temperature+humidity sensors, Accuweather Atlas weather station, and another ESP32 monitoring garage doors
- Motion messages from Home Security Camera using MQTT (Blue Iris)
- Accuweather integration for forecasts

## Other resources

- [https://github.com/tiaanv/esphome-components]
- [https://github.com/Xinyuan-LilyGO/LilyGo-EPD47]
- [https://github.com/vroland/epdiy]
- [https://esphome.io/components/display/index.html]
- [https://www.reddit.com/r/homeassistant/comments/rm71z4/lilygo_t5_epaper_display_now_using_esphome/]
- [https://www.reddit.com/r/homeassistant/comments/rwwy6r/i_built_a_personal_dashboard_with_a_47_epaper/]
- [https://pictogrammers.github.io/@mdi/font/5.3.45/]

## License

Feel free to use any code from this repo, in any way you want. (WTFPL)
