add_executable(varuna-llvm-as llvm-as.cpp)
llvm_map_components_to_libnames(as_libs
    AsmParser
    BitWriter
    Core
    Support)
target_link_libraries(varuna-llvm-as ${as_libs})
