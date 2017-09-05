### Uniform time

Let's play with time.  Look at lines 15, 18, 35, and 57.  We create u_time on line 35 and put it inside our uniform.  On line 57, we increment u_time every tick so that it changes over time.

Exercises:
* What is our delta time?  Can you change the speed at which the teapot flashes?
* Look at line 18.  Notice that the second parameter of the vec4 is more than just `u_time` or `sin(u_time)`.  Why?  Try replacing it with `u_time` and `sin(u_time)` and see what happens.
* Try combining `u_time` and `st` in various ways.  Can you come up with something interesting?  Try using functions like `sin`, `cos`, `tan`, `abs`, and `clamp`.
