add_executable(test-consensusproblem-montecarlosolver
	${PROJECT_TESTS_INIT_FILE}
	./test_MonteCarloSolver.cpp
)

target_include_directories(test-consensusproblem-montecarlosolver
	PRIVATE ${PROJECT_LIB_DIR}
)

target_link_libraries(test-consensusproblem-montecarlosolver PRIVATE gtest)
target_link_libraries(test-consensusproblem-montecarlosolver PRIVATE consensusproblem)

add_test(
	NAME test-consensusproblem-montecarlosolver
	COMMAND test-consensusproblem-montecarlosolver
)
