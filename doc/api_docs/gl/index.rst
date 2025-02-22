.. _arcade-api-gl:

OpenGL
======

This is the low level rendering API in Arcade and is used
internally for all drawing/rendering. It's a higher level
wrapper over OpenGL 3.3+ core and gives the user easy
access to GPU programs (shaders), textures, framebuffers,
queries, buffers, vertex arrays/geometry and compute shaders
(Note that compute shaders are not supported on MacOS).

This API is also heavily inspired by ModernGL_. It's basically
a subset of ModernGL_ except we are using pyglet's
OpenGL bindings. However, we don't have the context
flexibility and speed of ModernGL_.

The higher level abstraction is the main selling point because
it's much easier to learn, use and understand.
It saves the user from an enormous amount of work
and protects them from the most common pitfalls.

Note that all resources are created through the
:py:class:`arcade.gl.Context` / :py:class:`arcade.ArcadeContext`.
An instance of this type should be accessible the window
(:py:attr:`arcade.Window.ctx`).

This API can also be used with pyglet by creating an instance
of :py:class:`arcade.gl.Context` after the window creation.
The :py:class:`arcade.ArcadeContext` on the other hand
extends the default Context with arcade specific helper methods
and should only be used by arcade.

Some prior knowledge of OpenGL might be needed to understand
how this API works, but we do have examples in the experimental
directory (git).

.. toctree::
   :maxdepth: 1

   context
   texture
   buffer
   buffer_description
   geometry
   framebuffer
   query
   program
   compute_shader
   utils
   exceptions

.. _ModernGL: https://github.com/moderngl/moderngl
