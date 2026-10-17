# Setup Alecto WS-5500 (weather station) with Ecowitt in Home Assistant

I searched for a solution to add my Alecto WS-5500 weather station to Home Assistant.
Then finally an AI helpt me with the right steps. For any one having difficulties setting up their Alecto Weatherstation try these steps. I think it will work from WS-2900 and upward.

The **Alecto WS-5500** uses hardware manufactured by *Fine Offset / Foshk*. Because of this, it natively supports the **Ecowitt protocol**. By using this method, your weather station display transmits sensor data directly to your Home Assistant server over your local Wi-Fi network—no internet cloud or external APIs required.

**Step 1: Add the Ecowitt Integration in Home Assistant**

1. In Home Assistant, navigate to **Settings** → **Devices & Services**.
2. In the bottom right corner, click **Add Integration** and search for **Ecowitt**.
3. Follow the on-screen instructions. Home Assistant will automatically generate a unique webhook URL for you (for example: `/api/webhook/a_long_string_of_characters`).
4. **Note down these details:** You will need your **Home Assistant local IP address**, the **port number** (usually `8123`), and the exact **webhook path**. (I copied the api to whatsapp, so I can copy and past it in WS View app. I left the port on: 80)

**Step 2: Configure the Alecto WS-5500 Display**

To route the data locally, you need to use the app that manages your weather station's Wi-Fi connection (typically the **WSView Plus** or **WS View** app).

1. Ensure your smartphone is connected to the **same 2.4 GHz Wi-Fi network** as your weather station.
2. Open the **WSView Plus** app and select your weather station from the device list.
3. Click the arrow in the top right corner (my version "Next") (or swipe through the settings pages) until you reach the **"Customized"** page.
4. Configure the following values exactly as shown:
   * **Enable:** Check the box / turn it on.
   * **Protocol / Protocol Type:** Select **Ecowitt**.
   * **Server IP / Host:** Enter the **local IP address** of your Home Assistant server (e.g., `192.168.1.50`).
   * **Path:** Paste the exact webhook path provided by Home Assistant (e.g., `/api/webhook/c631dcbc...`).
   * **Port:** Enter `8123` (or the custom port your Home Assistant instance runs on). (I left it at 80)
   * **Interval:** Set this to `60` seconds (or your preferred update frequency).
5. Click **Save** or **Success**.

Within a couple of minutes, all your 8-in-1 weather data (wind speed, rainfall, UV index, outdoor/indoor temperature, etc.) will start streaming live into Home Assistant!

*Note: Make sure your Alecto display is plugged into the wall outlet via its power adapter. If it runs purely on batteries, the Wi-Fi module will shut down to save power.*


All sensor data is displayed after a couple of minutes. Just missing the beautifull graphs from de app or webui from ecowitt.net.
