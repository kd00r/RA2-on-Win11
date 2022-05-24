# RA2-on-Win11
Instruction on how to runthe Origin version of  Red Alert 2 on Windows 11

#####################################################
#Downloading your bought copy of RA2+YR from Origin:#
#####################################################

1. Download RA2+YR from within the Origin client.
2. Download https://bibber.eu/downloads/cnc-ultimate-collection-launchers/
3. Unzip "cnc-ultimate-collection-launchers.zip"
4. Run and install "C&C Ultimate Collection Launchers Setup.exe"
5. Choose RA2+YR in the installer menu.
6. When it's done, copy the following folder to another location:

"C:\Program Files (x86)\Origin Games\Command and Conquer Red Alert II"

To, for example:
"C:\RA2"


#########################
#Installing the patches:#
#########################

In your copy of the above folder, "C:\RA2" in the example, do the follwing:

1. Download this:
https://github.com/CnCNet/cnc-ddraw

Direct link:
https://github.com/CnCNet/cnc-ddraw/releases/latest/download/cnc-ddraw.zip

2. Extract the zip file into the copied folder from above.
There should now be a new folder called "Shaders", and some new files in "C:\RA2":
cnc-ddraw config.exe
ddraw.dll
ddraw.ini


####################
#Configuring ddraw:#
####################

1. Run "C:\RA2\cnc-ddraw config.exe"

2. Go to Display Settings (should be opened by default) and:
Set Presentation to "Borderless"
Enable "Maintain aspect ratio"
Disable "VSync"
Enable "Adjust mouse sensitivity"
Enable "Lock cursor to window / screen"

3. Go to Advanced Settings:
Set Renderer to "OpenGL"
Set Shader to "Shaders\interpolation\bilinear.glsl"
Disable "Limit frame rate"
Disable "Enable windowboxing / integer scaling"
Enable "Show window borders in windowed mode"
Disable "Remember window position and size"

4. Go to Compability Settings:
Set "Limit game speed" to 60. i'll show how to specify it more fine grained later.
Disable all other (5) settings

5. Exit "cnc-ddraw config.exe"
6. Open "ddraw.ini" and:

Find the line "maxgameticks=60", should be on line 85.
Set it to your preferred speed. (I recommend somewhere around 100.)

7. Save and exit the "ddraw.ini" file.


#########################
#Configuring resolution:#
#########################

1. Open "RA2.INI"
2. Find the video section and change the defaults to your resolution like this (for 1080p in this example):

ScreenWidth=1920
ScreenHeight=1080

3. Repeat steps 1 and 2 for the file "RA2MD.INI"

4. Do not try to change the resolution from within the game.
Always change it from these two above configuration files.

Run "C:\RA2\RA2Launcher.exe"
Choose the game, RA2 or YR.
Enjoy.


###################################################################
#OPTIONAL: Setting up CNCNet for a revived multiplayer experience:#
###################################################################

1. Download CnCNet5_YR_Installer.exe from here:
https://cncnet.org/yuris-revenge#download

Direct link:
https://downloads.cncnet.org/CnCNet5_YR_Installer.exe

2. Make a copy of the "C:\RA2\" folder to, for instance, "C:\RA2_CNCNET\"

3. Run "CnCNet5_YR_Installer.exe"
4. MAKE SURE you choose "C:\RA2_CNCNET\" instead of the default:
"C:\Program Files (x86)\Origin Games\Command and Conquer Red Alert II"

5. MAKE SURE you do not choose "C:\RA2\" as well.

4. It will start automatically. Make sure to press Yes to edit the settings.
5. Exit the game.

6. Edit "C:\RA2_CNCNET\ddraw.ini".
7. On line 79 it should say the same value you chose before, eg:
maxgameticks=100

8. Save the file.

Run ""C:\RA2_CNCNET\CnCNetYRLauncher.exe" for the CNCNet multiplayer client.
Enjoy.


##########################################################
#OPTIONAL: Removing the Origin version to save HDD space:#
##########################################################
1. Open Origin.
2. Uninstall RA2.
