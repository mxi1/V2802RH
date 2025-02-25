# TP-Link Archer BE800 - Enabling 2.5G Mode

![Untitled](https://github.com/Anime4000/RTL960x/assets/1908715/80147e4c-99c4-4684-8303-adfcbfcf5771)

To enable 2.5G (HiSGMII PHY) on your TP-Link Archer BE800, follow these steps:

1. **Update Debug Firmware:**
   - Ensure you have the latest debug-enabled firmware installed. Refer to the firmware repository for the appropriate version.

2. **Reboot:**
   - Reboot your router to apply the updated firmware.

3. **Login to WebGUI:**
   - Access the router's Web Graphical User Interface (WebGUI) by navigating to `http://192.168.0.1`.

4. **Access Debug Page:**
   - Navigate to `http://192.168.0.1/webpages/debug.html` within the WebGUI.

5. **Enter Commands:**
   - Enter the following commands to enable 2.5G (HiSGMII PHY):
      ```plaintext
      combo_debug stop
      combo_debug set plus
      combo_debug ipg_set combo10g 1_192bit
      ```

   - To revert back to 1Gbps, use the following command:
      ```plaintext
      combo_debug ipg_set combo10g 1
      ```
6. **Wait and it will auto-negotiate**
![image](https://github.com/Anime4000/RTL960x/assets/1908715/0482c09d-56ae-4185-b094-b4f53896c610)


## Note:

   - The 2.5G mode activation is not persistent across power loss or router reboots. You will need to re-enter the commands after each occurrence.
   - Exercise caution when using debug features and refer to the router's documentation for additional guidance on the commands and their implications.
