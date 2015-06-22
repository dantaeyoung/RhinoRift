**RhinoRift**
=========
**(Oculus Rift DK1/2 + Rhino + Grasshopper + OpenTrack)**

1) Download these files (also attached below):

2) Run OpenTrack binary - working version in OpenTrackBinary folder, or download from https://github.com/opentrack/opentrack.

3) In OpenTrack, load the 'OpenTrackRiftGrasshopperUDP.ini' profile. Click the 'Start' button and move your Rift around - make sure that it looks like the Yaw/Pitch/Roll data is being sent. 

4) In Rhino, open the example 3dm file. You'll notice that there are two viewports - called 'LeftEye' and 'RightEye'. These have been placed to mimic where the screens should be for the Oculus Rift --- but only when Rhino is in fullscreen mode, with the command 'Fullscreen'. The placement needs to be tweaked, but should work.
If you want to use your own model, you can load your own .3dm file in Rhino, then you can right-click on the viewport name, and go to Viewport Layout > Read from File. If you then load my test file, Rhino should open my two viewports, sized correctly, onto your model.
The placement of these viewports need to be tweaked; if you find a better viewport layout, upload an empty Rhino file with your viewports, and we can share eye-layout 'templates'.

5) In Grasshopper, open the example .ghx definition. Everything that is multiple-grouped is a value that can be changed. Two things here:
- IPD: Set this and convert it to the proper units for your model. 
- Left/right viewport names. In this case, leave this as-is, since you're using my example file.

6) Turn on the Grasshopper Timer, if it isn't on already.

7) In the GH definition, toggle 'SyncEyes' to be True. Then, in the left viewport, try orbiting around with the mouse. The 'RightEye' viewport should move around as well, pretty much simultaneously.

8) In OpenTrack, click 'Start', then toggle 'ReadUDP' to be True. You should see the 'OpenTrackInfo' panel fill with data that's constantly changing.

9) Move around the landscape with your camera, and when you set on a starting view that's ideal, click the triangle of the Data Dam component to 'store' the data.

10)  Finally, toggle 'OculusMove' to be true. If all works correctly, both viewports should move based on the Rift's movement.
