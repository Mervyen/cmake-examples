# Set the project name
project (sublibrary1)

# Add a library with the above sources
add_library(${PROJECT_NAME} src/sublib1.cpp)#生成库的名字为${PROJECT_NAME}(sublibrary1)
add_library(sub::lib1 ALIAS ${PROJECT_NAME})#创建库的别名

target_include_directories( ${PROJECT_NAME}
    PUBLIC
        ${PROJECT_SOURCE_DIR}/include
)
