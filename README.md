Link: https://shorturl.at/TX93n

# TEST NOTES

on Windows 11 24H2 Build 26100.4652 the conversion works fine except for the translucent taskbar. It's buggy.

on Windows 10 22h2 (last win10 version) it works fine

# .NET Framework 3.5

1) Install .NET 3.5 with `dotNetFx35setup.exe`

# Disable Windows Update

1) run `disable updates.bat`

I have provided a script to completely disable windows update service, since they break the theme applications such as WindowBlinds.

Don't disable win update BEFORE installing .NET or it will fail to download.


# Explorer Patcher - Pre-made config

1) Install `Explorer Patcher`

2) `Right click` on the task bar > `properties` then go to `Settings and unin...`

3) Click `Import Settings` and in `01.Explorer Patcher` folder, import the `.reg` file provided

4) Click on `Restart Explorer`

4) If it doesn't work properly, check the manual configuration below.


# Explorer Patcher - Taskbar

1) Install `Explorer Patcher`

2) `Right click` on the task bar > `properties`

3) `Taskbar` > `customize system icons` > disable:

	- action center (if not available ignore it )
	
4) Disable `show search button` and `show task view button`

5) set `combine taskbar icons on primary AND secondary taskbar` to `always combine`


# Explorer Patcher - System Tray

1) set `Skin taskbar and tray popup-menus` to false

2) set `center tray icon popup menus` to false

3) Set `network` to `windows 8 flyout`

4) set `Sound`, `Clock` and `Battery` to `Windows 7`


# Explorer Patcher - Start Menu

1) set `start menu style` to `Windows 10`

2) Set `position on screen` to `at screen edge`



# Explorer Patcher - File Explorer

1) set `Disable windows 11 context menu` to true

2) Set `Always use legacy file transfer dialog` to true

3) Set `use classic drives grouping in "This PC"` to True

4) Set `Control Interface` to `Windows 7 command bar`

5) Set `use immersive menus when displaying Windows 10 context menus` to false

6) set `disable modern search bar` to true

7) set `shrink address bar height` to true



# Explorer Patcher - Other

1) set `System/about page` to true

2) set `Programs and features` to true

3) set `Adjust date/time` to true

4) set `Customize notification icons` to true


Click `Restart file Explorer`



# Legacy Balloon Notifications

1) press start and type `regedit`

2) go to `HKEY_CURRENT_USER/SOFTWARE/Policies/Microsoft/Windows/Explorer`

3) Right click on the empty window and `Create DWORD`, call it `EnableLegacyBalloonNotifications`

4) Set the created key value to `1`


# Old New Explorer

1) Open `OldNewExplorerCfg.exe`

2) Click on `install`

3) Enable `Use classic drive grouping in This PC`

4) Enable `Use libraries; hide folders from This PC`

5) Enable `Use command bar instead of Ribbon`

6) Enable `Show details pane on the bottom`

7) Disable `Show status bar`


# Explorer settings

1) Open `This PC` and on the top left click `Organize > Settings`

2) Go into `View` tab and enable `Decrease space between items`


# Start Menu - Pre-made config

1) Copy `WIN7LIKE COMBO revE.skin7` into `C:\Program Files\Open-Shell\Skins`

2) Open `Open-Shell` and click on the tiny arrow near the `backup` button

3) Click `Load from XML File` and import the provided config called `Windows 7 Menu Settings.xml` in `03.Open-Shell`



# Start Menu - Manual Config

1) Install Open-Shell, leave everything as is in the installer

2) right click on the start button > `settings`

3) Select `windows 7 style`

4) in `04.Start Menu Skin` move `WIN7LIKE COMBO revE.skin7` to `C:\Program Files\Open-Shell\Skins`

5) Repeat `Step 2)` and go to `Skin` tab

6) Select as a skin `WIN7LIKE COMBO RevE`

7) Set `User Picture` as `Glared picture Frame`

8) Set` Glass Color Intensity` to `High. CSM Override color takbar match.`

9) Enable `7 Glass separators (more transparent)` and `7 Blue box shutdown update image`

