find_package(boost_filesystem CONFIG REQUIRED)
find_package(boost_system CONFIG REQUIRED)
find_package(boost_unit_test_framework CONFIG REQUIRED)

add_executable(
    numerary_tests
    test_numerary.cpp
    test_root.cpp
    test_minimum.cpp
    test_maximum.cpp
    test_integrate.cpp
    test_differentiate.cpp
    test_gamma.cpp
    test_newton.cpp
    test_dorpi.cpp
    test_lagrange_polynomial.cpp
    test_regression.cpp
    test_linear_systems_of_equations.cpp
)

target_compile_definitions(numerary_tests PRIVATE BOOST_TEST_DYN_LINK)

target_link_libraries(
    numerary_tests
    PRIVATE
    numerary
    Boost::filesystem
    Boost::system
    Boost::unit_test_framework
)

add_test(NAME numerary_tests COMMAND numerary_tests)
