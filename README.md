# MT4U Reaper Scripts

Cockos Reaper Scripts, developed to enhance the use of CSI (Control Surface Integrator)

Installation:
-------------
    Different folders contain the necessary scripts for each functionality and a CSI.txt file.
    Copy the scripts to your Reaper Scripts directory and check the CSI.txt file to find the
    changes needed in your CSI Zone files to make things work.

MT4U_View (Show/Hide tracks with button feedback)
-------------------------------------------------
    These scripts are for setting a track's "category" and then use surface buttons to
    show/hide tracks depending on their category.

    You can configure your buttons however you want. The provided configuration works out of the
    box with the View buttons on an MCU and the "Option+" modifier:
        MIDI Tracks - Audio Tracks - Audio Inst. - Aux - Busses - User
   
    The buttons will show/hide tracks depending on their category.

    Holding the "Alt" modifier will provide feedback on the category associated with the 
    selected track, while pressing the View buttons will change the category to that associated 
    with the button.

MT4U_Colours (Track Colouring)
------------
    A set of scripts to batch set the color for all selected tracks.