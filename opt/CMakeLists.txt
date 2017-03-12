file(GLOB opt_sources *.cpp)
file(GLOB opt_headers *.h)

add_executable(varuna-opt ${opt_sources} ${opt_headers})
llvm_map_components_to_libnames(opt_libs
    ${LLVM_TARGETS}
    Analysis
    BitWriter
    CodeGen
    Core
    IPO
    IRReader
    InstCombine
    Instrumentation
    MC
    ObjCARCOpts
    ScalarOpts
    Support
    Target
    TransformUtils
    Vectorize
    Passes)
target_link_libraries(varuna-opt ${opt_libs})
