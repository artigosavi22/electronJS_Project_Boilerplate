
To create ElectronJS Application 

1. craete folder/directory 
        mkdir my-electron-app 
        cd my-electron-app


2.create Package.json file  
npm init -y     (create setup with default using -y flag)

3.update package.json file with 
     "main": "main.js", // replace with index.js with main.js

4.install electron 
npm install --save-dev electron

5.In the scripts field of your package.json config, add a start command like so:

{
  "scripts": {
    "start": "electron ."
  }
}

6.create main.js file in root directory

7.write createWindow() and loadFile with index.html code 

8. start application 
npm run start


=======================================================================
Activate Application

9. On Windows and Linux, exiting all windows generally quits an application entirely.

To implement this, listen for the app module's 'window-all-closed' event, and call app.quit() if the user is not on macOS (darwin).

app.on('window-all-closed', () => {
  if (process.platform !== 'darwin') app.quit()
})

==============================================================================

Production Ready Application

The fastest way to distribute your newly created app is using Electron Forge.

create Application which we can start app with double-click on app icon using below commands:

1.npm install --save-dev @electron-forge/cli
2.npx electron-forge import
3.npm run make 

