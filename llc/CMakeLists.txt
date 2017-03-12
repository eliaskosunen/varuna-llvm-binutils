add_executable(varuna-llc llc.cpp)
llvm_map_components_to_libnames(llc_libs
    ${LLVM_TARGETS}
    Analysis
    AsmPrinter
    CodeGen
    Core
    IRReader
    MC
    MIRParser
    ScalarOpts
    SelectionDAG
    Support
    Target
    TransformUtils)
target_link_libraries(varuna-llc ${llc_libs})
