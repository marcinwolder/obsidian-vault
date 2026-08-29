Plik CMake który pozwala na poprawne budowanie projektów niezależnie od maszyny.
### Możliwość dodawania bibliotek
Dodatkową funkcją jest dodawanie bibliotek prosto z repozytorium git:
```CMake
include(FetchContent)

FetchContent_Declare(cpr GIT_REPOSITORY https://github.com/libcpr/cpr.git GIT_TAG 1.14.2)

FetchContent_MakeAvailable(cpr)  

add_executable(HttpClient src/main.cpp)

target_link_libraries(HttpClient PRIVATE cpr::cpr)
```
### Export komend do kompilowania
Aby poprawnie 
```cmake
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
```
