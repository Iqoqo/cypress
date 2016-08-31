# Cypress Core Desktop Gui [![CircleCI](https://circleci.com/gh/cypress-io/cypress-core-desktop-gui.svg?style=svg)](https://circleci.com/gh/cypress-io/cypress-core-desktop-gui)

![core-desktop-gui](https://cloud.githubusercontent.com/assets/1271364/18134339/0fab0644-6f6c-11e6-8816-5d4528de6108.png)

The desktop GUI is the desktop application [installed](https://on.cypress.io/guides/installing-and-running#section-installing) to the user's OS using the `cypress install` command from the [Cypress CLI](https://github.com/cypress-io/cypress-cli) or through [direct download](http://download.cypress.io/desktop).

The desktop GUI has the following responsibilities:

- Allowing users to login through GitHub.
- Allowing users to add projects to be tested in Cypress.
- Displaying existing projects and allowing the removal of projects.
- Initializing the server to run on a specific project.
- Allowing users to choose a specific browser to run tests within.
- Displaying the resolved configuration of a running project.
- Displaying the list of tests of a running project.
- Initializing the run of a specific test file or all tests chosen by the user.
- Notifying users of updates to Cypress and initializing update process.

## Installing

```bash
npm install @cypress/core-desktop-gui
```

## Developing

To run the GUI in dev mode, you need to run the [Cypress App](https://github.com/cypress-io/cypress-app).

- Navigate to `cypress-app` and run the following commands:

```bash
npm i
npm start
```

The GUI should now be in your taskbar. Click in the taskbar to open it.

In your console, you will probably see the following error:

```bash
Error: connect ECONNREFUSED 127.0.0.1:1234
 > It looks like you're not running the local api server in development. This may cause problems running the GUI.
```

In order to access the api to do things like logging into the GUI, we need to run the [Cypress API](https://github.com/cypress-io/cypress-api). Navigate to `cypress-api` and run the following commands:

```bash
npm i
npm start
```

If you get any errors doing the above commands, go through the [install instructions](https://github.com/cypress-io/cypress-api) of the cypress-api app.

## Testing

```bash
npm test
```

## Debugging

If you want to see the `ipc` events which are pending from Cypress tests:

- Switch to 'Your App' frame
- App.ipc() <-- returns you object with pending events

## License
LGPL

## Changelog

#### 0.3.4 - *(08/31/16)*
- fix github focus button

#### 0.3.3 - *(08/30/16)*
- added applying updates view

#### 0.3.2 - *(08/30/16)*
- fixes dist dir and updates.html

#### 0.3.1 - *(08/30/16)*
- fix for incorrect references in index.html

#### 0.3.0 - *(08/30/16)*
- new UI, migrated to react

#### 0.2.2
- renamed Login -> Log In

#### 0.2.1
- internal updates to cypress.json settings change notification

#### 0.2.0
- display list of launchable browsers
- handle error when no browsers available

#### 0.1.5
- updated node version to 5.10.0

#### 0.1.4
- added link to gitter chat in options popup

#### 0.1.3
- added specific error msg and link to docs on unauthed login

#### 0.1.2
- updated license

#### 0.1.1
- renamed to cypress-core-desktop-gui
- removed dead code

#### 0.1.0
- initial release