# Connecting RAD Studio

## A) Set Up the Connection in RAD Studio

To connect RAD Studio on your Windows machine to the PA Server running on your Mac, follow these steps:

**Open RAD Studio:**
Launch the RAD Studio development environment on your Windows machine.

**Access the Connection Profile Manager:**
Navigate through the menu: `Tools > Options > Deployment > Connection Profile Manager`.

**Create a New Profile:**

  - **Profile Name:** Provide a descriptive name for the connection profile, such as "iOS Deployment".
  - **Platform:** Choose `64-bit iOS` from the platform options.
  - **PAServer Hostname:** Input the IP address of your Mac, found under `System Settings > Wi-Fi > Details > IP address`.
  - **PAServer Port:** Type the PA Server port number, typically `64211`.
  - **Password:** Use the password established during the PA Server setup or leave blank.
## B) Test the Connection
1.	**Test:** Click the Test Connection button to verify that RAD Studio can communicate with the PA Server on your Mac. If the test fails, ensure your network settings and firewall are configured correctly.
