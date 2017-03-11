add_executable(varuna_llc llc.cpp)
llvm_map_components_to_libnames(varuna_llc_libs
    AArch64
    AMDGPU
    ARM
    BPF
    Hexagon
    Mips
    MSP430
    NVPTX
    PowerPC
    Sparc
    SystemZ
    X86
    XCore
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
target_link_libraries(varuna_llc ${varuna_llc_libs})
