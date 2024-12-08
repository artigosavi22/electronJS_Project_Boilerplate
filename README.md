
# ElectronJS Application Setup and Distribution Guide

This guide explains how to create, activate, and make a production-ready ElectronJS application.

---
## **To Create an ElectronJS Application**

1. **Create a Folder/Directory**:
   ```bash
   mkdir my-electron-app
   cd my-electron-app

2. **create Package.json file**:
```bash
npm init -y     //(create setup with default using -y flag)

3.update package.json file with 
```bash
"main": "main.js", // replace with index.js with main.js

4.install electron
```bash
npm install --save-dev electron

5.In the scripts field of your package.json config, add a start command like so:
```bash
{
  "scripts": {
    "start": "electron ."
  }
}

6.create main.js file in root directory

7.write createWindow() and loadFile with index.html code 

8. start application
```bash
npm run start


=======================================================================
Activate Application

9. On Windows and Linux, exiting all windows generally quits an application entirely.

To implement this, listen for the app module's 'window-all-closed' event, and call app.quit() if the user is not on macOS (darwin).
 ```bash
app.on('window-all-closed', () => {
  if (process.platform !== 'darwin') app.quit()
})

==============================================================================

Production Ready Application

The fastest way to distribute your newly created app is using Electron Forge.

create Application which we can start app with double-click on app icon using below commands:

 ```bash
1.npm install --save-dev @electron-forge/cli
2.npx electron-forge import
3.npm run make 
