# MT4U Reaper Scripts

Cockos Reaper Scripts, developed to enhance the use of CSI (Control Surface Integrator)

Installation:
-------------
    Different folders contain the necessary scripts for each functionality and a CSI.txt file.
    Copy the scripts to your Reaper Scripts directory and check the CSI.txt file to find the
    changes needed in your CSI Zone files to make things work.

MT4U_FX_Rack (Virtual FX Rack for CSI)
--------------------------------------
---DEPRECATED---

MT4U_FX_Rack_Reaper7 (Virtual FX Rack for CSI - Reaper 7+)
--------------------------------------
    
    These set of scripts allow you to configure an FX Rack with your favourite plug-ins.

    It can be configured however you see fit, the example uses the F1-F8 buttons on an MCU 
    like this:
    
      F1 - Channel Strip 
      F2 - Compressor   
      F3 - Chorus   
      F4 - Stereo Imaging   
      F5 - Delay   
      F6 - Reverb   
      F7 - Flanger   
      F8 - Phaser  
      Shift+F1 - Tremolo  
      Shift+F2 - AutoPan  
      Shift+F3 - Distortion  
      Shift+F4 - Transient
      Shift+F5 - Filter
      Shift+F6 - Pitch
      Shift+F7 - Other
    
    and the MCU EQ Button:
    
      EQ - EQ
    
    There is a list of plug-ins that you can edit to enter your favourites for each category.
    
    If an FX of the category is found in the track's chain, the LED will turn on, and pressing 
    the button will bring the FX GUI on screen. With FocusedFXMapping enabled in CSI, your 
    surface will map the plugin. The Cancel button on the MCU will unmap and close the plug-in, 
    returning to the previous zone.

    Selecting a different track, the LEDs will show what plug-in categories are already in the 
    track's FX chain, giving you a swift overview.
    
    If the FX is not found, the first in the list will be added. Once added, the Alt modifier 
    will make the Prev/Next Channel MCU buttons go forward and backwards, replacing the current FX 
    with the next/prev on your list for each given category.
    
    If you press and hold the same button, a new instance of the default FX for that category
    will be added, regardless of the presence of another one in the chain.
    
    If, on the other hand, you are inside CSI's FX Menu, the plug-in will be added but not 
    displayed, since it's not necessary to take advantage of FocusedFXMapping. In this case 
    every effect in the FX chain can be replaced with the next/prev on your list using the 
    encoders.
    
    In the example configuration, the RecordArm button selects an FX. With the Alt modifier, 
    it can be moved up and down in the chain, while holding RecordArm will delete it.    
    ************************************************************************************************
    Reaper 7 implements FX Containers. This versions of the scripts allow you take advantage of that
    new feature. When using the MT4U_FX_MENU_MoveUp.eel (and MoveDown) scripts, the selected plug-in 
    will move crawling in and out of those containers whenever necessary.
    ************************************************************************************************    
    
    To install, add an MT4U folder inside Reaper's root scripts directory (<resource dir>/Scripts)
    and copy the MT4U_F_FUNCTIONS and MT4U_FX_MENU folders there, as well as the MT4U_FX_List.eel 
    and MT4U_FX_Navigator.eel files.
    Keeping this directory structure makes sure the Command IDs assigned to the actions will match
    the ones in the provided scrips and Zone File addendums.
    The MT4U_FX_List.eel file contains the list of plug-ins for each category and is shared
    by the scripts in both directories. It's been prepared for easy editing in case you don't feel 
    comfortable with EEL scripting, just open it and you will see.
    
    The CSI.txt file contains the necessary mappings required inside your CSI zone files to achieve 
    this behaviour in their default configuration.



MT4U_View (Show/Hide tracks with button feedback)
-------------------------------------------------
    These scripts are for setting a track's "category" and then use surface buttons to
    show/hide tracks depending on their category.

    You can configure your buttons however you want. The provided configuration works out of the
    box with the View buttons on an MCU and the "Option+" modifier:
        MIDI Tracks - Audio Tracks - Audio Inst. - Aux - Busses - User
   
    The buttons will show/hide tracks depending on their category.

    Holding the "Alt" modifier will provide feedback on the category associated with the 
    selected track, while pressing the View buttons will change the category for all selected 
    tracks to that associated with the button.


MT4U_Colours (Track Colouring)
------------
    A set of scripts to batch set the color for all selected tracks.
