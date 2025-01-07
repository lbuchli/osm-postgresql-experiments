#-----------------------------------------------------------------------------
#
#  CMake Config
#
#-----------------------------------------------------------------------------

add_executable(ope main.cpp util.cpp formatting.cpp table.cpp)
target_link_libraries(ope ${Boost_LIBRARIES} ${OSMIUM_LIBRARIES} fmt::fmt)
set_pthread_on_target(ope)
install(TARGETS ope DESTINATION bin)

