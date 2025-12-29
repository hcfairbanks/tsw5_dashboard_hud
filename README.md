# tsw5_dashboard
A dashboard for TSW5 ( maybe TSW6 too ). Written in JS. Clones the games HUD.
Runs a webserver for access across your local network (for things like
cellphones or tablets). If you have three monitors you can run this and use your
phone for a HUD and place it under the center monitor. 
This is the first draft and it's still in a very rough state.

For the latest version, a public repo is available here
https://github.com/hcfairbanks/tsw5_dashboard_hud


Setup and Installation

TSW5 needs to run with HTTP API Enabled
Here are the instructions from the Dovetail doccumentation 

To enable the External Interface API, the title must be launched with the command line
parameter “-HTTPAPI”. This can be done within Steam as follows.
Find the title in your Steam Library, right click on it and select Properties.
From the dialog that opens, select the General tab (which should be the default) and
observe the “LAUNCH OPTIONS” section. Add the parameter there, as shown:
With this in place, load the game up to the main menu once and then exit. This will
ensure that the communication API key is generated.

The official API PDF instructions are available 
https://forums.dovetailgames.com/threads/train-sim-world-api-support.94488/


In a Windows Powershell

Set permissions so you can install node packages in windows powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

Reversing the permissions if and when you need to
Set-ExecutionPolicy -ExecutionPolicy Restricted -Scope CurrentUser

Get a list of permissions
Get-ExecutionPolicy -List

Install nvm-setup.exe from here

https://github.com/coreybutler/nvm-windows/releases

Install node 24.12.0
nvm --version
nvm install 24.12.0
nvm use 24.12.0

To see if it has worked run
node -v

You should see
v24.12.0

Open the program folder up in VS code or another IDE
In the file "server.js" you can comment out lines 8 & 9 and run line 7 if your
API keys are stored in a differnt place other than the steam default
const apiKeyPath = 'C:\\Users\\<YOUR_USER_HERE>\\Documents\\My Games\\TrainSimWorld5\\Saved\\Config\\CommAPIKey.txt';

In the "server.js" file you can specify if you want the data in KM or Miles by setting the "useMiles".
This will display all data in the relevant Miles/Feet or KM/Meters
const useMiles = true;

The root of the folder you can start the server by running this command on a terminal
node ./server.js

Once you start the sever you will get a message letting you know where you can see the application 

All subscriptions created
Server running locally at http://localhost:3000
Server accessible on local network at http://192.168.2.85:3000

To see the application running from your phone or other networked device type
Use the second address listed
Server accessible on local network at http://192.168.2.85:3000

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

