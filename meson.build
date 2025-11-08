imgui_srcs = files(
  'imgui.cpp',
  'imgui_draw.cpp',
  'imgui_tables.cpp',
  'imgui_widgets.cpp',
  'imgui_demo.cpp',
  'backends/imgui_impl_glfw.cpp',
  'backends/imgui_impl_opengl3.cpp',
)

imgui_inc = include_directories('.', 'backends')

imgui_lib = static_library('imgui', imgui_srcs,
  include_directories: imgui_inc,
  cpp_args: [
    '-DIMGUI_ENABLE_DOCKING',
    '-DIMGUI_IMPL_OPENGL_LOADER_GLEW'
  ],
  dependencies: [dep_glfw, dep_gl])

imgui_dep = declare_dependency(
  link_with: imgui_lib,
  include_directories: imgui_inc,
)
