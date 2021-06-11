[![Build Status](https://travis-ci.org/justddreamm/lab04.svg?branch=master)](https://travis-ci.org/justddreamm/lab04)

## Homework. Lab #04


1. Общий CMakeLists.txt

```
cmake_minimum_required(VERSION 2.8)
project(travis)
include_directories(hello_world_application)
include_directories(solver_application)
```

2. Файл для *Travis CI* ".travis.yml"

```
language: cpp

script:
- cd solver_application
- cmake .
- make
- cd ..
- cd hello_world_application
- cmake .
- make

addons:
  apt:
    sources:
      - george-edison55-precise-backports
    packages:
      - cmake
      - cmake-data
      - mingw-w64
```

3. Далее заливаем все файлы на *GitHub*

4. После соединения с *Travis CI* началась сборка проекта.

