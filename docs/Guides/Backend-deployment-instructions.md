# Backend deployment instructions

This guide provides detailed steps on how to deploy the backend of the project.

## Prerequisites

Ensure you have the following:

- Access to the project repository
- Access to the google cloud platform service account key (please contact `Bieber.capstone@gmail.com` for access with heading (service key))
- Necessary permissions to modify files and execute scripts

## Steps
1. install the google cloud sdk by following the instructions [here](https://dl.google.com/dl/cloudsdk/channels/rapid/GoogleCloudSDKInstaller.exe)
   
2. make sure the sdk is set as a path environment variable, add the path `C:\Users\<Username>\AppData\Local\Google\Cloud SDK\google-cloud-sdk\bin`

3. **Update Database Credentials**: Open the `application.properties` file located:
```bash
    Backend/src/main/resources/application.properties
```
4.  Replace the existing database credentials with the correct ones.

5. **Copy JSON File**: Locate `events-system-back-329277c97613.json` file. Copy this file into the Backend directory of your project.

6. **Switch File Mode**: The `backend-deploy.bash` file needs to be in LF mode. If it's in CRLF mode, please switch it using your IDE. the button to change end of line sequence should be located at the bottom right of the IDE. eg.
    ![Alt text](/img/lfmode-intellij.png)

7. **Run Bash Script**: Execute the bash script by typing `bash backend-deploy.bash` in your terminal. This script sets up the necessary environment for the backend.

8. **Switch Project**: The terminal will ask if you want to switch the current project to "events-system-back". Type `Y` and press enter.

9.  **Remove Credentials**: Before making a commit, ensure you remove the database credentials from the `application.properties` file. It's crucial to not commit sensitive information to your repository.

## Note

If you encounter any issues during the process, please contact the project administrator ( `Bieber.capstone@gmail.com`).