add_executable(varuna-llvm-dis llvm-dis.cpp)
llvm_map_components_to_libnames(dis_libs
    BitReader
    Core
    Support)
target_link_libraries(varuna-llvm-dis ${dis_libs})
