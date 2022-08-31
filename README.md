# A minimum setup for calling OpenGL from Elixir

This is the code from ["Getting started with OpenGL in Elixir"](https://wtfleming.github.io/blog/getting-started-opengl-elixir/) updated to run on Erlang 25 and Elixir 1.13.

Specific changes:

* added `:wx` to `extra_applications` in `mix.exs`
* silenced a warning about `export_all` from Erlang
* adjusted the usage of `:wxGLCanvas.setCurrent` to reflect the new calling convention (post-wxWidgets 2.9)

## Installation

If you use `asdf` to manage versions, make sure to have the prerequisites for using `:wx` installed **before** installing Erlang or the library will not be available.

On OS X, `brew install wxmac` should be sufficient.

## Usage

Start `iex` with the application loaded:

```
iex -S mix
```

Then start the application:

```
ElixirOpengl.start_link()
```

