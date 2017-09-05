### Varyings and Uniforms

Here we introduce two concepts: Varyings and Uniforms.

#### Uniforms
A uniform is a variable passed into our shader (in this case from our app) that stays constant between all shader instances for a given frame.  In this case, we are passing in the resolution of the window as the 2-D vector `u_resolution` so that we can normalize our xy coordinates and keep our results consistent even if the resolution size is scaled.  You can test this by changing the window size and then reloading the page.

#### Varyings
A varying is another variable that our shader recieves, but this type of variable can be different between shader instances (it "varies").  In the case of our example, each shader receives a varying variable `gl_FragCoord`, which contains xy coordinates for the location of the pixel on the screen that it is supposed to manipulate.  In WebGL this variable is provided to us directly, but in other GLSL implementations it may need to be declared as something like `varying vec4 gl_FragColor` similar to our uniform above.

Exercises:
* Change the cube's color.  How can you do it this time?
* Try replacing the `fragmentShader` property on line 31 with `fragmentShader: 'void main() { gl_FragColor = vec4(1.0, 1.0, 1.0, 1.0); }'`.  Does it work?  Why?
* In GLSL, we have access to many math functions that you may be familiar with.  Try replacing some parameters in the `vec4` on line 17 with `sin(st.x * 3.14)`.  Does it give the results you expect?  Try changing the value of `3.14` and see what happens.
* If you try a particularly large value (~100 or so) for the exercise above, you may have noticed that the black bars are larger than the colored ones.  Why?  Can you fix this?
* Our `st` variable is a 2-D vector, which means it also has a y property.  Replace one of the `0.0` values on line 17 with `st.y`.  What happens?
