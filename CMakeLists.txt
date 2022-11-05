include_directories(include)
file(GLOB INCLUDES 
  "spine-cpp/include/**/*.h"
  "spine-sfml/*.h"
)
file(GLOB SOURCES
  "spine-cpp/src/**/*.cpp"
  "spine-sfml/*.cpp"
)

add_library(spine-cpp-sfml STATIC ${SOURCES} ${INCLUDES})
target_include_directories(spine-cpp-sfml PUBLIC
  spine-cpp/include
  spine-sfml
  ../SFML/include
)