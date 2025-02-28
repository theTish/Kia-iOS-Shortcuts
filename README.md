# Kia-iOS-Shortcuts

A Python Flask API for creating iOS shortcuts that execute commands, such as Lock/Unlock, Start/Stop Climate.

---
## Intro

This uses the Kia API written in Python. It was developed specifically for iOS shortcuts, though it may also work on Android OS. This allows for shortcuts to:

- Lock Vehicle  
- Unlock Vehicle  
- Start Climate  
- Stop Climate  

This uses the following Python package: [Hyundai Kia Connect API](https://github.com/Hyundai-Kia-Connect/hyundai_kia_connect_api).

---

## Installation

You will need to add Environment Variables for the items below in order for the `# Initialize Vehicle Manager` to work. These include your Kia account:

- **Username**  
- **Password**  
- **PIN**  

Additionally, there is a placeholder for a Secret Key for extra security. You will need to define a secret key in the placeholder and in the Environment Variables. 


The API requires your **region**. By default, it is set to the USA. If you are outside the US, update it using the following region codes:

REGIONS = {
    1: REGION_EUROPE,
    2: REGION_CANADA,
    3: REGION_USA,
    4: REGION_CHINA,
    5: REGION_AUSTRALIA }

If you have multiple Kia vehicles, the script includes logic to search for all vehicles associated with your account and match them by vehicle ID. If you have multiple vehicles, run the code without the direct lookup first to identify your vehicle ID, then update the script accordingly. If you only have one vehicle, you can remove the direct lookup.

The climate command requires a Climate Request Option. By default, it is set to 72°F for 10 minutes, but you can modify this based on your preferences.

---

## Notes

There are additional commands available through the API, but this implementation currently supports only the four commands listed above.
