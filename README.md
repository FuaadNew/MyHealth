# MyHealth

## Table of Contents
- [Introduction](#introduction)
- [Technical Specifications](#technical-specifications)
- [Deployment](#deployment)
- [Main Features](#main-features)
- [Walkthrough](#walkthrough)
- [Future Enhancements](#future-enhancements)
- [Appendix](#appendix)

## Introduction
MyHealth is a web application designed to help users reach their fitness goals. While its full functionalities were not fully realized, the application provides seamless navigation, functional login and logout capabilities, and an attractive UI.

## Technical Specifications
MyHealth is an Express web application that needs to be hosted on your localhost. The hardware requirements are minimal, typically needing a modern processor, a few gigabytes of RAM, and sufficient storage space. Most node modules are included, so additional dependencies are not required.

## Deployment

### Follow these instructions to run MyHealth:

1. **Download MongoDB**

   - Visit the MongoDB website and download the installer for your device's specifications.
   - Run the installer and follow the instructions provided.

2. **Make MongoDB an Environment Variable**

   **Windows:**
   - After installing MongoDB, add its bin directory to the system’s PATH environment variable:
     - Right-click on “This PC” or “My Computer” and select “Properties”.
     - In the System Properties window, click on “Advanced system settings”.
     - Click on “Environment Variables…” and under “System variables”, find the “Path” variable, select it, then click on “Edit…”.
     - In the Edit environment variable window, click on “New” and add the path to the bin directory of your MongoDB installation (e.g., `C:\Program Files\MongoDB\Server\4.4\bin`).
     - Click ‘OK’ on all windows to save changes.

   **Mac:**
   - Open Terminal.
   - Use a text editor (like nano or vi) to edit the `.bash_profile` file in your home directory: `nano ~/.bash_profile`.
   - Add the following line: `export PATH="/usr/local/opt/mongodb/bin:$PATH"`.
   - Save the changes and exit the text editor.
   - In Terminal, run the command `source ~/.bash_profile` to apply the changes.

3. **Download MyHealth Repository**
   - Download the MyHealth repository and keep track of its location.

4. **Download Node.js**
   - Visit [nodejs.org](https://nodejs.org/en/download/) and choose the version compatible with your machine.
   - Follow the installer instructions to install Node.js.

5. **Make Node.js an Environment Variable**

   **Windows:**
   - After installing Node.js, add its bin directory to the system’s PATH environment variable:
     - Follow the same steps as MongoDB, replacing the path with the bin directory of your Node.js installation (e.g., `C:\Program Files\nodejs\bin`).

   **Mac:**
   - Open Terminal.
   - Use a text editor to edit the `.bash_profile` file: `nano ~/.bash_profile`.
   - Add the following line: `export PATH="/usr/local/opt/nodejs/bin:$PATH"`.
   - Save the changes and exit the text editor.
   - In Terminal, run the command `source ~/.bash_profile` to apply the changes.

6. **Run the App**
   - Open a terminal window and change directories to where you downloaded MyHealth.
   - Run the following commands:
     ```
     mongod
     node app.js
     ```

## Main Features
- **Account Functionality:**
  - Users can log into MyHealth with a specified username and password or create a new account.
  - The home page can only be accessed after user authentication.

- **Interactive UI:**
  - The home page features a 'burger' UI icon for navigation.
  - A CSS-styled hamburger menu on every static HTML page provides links to other static pages.
  - Popups remind users to log their activities or food intake.

- **Health Goals:**
  - The MyHealthTasks page allows users to add goals to their account.
  - Goals are stored during the session but are cleared upon logout.

- **Nutritional and Exercise Information Logging:**
  - The MyHealthTracking page uses the CalorieNinjas API to provide nutritional information.
  - Users can manually log food and exercise information, which is cleared upon page refresh.
  - The MyHealth Achievements page lists some stock achievements.

## Walkthrough
1. Access the Login page and click on the signup button.
2. Create a unique username and password on the signup page.
3. Sign in on the Login page with your new account.
4. On the home page, click on the hamburger icon to open the navigation menu.
5. Navigate to MyHealthTracking to log your food and exercise for the day.
6. Use the non-manual food field to get nutritional information.
7. Add a new user goal on the MyHealthTasks page.
8. Return to the home page and log out using the navigation menu.

## Future Enhancements
- Persist user goals and achievements beyond sessions.
- Improve data storage to allow users to log out and log in without losing previously set goals or achievements.
- Continue to check for updates as new features are added.

