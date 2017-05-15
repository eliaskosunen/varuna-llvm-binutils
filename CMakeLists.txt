set(TOOLS_OUTPUT_DIRECTORY ${CMAKE_RUNTIME_OUTPUT_DIRECTORY})

function(add_varuna_llvm_tool tool_name)
    if(WIN32)
        set(EXEC_SUFFIX .exe)
    else()
        set(EXEC_SUFFIX)
    endif()
    add_custom_command(
        OUTPUT ${TOOLS_OUTPUT_DIRECTORY}/varuna-${tool_name}${EXEC_SUFFIX}
        COMMAND ${CMAKE_COMMAND} -E copy
        ${LLVM_TOOLS_BINARY_DIR}/${tool_name}${EXEC_SUFFIX}
        ${TOOLS_OUTPUT_DIRECTORY}/varuna-${tool_name}${EXEC_SUFFIX}
    )
    add_custom_target(varuna-${tool_name} DEPENDS ${TOOLS_OUTPUT_DIRECTORY}/varuna-${tool_name}${EXEC_SUFFIX})
    install(PROGRAMS ${TOOLS_OUTPUT_DIRECTORY}/varuna-${tool_name}${EXEC_SUFFIX} DESTINATION bin)
endfunction()

add_varuna_llvm_tool(llc)
add_varuna_llvm_tool(llvm-as)
add_varuna_llvm_tool(llvm-lto)
add_varuna_llvm_tool(opt)
