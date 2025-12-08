This "ERR_GFX_STATE" error in Red Dead Redemption 2 is extremely common and is usually caused by corrupted cache files related to the graphics pipeline.

Here is a step-by-step guide to fix it, ordered from the most effective (and easiest) to the more advanced solutions.
Fix 1: The Pipeline Cache Fix (Most Likely to Work)

This is the standard fix for this specific error. You need to delete some temporary files that the game rebuilds automatically.

    Close the game and the Rockstar Launcher completely.

    Open File Explorer and go to Documents > Rockstar Games > Red Dead Redemption 2 > Settings.

    In this folder, look for files that start with sga_ (e.g., sga_vulkan_final_init.vkPipelineCachewindows).

    Delete all files starting with sga_. (Do not delete the other files like system.xml).

    Restart the game.

Fix 2: Add a Launch Argument

To stop the error from coming back, you can force the game to ignore the pipeline cache so it doesn't get corrupted again.

For Steam:

    Right-click RDR2 in your Library and select Properties.

    In the General tab, look for "Launch Options".

    Type this exactly: -ignorepipelinecache

    Close the window and launch the game.

For Rockstar Launcher:

    Open the launcher and go to Settings.

    Select RDR2 under "My installed games".

    Scroll down to "Launch arguments" and type: -ignorepipelinecache

For Epic Games:

    Go to Settings in the Epic Launcher.

    Scroll down to Red Dead Redemption 2 and expand it.

    Check "Additional Command Line Arguments" and type: -ignorepipelinecache

Fix 3: Switch Graphics API (Vulkan vs DX12)

Sometimes the error is specific to the Vulkan API (which is the default). Switching to DirectX 12 often stabilizes it.

    Go to Documents > Rockstar Games > Red Dead Redemption 2 > Settings.

    Right-click system.xml and open it with Notepad.

    Find the line that says <API>kSettingAPI_Vulkan</API>.

    Change it to: <API>kSettingAPI_DX12</API>

    Save the file and launch the game.

Summary Checklist

    [ ] Deleted sga_ files in Documents.

    [ ] Added -ignorepipelinecache to launch options.

    [ ] (If needed) Switched system.xml to DX12.