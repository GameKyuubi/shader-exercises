### This cube has a fragment shader attached to it

What's different from before?  Look at lines 13~17, 30~31, and 35.  Notice that we created a shader as a separate script and given it a special id for reference later at line 31.  We then use the material we've created on line 35, replacing the wireframe material.

Exercises:
* Change the cube's color.  How can you do it this time?
* Try replacing the `fragmentShader` property on line 31 with `fragmentShader: 'void main() { gl_FragColor = vec4(1.0, 1.0, 1.0, 1.0); }'`.  Does it work?  Why?
