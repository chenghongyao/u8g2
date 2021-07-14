
add_library(u8g2
        "u8g2_d_setup.c"
        "u8g2_d_memory.c"
        "u8g2_intersection.c"
        "u8g2_ll_hvline.c"
        "u8g2_setup.c"
        "u8g2_hvline.c"
        "u8g2_font.c"
        "u8g2_buffer.c"

        "u8g2_box.c"
        "u8g2_circle.c"
        "u8g2_polygon.c"
        "u8g2_bitmap.c"
        "u8g2_cleardisplay.c"
        "u8g2_input_value.c"
        "u8g2_line.c"
        "u8g2_kerning.c"
        "u8g2_message.c"
        "u8g2_selection_list.c"


        "u8x8_gpio.c"
        "u8x8_setup.c"
        "u8x8_display.c"
        "u8x8_cad.c"
        "u8x8_byte.c"

        "u8x8_string.c"
        "u8x8_display.c"
        "u8x8_8x8.c"
        "u8x8_capture.c"
        "u8x8_debounce.c"
        "u8x8_message.c"
        "u8x8_selection_list.c"
        "u8x8_input_value.c"
        "u8x8_u8toa.c"
        "u8x8_u16toa.c"
        )
target_include_directories(u8g2 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

add_library(u8g2_ls013b7dh03 OBJECT "u8x8_d_ls013b7dh03.c" )
target_link_libraries(u8g2_ls013b7dh03 PUBLIC u8g2)
add_library(u8g2::ls013b7dh03 ALIAS u8g2_ls013b7dh03)

add_library(u8g2_fonts OBJECT "u8g2_fonts.c" )
target_link_libraries(u8g2_fonts PUBLIC u8g2)
add_library(u8g2::fonts ALIAS u8g2_fonts)
