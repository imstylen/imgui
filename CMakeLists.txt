project(imgui)

add_library(imgui 
		"imconfig.h"
		"imgui.h"
		"imgui.cpp"
		"imgui_draw.cpp"
		"imgui_internal.h"
		"imgui_widgets.cpp"
		"imstb_rectpack.h"
		"imstb_textedit.h"
		"imstb_truetype.h"
		"imgui_demo.cpp"
		"imgui_tables.cpp"
		"backends/imgui_impl_opengl3.h"
		"backends/imgui_impl_opengl3.cpp"
		"backends/imgui_impl_glfw.h"
		"backends/imgui_impl_glfw.cpp"
		"libs/emscripten/emscripten_mainloop_stub.h"
)


target_include_directories(imgui PUBLIC 
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/backends
    ${CMAKE_CURRENT_SOURCE_DIR}/libs

)


target_link_libraries(imgui PRIVATE glfw)