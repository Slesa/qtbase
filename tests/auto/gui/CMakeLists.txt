# Generated from gui.pro.

add_subdirectory(kernel)
if(NOT UIKIT)
    add_subdirectory(image)
    add_subdirectory(math3d)
    add_subdirectory(painting)
    add_subdirectory(text)
    add_subdirectory(util)
    add_subdirectory(itemmodels)
    add_subdirectory(rhi)
endif()
if(QT_FEATURE_opengl AND NOT UIKIT AND NOT WINRT)
     add_subdirectory(qopenglconfig)
     add_subdirectory(qopengl)
endif()
if(QT_FEATURE_vulkan AND NOT UIKIT)
    add_subdirectory(qvulkan)
endif()
