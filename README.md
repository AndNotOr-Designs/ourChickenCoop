# ourChickenCoop

## Story
I'm lazy and don't want to walk out to the chicken coop every night and morning to open and close the door. In the past I had Arduino code running on the ESP32 that had web pages, but the webpages were slow and unreliable and I never really dug into the issue. Then we had a short in the coopMaster program that was causing the ESP32 to stop working. Enter Home Assistant and ESPHome! This repo moves all coop related items into 1 repo instead of 2 different repos. Eventually I'll put the coopMaster on an ESP dev board and get everything on the coop controllable in Apple HomeKit for the entire family.

# 1.01 - 2022-07-03
- coop door control deployed in ESP Home
    - Status LEDs
        - 4 LEDs on front of coop
            - Blue: ESP status pin
            - Red: door open
            - Yellow: door moving
            - Green: door closed
        - 2 LEDs in controller case
            - Blue: unused
            - Red: door stopped
    - Local physical buttons
        - Up/Stop/Down
            - one set outside, one set inside controller case
        - bump buttons
            - one for up, one for down
            - for if/when the door get's beyond the limit switches
    - reed sensors
        - one for door open
        - one for door closed
    - motor controller
        - motor is 24vdc motor
    - MQTT handled by Home Assistant on door status change