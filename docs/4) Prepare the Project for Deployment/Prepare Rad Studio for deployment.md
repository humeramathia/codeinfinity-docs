# Prepare the Project for Deployment
We will set up Rad Studio to start the deployment process to TestFlight
## Setup 
- Navigate to project -> Options -> Version Info
- Under CFBundleIdentifier you will add your bundle id (e.g., com.example.myapp)
- Set a versioning of your app at CFBundleVersion (e.g., 0.0.1)
## Navigate to Provisioning Settings:
- Go to Project -> Options. This will open the Project Options dialog.
- From the left pane, expand the Building node, then select Provisioning. This section is specifically used for configuring settings related to the deployment and provisioning of your iOS applications.

## B. Configuring the Provisioning Profile
## Select the Target:

- Ensure that the target platform set at the top of the Project Options dialog is iOS, as you are configuring provisioning for an iOS app.

## Load Provisioning Profiles
- RAD Studio should automatically detect and list the provisioning profiles available on your system if the PA Server is properly configured and connected.

## Choose the Correct Provisioning Profile:

From the list of provisioning profiles, select the one that corresponds to your app. The provisioning profiles are typically named based on the app identifier and the type of profile (development or distribution).
# Make sure to choose the correct profile type:
- Development Provisioning Profile for debugging and development.
- Distribution Provisioning Profile for releasing to TestFlight or the App Store.