# CMPM163Labs


LAB2
------------------------------------------------------------------------
Part1:https://drive.google.com/open?id=15HSsHdradaDTHRmVrrzksoCouMAxyoWD
Part2:https://drive.google.com/open?id=1qK6mUiT5SbHChU7VXLHxE5Jm4yQ8NH46
https://drive.google.com/open?id=1Ia1bDh9WOfuDdmmM7_bqfahEfvavBh3m
------------------------------------------------------------------------
LAB3
------------------------------------------------------------------------
https://drive.google.com/open?id=1CuTb58CfGz0LbGdSclJMYN2yylLVw9oe
The leftmost square is a THREE basic mesh material with a wireframe and a yellow color.
The next square going to the right uses the shaders from the assignment with a light blue interpolated
with a purple blue color. The next cube is the THREE phong material cube from the assignment with a metalic and green sheen.
Finally the one on the far right is the custom shaded cube. I first made all pixels on the cube oscillate between a variety of color values based on the position
of the vertex and the time from the first render using a sin function for each color with THREE libraries clock object. I then decided to experiment with 3d simplex
noise I found online and tried to make a lava lamp type texture by adding the snoise output of the position vector to each color. Then using another technique I found online, I interpolated a
subset of color values to have color using the smoothstep function, while the rest of the noise particles are turned black. This gave some the 3d looking goop even though the model
is done completely with shaders.
Sources:https://thebookofshaders.com/glossary/?search=smoothstep
https://gist.github.com/patriciogonzalezvivo/670c22f3966e662d2f83
------------------------------------------------------------------------
