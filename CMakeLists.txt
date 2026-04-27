add_library(
    numerary
    src/integration.cpp
    src/root.cpp
    src/minimum.cpp
    src/maximum.cpp
    src/differentiation.cpp
    src/incgamma.cpp
    src/regression.cpp
    src/interpolation.cpp
    src/linear_systems_of_equations.cpp
    src/nonlinear_systems_of_equations.cpp
    src/ordinary_differential_equations.cpp
    src/functions.cpp
)

target_include_directories(numerary PUBLIC include)
if(NUMERARY_BUILD_TESTS)
    add_subdirectory(tests)
endif()
