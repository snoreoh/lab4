[![Build Status](https://travis-ci.org/justddreamm/lab04.svg?branch=master)](https://travis-ci.org/justddreamm/lab04)

## Лабораторная работа №04 Лагов Сергей ИУ8-22

Повторил всё, что мы с Вами проделали на семинаре, дома, но уже с другими программами из *lab03*

1. Написал CMakeLists.txt

```
cmake_minimum_required(VERSION 2.8)
project(travis)
include_directories(hello_world_application)
include_directories(solver_application)
```

2. Написал конфигурационный файл *Travis CI*

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

3. Запушил репозиторий на *GitHub*

4. Пришлось обновить токен *GitHub*, так как они *Travis CI* не хотел синхронизироваться с моим репозиторием. Оказывается, *Git* обновил формат токенов, поэтому пришлось его ещё раз сгенерировать

5. После того, как всё синхронизировалось и *Travis CI* увидел репозиторий, я стриггерил билд и началась сборка проекта (безумно приятное чувство в этот момент)

6. Всё продлилось *1 min 38 sec*, завершилось с кодом *0*, что можно считать вполне приемлемым

7. Скопировал ссылку на значок для файлов *Markdown* и вставил его в начало этого *README*
