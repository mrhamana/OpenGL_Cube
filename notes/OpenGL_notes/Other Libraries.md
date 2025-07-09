## GLFW (Graphics Library Framework)

This is a library targeted at OpenGL . The most of the codes here is written in C lang.It allows us to create an OpenGL context, define window parameters, and handle user input, which is plenty enough for our purposes.

## GLAD
OpenGL is only really a standard/specification it is up to the driver manufacturer to implement the specification to a driver that the specific graphics card supports. Since there are many different versions of OpenGL drivers, the location of most of its functions is not known at compile-time and needs to be queried at run-time. It is then the task of the developer to retrieve the location of the functions he/she needs and store them in function pointers for later use. Retrieving those locations is [OS-specific](https://www.khronos.org/opengl/wiki/Load_OpenGL_Functions). In Windows it looks something like this:
```
typedef void (*GL_GENBUFFERS) (GLsizei, GLuint*); 
GL_GENBUFFERS glGenBuffers = (GL_GENBUFFERS)wglGetProcAddress("glGenBuffers"); unsigned int buffer; glGenBuffers(1, &buffer);
```