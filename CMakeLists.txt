cmake_minimum_required(VERSION 3.14) # 3.4 Required for manifest in sources, but compat with <3.5 will soon be removed. Just use 3.14 which was shipped with VS2019 Update 1
project(UTF8WindowsDemo)

# Any file with '.manifest' extension will be merged into the final manifest
add_executable(test_utf8 main.cpp app.manifest)
target_compile_options(test_utf8 PUBLIC /utf-8)

