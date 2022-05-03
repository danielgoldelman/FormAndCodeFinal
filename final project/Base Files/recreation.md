# Base Files

Welcome to the `Base Files` directory! If you wanted to figure out how all of this was built, you're in the right place. 

*ghSetup.gh* is the Grasshopper file that manipulated all of the shapes in the *setups.3dm* Rhino 7 file. To recreate all of the shapes contained within the various files you will see, please read the detailed instructions within the "{}.md" files in the directory.

`SVG Examples` explains how to use a downloadable svg with this tool.

### What the hell is going on in that Grasshopper file?

This short script does a lot of work behind the scenes to create the shapes you can see in the Rhino files. Here is what to do to use it:

- Draw a shape, upload a svg, or make some lines and join them, and place that shape into the middle of the circle in the middle of the drawn graph. Try to make your shape about half the size of that circle (resizing to make that possible is completely ok).
- Right click on the curve on the very left of the Grasshopper script. Click on "Set one curve".
- Select the curve you drew.
- Change the slider on the very left called "Count Dividers" to a desired value.
- Change the number slider on top in the middle of the script to a desired value.
- Press the button on the right side of the script to reset the outputs.
- To print the shape to a layer, right click on the curve on the very right of the script and click "Bake". You can bake it to the "testLayer".

But what is it acutally doing?

- Intakes a curve and divides it into the number of nodes you selected in the "Count Dividers" slider.
- Makes lines in between all of those nodes in the sequence.
- Based on the number slider you changed in the middle of the script, it increases or decreases the distance between those points. Each point will be equidistant to its immediate neighbors.
- A few of the blocks in the script try to eliminate crossovers by creating a circle around each node that every other node cannot be placed in.
- The large circle that should be encapsulating your design will try to place a bound on the points; that is, the points will try to stay within that circle.
- These lines are then converted from a polyline into a closed shape as a curve.


### Important notices:
- You can change the number slider that controls the multiplication without having to reset the function using the button, but changing the number of dividers will require you to reset the function.
- Making the shape too large will pretty largely affect the outcomes of the function. It is highly reccommended to make your shape about half the size of the bounding circle.
- Creating shapes with lines inside some outer boundary (like the ying yang in `Symbol Animations`) creates some weird interactions. This is not to say not to do that, just a warning.
- This tool only works on single connected curves. If you want to create new shapes that uses multiple curves as the base, you will need to run the tool on each curve individually. I reccommend splitting up the points allocated for each to create the two shapes. See the videos in this directory for more explanation.
- *setup.3dm* is not a finished work, and it is not supposed to be. It is instead a place for one to sketch their ideas and experiment. See the other files for finished and well organized work.

There are a few ways to make shapes to use with this tool. First, you can draw shapes using built-in Rhino properties or Grasshopper, then assign the curve to the tool's input. Note that if you use multiple lines or shapes to build some curve you may need to use a "join" method to make them into one curve. A second option is to import SVG files. See *SVGExamples.md* within the `SVG Examples` directory for instructions.
