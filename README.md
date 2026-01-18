# Quixel-Bridge ⇢ Blender
An adjusted version of the Bridge addon to receive all assets in Blender without manually exporting and importing.
The original Addon can be found [here](https://quixel.com/plugins).

# Available Versions

[3.9.0 for Blender 5.0](https://github.com/EMBMUSICOFFICIAL/QUIXEL-BRIDGE-BLENDER-unofficial/releases/tag/v3.9.0)

[3.8.0 for Blender 4.0](https://github.com/EMBMUSICOFFICIAL/QUIXEL-BRIDGE-BLENDER-unofficial/releases/tag/v3.8.0)

[3.7.0 for Blender 3.1](https://github.com/EMBMUSICOFFICIAL/QUIXEL-BRIDGE-BLENDER-unofficial/releases/tag/v3.7.0)

[3.5.2 for Blender 2.8](https://github.com/EMBMUSICOFFICIAL/QUIXEL-BRIDGE-BLENDER-unofficial/releases/tag/v3.5.2)

# Installation
Plugin installation is part of Bridge Export Settings. These settings are global and once set up, will not need to be changed too often.  
You can install the plugin using any one of these methods:
 1. You can set up the plugin when you launch Bridge after installing it for the first time on your machine.
 2. Through Export Settings.
 3. Through the Manage Plugins option in the Edit menu.

Note: Make sure Blender is closed before installing.

## Installation during initial setup
1. When you launch Bridge after installing it for the first time on your machine, you will see initial setup options. Click the Library Path to choose the folder on disk where you would like your asset library to be.

      <sub>_The Library Path is important because this is where Bridge will store your assets and plugins. If you don’t already have a folder for this purpose, Bridge will create it for you._ </sub> 

2. Click Next.
3. From the Export Target drop-down, select Blender.
4. Click Download Plugin to begin downloading the plugin.
5. Once the download is done you’ll see a confirmation message in Bridge.
6. Click Install Plugin to install the plugin in Blender.
7. Once the plugin is installed you should see the Installed status on the pop-up. Click Done to complete the set up.
8. Start up Blender and the plugin will automatically start up as well. 

## Installation via Export Settings
1. To access the settings, click the gear icon on the bottom left corner of the asset’s right panel or go to Edit > Export Settings.

<img width="2500" height="1496" alt="image" src="https://github.com/user-attachments/assets/617cdf51-a73e-40ea-9947-df8c4c9efb62" />

2. Click Export Settings in the pop-up menu to view all the export options. You can tweak your settings, like texture format, LODs, mesh format (FBX or OBJ), etc.

<img width="1920" height="997" alt="image" src="https://github.com/user-attachments/assets/0cecbc1e-3806-4de0-b6df-98333451eb75" />

## Exporting Assets
1. In Bridge, go to the Local filter in the left panel to export a downloaded asset. Make sure Blender is running.
2. Click the Quick Export icon <img width="16" height="19" alt="image" src="https://github.com/user-attachments/assets/1448b041-8628-4243-87a8-72b0d7059e7e" /> or hit the Export button.


As soon as you click on Export in Bridge your asset should pop up in your Blender scene.

 <img width="656" height="510" alt="image" src="https://github.com/user-attachments/assets/2d44b213-946a-4446-b522-b82d5ca49b59" />


## Exporting Alembics to Blender
In order to export Alembic files to Blender you will need to do an additional step after exporting that Alembic asset from Bridge.

This is due to the way Blender’s Python API works.

After exporting an alembic asset from Bridge simply follow this step:

1. Go to “File > Import > Megascan: Import Alembic Files” to start the plugin.


The plugin will import the alembic files that were exported from Bridge as well as assign the right material to it.

## Custom Installation
If the current installation process in Bridge isn’t suitable for your pipeline, you can download the plugin manually as follows.

1. Download the plugin with your desired Version.

2. Extract the plugin from the .zip file.
3. Depending on your OS, go to the “startup” folder using the paths given below
 - Windows: C:\Users\username\AppData\Roaming\Blender Foundation\Blender\X.X.X\scripts\startup\
 - Mac OS: /Users/username/Library/Application Support/Blender/X.X.X/scripts/startup/
 - Linux: /home/username/.config/blender/X.X.X/scripts/startup/
   
5. Copy the MSPlugin folder in the startup folder.
 
      Now the Megascans plugin will startup when you launch Blender.

6. Open Bridge, and in the Local filter click on the asset you want to export.

<img width="1920" height="999" alt="image" src="https://github.com/user-attachments/assets/59ba5786-845f-41c5-bd82-b009bca96e1c" />


6. Go to the asset’s Export Settings, select Custom Socket Export from the Export Target drop-down.
7. Set the Socket Port field to 28888.
8. Go back to the asset details panel, click Export and your asset should appear in Blender.

## Uninstallation
1. Close Blender if running.
2. Depending on your OS, go to the “startup” folder using the paths given below:
- Windows: C:\Users\username\AppData\Roaming\Blender Foundation\Blender\X.X.X\scripts\startup\
- Mac OS: /Users/username/Library/Application Support/Blender/X.X.X/scripts/startup/
- Linux: /home/username/.config/blender/X.X.X/scripts/startup/
3. Delete the MSPlugin folder.