10) Enable `Original Glass Selector`, `Reduced size of small selectors` and `Programs tree indent`

11) Go to `Customize start menu` and set `Recent items`, `Settings` and `Run` to `Don't display this item`

12) Set `Control Panel` to `Display as link`

13) Enable `Show all settings` in Open-Shell and go to `Main Menu` tab

14) Set `Show recent or frequent programs` to `Don't Show`

15) Set `Show start screen shortcut` to false`

16) Go to `menu look` tab

17) set `Main Menu Animation` to `no animation`


# Classic Explorer Bar

1) Search for `Internet Options` in the start menu

2) go to `Programs > Manage Add-ons`

3) Click on `Classic Bar Explorer` then click `Disable`


# Icon Pack

1) Open 7TSP GUI

2) Click `Add custom pack`

3) Select `Windows 7 icons.zip`, without extracting the archive

3a) If you don't see the archive to select, write manually the name of the archive in the `File name` bar of the window and press enter

4) Click `Start Patching` and agree to create a restore point. Wait until process is finished. When prompted to reboot, do so.
   Once the reboot is done, you will get a message which says `System has been patched`
   
5) If start menu icons don't update, open settings of `Open-Shell` and on the `Backup` button click the 
   tiny arrow, then select `Clear cached information`
   
6) To change file explorer icon on the task bar, search `File Explorer` on the start Menu
   
   right click on it and go to `Properties`, click `change icon` and then type `imageres.dll`
   
   then select the explorer icon, which is a `frontal folder with a blue-glassed square on the bottom of the folder`
   
   remove the current shortcut of file explorer into the task bar and create a new one, by clicking on the 
   file explorer application from the start menu and dragging it into the task bar
   

# WinFlip

1) Open WinFlip.exe, an icon will appear on the system tray icons on the bottom-right. If not visible it should be under the arrow icons.

2) Right click on it and go into `Options`

3) On `Quick Flip` Select the `ALT` key (i recommend keeping the `WIN` key so you can keep the classic `alt+tab` switch mechanism)
   

# WindowBlinds (Windows 10 works better here)

1) Install WindowBlinds and activate trial
   
   Use https://temp-mail.org/it/ to generate a temporary email.
   
2) In windowblinds click on the `Gear` icon on the top-right, then `install new`

   then select `BetterAero7X 2.7.wba` provided in `07.BetterAero7X 2.7` folder

3) Select `BetterAero7X` from the schemes, then apply. I recommend keeping it in light mode.


# Aero Cursor

I have provided a .inf file to automatically register the cursor in the system.

1) in `10.Aero Cursor` Open `cursor.inf` with a text editor
  
2) find the following section:

```
[Strings]
CURDIR="Path\To\10.Aero Cursor\cursor.inf"
```

modify the path string so that it points to the current location of your cursor.inf

3) Right click on cursor.inf > `install`

4) on start menu, search for `change mouse pointer appearance`

5) By default it will display the aero cursor, click on `Save As` and save the combination as `Aero`

   Select that combination and click `Apply` on bottom-left of the window.
   
 
 # Classic Task Manager
 
 1) Run `tm_cfg_win8-win10.exe` provided in `11.Classic Task Manager`
 
 
 # Classic Logon UI
 
 1) Install AuthUX provided in `09.Login UI (AuthUX)`
 
 2) If you disconnect your user you should now see the new logon UI.
 
 
 # Translucent Task Bar (Windows 10 works better here)
 
 1) Run `TranslucentTB.exe` provided in `08.Translucent Taskbar`
 
 2) It will minimize on system tray, bottom-right under the tiny arrow. Right click on the `TB icon > desktop > acrylic`


# Classic UAC (User Account Control) 

1) Get the files contained in `12.Classic UAC Prompt\Windows\System32\resources`

2) copy-paste them into `C:\Windows\System32\Resources`

3) Go into `12.Classic UAC Prompt\registry` and double click on `entries.reg`


# Winver Icons


# Boot animation

 
 # System Sounds TODO
