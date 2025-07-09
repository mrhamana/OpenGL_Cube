A **graphics API specification** — a set of **rules and functions** that define how to communicate with the GPU for rendering. It doesn't create windows, handle inputs, or provide GUI tools.

There are many misunderstandings regarding OpenGL. Some of them are mentioned below:
1) It describes **what functions must exist**
2) It defines **how these functions should behave**.
3) But it **doesn’t implement** those functions.

And the specifications mentioned in the OpenGL should be followed by the library which implements these things in programs. Some of the library used in this project are mentioned below:

1) GLFW (Graphics Library Framework) 
	One of the core library which creates windows, utilizes input/output to display in runtime, the event loop, allowing your application to respond to user actions, and many other things which makes the application interactive.


2) GLAD(OpenGL Loader Generator)
	GLAD is an **OpenGL loader library**. Its purpose is to load OpenGL function pointers at runtime. Modern OpenGL versions (3.0+) are designed in a way that many functions are not directly available through the standard library. Instead, they are exposed as function pointers that need to be queried from the graphics driver.
