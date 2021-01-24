add_library(imgui
    "imconfig.h"
	"imgui.h"
	"imgui.cpp"
	"imgui_draw.cpp"
	"imgui_internal.h"
    "imgui_widgets.cpp"
    "imgui_tables.cpp"
	"imstb_rectpack.h"
	"imstb_textedit.h"
	"imstb_truetype.h"
    "imgui_demo.cpp"
)

# for stb_sprintf
# imgui_stb_dir = PROJECT_SOURCE_DIR/OverEngine/vendor/stb
string(JOIN "/" imgui_stb_dir ${PROJECT_SOURCE_DIR} "OverEngine/vendor/stb")

target_include_directories(imgui PRIVATE
	${imgui_stb_dir}
)
