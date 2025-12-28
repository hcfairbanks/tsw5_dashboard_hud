# tsw5_dashboard
A dashboard for TSW5. Written in JS. Clones the games HUD. Runs a webserver
for access accross your local network (for things like cellphones or
tablets). If you have three monitors you can run this and use your phone for
a HUD and place it under the center monitor. 

Setup and Installation

// In a Windows Powershell

// Set permissions so you can install node packages in windows powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

// Reversing the permissions if and when you need to
Set-ExecutionPolicy -ExecutionPolicy Restricted -Scope CurrentUser

// Get a list of permissions
Get-ExecutionPolicy -List

// install nvm-setup.exe from here
https://github.com/coreybutler/nvm-windows/releases

// Install node 24.12.0
nvm --version
nvm install 24.12.0
nvm use 24.12.0
node -v

// Look for your computers internal network IP
// It will look something like this 192.168.12.88
// It will be listed next to "IPv4 Address" after running the command "ipconfig"
ipconfig

// Open the program folder up in VS code or another IDE 
// In the file "server.js" you can comment out lines 8 & 9 and run line 7 if your 
// API keys are stored in a differnt place other than the steam default
const apiKeyPath = 'C:\\Users\\<YOUR_USER_HERE>\\Documents\\My Games\\TrainSimWorld5\\Saved\\Config\\CommAPIKey.txt';

// In the server file again you can specify if you want the data in KM or Miles by setting the "useMiles".
// This will display all data in the relevant Miles/Feet or KM/Meters
const useMiles = true;

// the root of the folder you can start the server by running this command on a terminal
node ./server.js

// to see the running application open a browser and enter this URL 
localhost:3000

// to see the application running from your phone or other networked device type
// type your computers network ip address with the port number 3000
// it should look something like this
192.168.12.88:3000


Future Goals
- Have all features of TSW HUD in the application
- Create a HUD for steam engines
- Create specific pages dedicated to different gui interfaces of specific trains
- Create an .exe file to run the program


Missing Features
- Reverser
   + Off
   + Neutral
   + Forward 
   + Reverse
-Brake Systems
- Power Indicator
- LZB Distance To Speed
- Cruise Speed
- Accelerometer
- In-Cab Signaling / LBZ Speed Limit
- Train Door Status
- Safety Systems
- Current Time
- Time expected
- Load passengers progress bar
- Stop at location indicator with distance

