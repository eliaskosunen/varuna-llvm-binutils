add_executable(varuna-llvm-lto llvm-lto.cpp)
llvm_map_components_to_libnames(lto_libs
    ${LLVM_TARGETS}
    BitReader
    BitWriter
    Core
    IRReader
    LTO
    MC
    Object
    Support
    Target)
target_link_libraries(varuna-llvm-lto ${lto_libs})
