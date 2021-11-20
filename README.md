# HA-Media-Player

A variation on the [Radio Content player](https://www.digitaldomo.nl/homeassistant/dashboards/radio-content-player/).

![lovelace](https://www.digitaldomo.nl/wp-content/uploads/2021/08/image-4-768x303.png)

The big differance to the above script is that in this version each (radio)stream allong with all its variables are within 1 block.
This makes it easier to maintain because everything is placed inside 1 block instead of scatered thruout the script making it easy to find and change/adapt the variables. As a big plus you can now extend each block with extra metadata or even different type of media so you can now mix audio with video like youtube.
The installation stays the same as the original script.
Within the script you see 3 examples, one for a mediafile like a MP3, one for a radiostream and one for a youtube video.
The aim of this script is to work with google speakers and chromecast devices, but may possibly work on other mediaplayers like Echo dots etc. Just play around with the values for media_content_id and its metadata to fit your target device.

To add a file, stream or video just copy/paste the needed condition as much as you need. Just dont forget to add each conditions name into the input-select helper.

# Installation
- input_select helpers kan een keuze gemaakt worden voor het af te spelen station 
- met een input_select voor de speaker
- input_number voor het volume. 
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
- Check if the script entity matches your script
![card](https://www.digitaldomo.nl/wp-content/uploads/2021/08/image-2-768x486.png)




