function(manual_test)
   add_executable(${ARGV})
   set_target_properties(${ARGV0} PROPERTIES FOLDER reTurn/client/TurnLoadGenClient)
   target_link_libraries(${ARGV0} reTurnClient)
endfunction()

function(test)
   test_base(${ARGV})
   set_target_properties(${ARGV0} PROPERTIES FOLDER reTurn/client/TurnLoadGenClient)
   target_link_libraries(${ARGV0} reTurnClient)
endfunction()

manual_test(TurnLoadGenClient TurnLoadGenClient.cxx TurnLoadGenAsyncSocketHandler.cxx)

