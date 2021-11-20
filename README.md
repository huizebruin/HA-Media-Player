# HA-Media-Player
| Repository Status | ESPHome S0tool discord Community |
| :--- | :--- |
| [![last commit time][github-last-commit]][github-master] [![GitHub Activity][commits-shield]][commits] | [![Discord][discord-shield]][discord]  
|  [![License][license-shield]](LICENSE) [![Forks][forks-shield]][forks-url] [![Stargazers][stars-shield]][stars-url] [![Issues][issues-shield]][issues-url] | [![Contributors][contributors-shield]][contributors-url] |

A variation on the [Radio Content player](https://www.digitaldomo.nl/homeassistant/dashboards/radio-content-player/).

![image](https://user-images.githubusercontent.com/62996429/142732925-0b519f5b-187c-4626-bc76-70cf3b1909be.png)

The big differance to the above script is that in this version each (radio)stream allong with all its variables are within 1 block.
This makes it easier to maintain because everything is placed inside 1 block instead of scatered thruout the script making it easy to find and change/adapt the variables. As a big plus you can now extend each block with extra metadata or even different type of media so you can now mix audio with video like youtube.
The installation stays the same as the original script.
Within the script you see 3 examples, one for a mediafile like a MP3, one for a radiostream and one for a youtube video.
The aim of this script is to work with google speakers and chromecast devices, but may possibly work on other mediaplayers like Echo dots etc. Just play around with the values for media_content_id and its metadata to fit your target device.

To add a file, stream or video just copy/paste the needed condition as much as you need. Just dont forget to add each conditions name into the input-select helper.

# Installation
- input_select helpers kan een keuze gemaakt worden voor het af te spelen station 
- met een input_select voor de speaker
- input_number voor het volume . 
- Vervolgens wordt een script gebruikt om de radio te spelen.
- input_number radio_volume dient via ‘Helpers’ aangemaakt te worden. Deze wordt later gebruikt om het volume voor de speaker te zetten. 
- De naam dient ‘radio_volume‘ te zijn. Gebruik de volgende gegeven
![image-3-1004x1024](https://user-images.githubusercontent.com/62996429/142732323-d1253973-1e65-440d-85ff-a7083e899d57.png)

- Add this to your configuration.yaml

```yaml
input_select: !include input-select.yaml
```
- Copy the contents of script.yaml into your script.
- Add the content of lovelace-card.yaml into a new card on your lovelace dashboard.
 ```yaml
type: entities
entities:
  - entity: input_select.radio_source
  - entity: input_select.radio_speaker
  - entity: input_number.radio_volume
  - entity: script.radio_content_player
  - entity: script.1636695244480
  - entity: media_player.huiskamer
state_color: true
show_header_toggle: true
```
- Check if the script entity matches your script


[commits-shield]: https://img.shields.io/github/commit-activity/m/huizebruin/HA-Media-Player.svg
[commits]: https://github.com/huizebruin/HA-Media-Playerl/commits/main
[github-last-commit]: https://img.shields.io/github/last-commit/huizebruin/HA-Media-Player.svg?style=plasticr
[github-master]: https://github.com/huizebruin/HA-Media-Player/commits/main
[license-shield]: https://img.shields.io/github/license/huizebruin/HA-Media-Player.svg
[discord-shield]: https://img.shields.io/discord/723629686093119650.svg?logo=discord&color=7289da
[discord]: https://discord.gg/bN8rC7gEng
[contributors-url]: https://github.com/huizebruin/HA-Media-Player/graphs/contributors
[contributors-shield]: https://img.shields.io/github/contributors/huizebruin/HA-Media-Player.svg
[forks-shield]: https://img.shields.io/github/forks/huizebruin/HA-Media-Player.svg
[forks-url]: https://github.com/huizebruin/HA-Media-Player/network/members
[stars-shield]: https://img.shields.io/github/stars/huizebruin/HA-Media-Player.svg
[stars-url]: https://github.com/huizebruin/HA-Media-Player/stargazers
[issues-shield]: https://img.shields.io/github/issues/huizebruin/HA-Media-Player.svg
[issues-url]: https://github.com/huizebruin/HA-Media-Player/issues
