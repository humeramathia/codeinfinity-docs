# A. Access the Apple Developer Account
First, ensure you have access to the Apple Developer account. This is a paid subscription service provided by Apple, required for app deployment on iOS devices.

# B. Create an App ID
Before you can create certificates and provisioning profiles, you need to define your app with an App ID in the Apple Developer portal.

- Log into the Apple Developer Portal
- Navigate to "Certificates, Identifiers & Profiles".
- Go to Identifiers > + (plus icon).
- Select App IDs and click Continue.
## Define your App ID:
- **Name:** Enter a unique name for your app.
- **Bundle ID:** This is a unique identifier, usually in reverse domain name format (e.g., com.example.myapp).
-Select capabilities if your app uses services like Push Notifications, Wallet, etc.

## C. Create Provisioning Profiles
Proceed to create provisioning profiles.

- Navigate to "Certificates, Identifiers & Profiles".
- Select Profiles > + (plus icon).
- Choose the profile type:
- iOS App Development (for testing on registered devices).
- App Store (for distribution through TestFlight and the App Store).
- Select the App ID you created for your app.
- Choose the certificates for signing the app.
- Select devices for development profiles (if applicable).
- Provide a name for the profile and generate it.
- Download and install the profile by double-clicking on it and transfer the file to your windows.

# D. Generate Certificates
You'll need to create both development and distribution certificates. Distribution certificates are necessary for uploading your app to TestFlight.

- Navigate to Certificates section in the Apple Developer portal.
- Add a new certificate by clicking the + icon.
## Choose the appropriate certificate type:
- iOS App Development (for development purposes).
- iOS Distribution (App Store and Ad Hoc) (for distributing your app via TestFlight and the App Store).

## Follow the instructions to generate a Certificate Signing Request (CSR):
- Open Keychain Access on your Mac.
- Select Keychain Access > Certificate Assistant > Request a Certificate from a Certificate Authority.
- Enter your email address, choose the 'Saved to disk' option, and follow prompts to generate the CSR.
- Upload the CSR file on the Apple Developer website and download your certificate.
- Install the certificate by double-clicking the downloaded certificate file, which will add it to your Keychain.

## Ensure RAD Studio on Windows Can Use the Certificate
Since RAD Studio is running on your Windows machine, you'll need to ensure it can utilize the certificate for signing your app during the build process. The PA Server facilitates this connection. Here’s how to ensure everything is correctly set up:

# Export the Private Key and Certificate from Mac:

- Open Keychain Access.
- Find the certificate you installed (under "login").
- Right-click on the certificate and select "Export".
- Save it as a .p12 file, setting a password when prompted.
- 
# Transfer the .p12 File to Your Windows Machine:
- Use a secure method to transfer the file (like a USB drive or a secure network transfer).
- Import and Install the .p12 File on Windows
- Locate the .p12 File on Your Windows Machine: After transferring the file, navigate to the location where you saved it.

# Install the .p12 File:

- Double-click the .p12 file to start the import wizard. The Certificate Import Wizard in Windows will guide you through the process.
- Select the store location as “Current User” and click "Next".
- Browse and select the .p12 file you transferred, then click "Next".
- Enter the password you set during the export process from your Mac.
- Select the option to “Mark this key as exportable”. This ensures that you can back up or transport your keys and certificates at a later time if needed.
- Choose to "Automatically select the certificate store based on the type of certificate" or manually select the “Personal” store to place the certificate.
- Complete the wizard by clicking "Finish".