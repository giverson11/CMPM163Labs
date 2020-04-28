# CMPM163Labs


LAB2
------------------------------------------------------------------------
Part1:https://drive.google.com/open?id=15HSsHdradaDTHRmVrrzksoCouMAxyoWD
__________Part2:https://drive.google.com/open?id=1qK6mUiT5SbHChU7VXLHxE5Jm4yQ8NH46
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
LAB4
------------------------------------------------------------------------
https://drive.google.com/open?id=1Mz-vJvsf3JqBUoizsRmSKHxB9FObhEDb
CUBE 1: Cube created with basic THREE material with texture 193 added. (middle lower)
CUBE 2: Cube created with basic THREE material with texture 193 added along with normal map 193_norm. (lower left)
CUBE 3: Cube created with basic THREE material with texture 171 added along with normal map 196_norm. (lower right)
CUBE 4: Cube created using shaders with 171 texture mapped to each surface. (top right)
CUBE 5:  Cube created using shaders with 176 texture tiled 4 times per surface. This was done by doubling the rate at which the uv coordinates grow
as the texture is being mapped to the surface (2.0*uv), thus making it so the texture is drawn 4 times before reaching the end of the surface. The vUv variable
was kept in range of 1.0 by using (mod(vUv, 1.0)) when mapping the texture to prevent the uv coordinate from growing outside the range of the texture.

a. x = fx(u) -> {rounddown(u*8) (u != 1.0)
               {7 (u == 1.0)
b. y = fy(v) -> {rounddown(8*(1-v)) (v != 1.0)
               {0 (v == 1.0)
c. fx(0.375) = rounddown(0.375*8) = 3
   fy(0.25) =  rounddown(8*(1-0.25))= 6
   (3,6) grid = white
