# CMAKE - C++

- salvar o arquivo como CMakeLists.txt

- ` cmake_minimum_required(VERSION 3.10) ` => Versão mínima do cmake necessária

- ` project(HelloWorld VERSION 1.0) ` => Nome do projeto

- ` set(CMAKE_CXX_STANDARD 17) ` => Versão do C++

- ` set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib) ` => Define onde os arquivos gerados serão salvos

- ` set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin) ` => Define onde gerar o .exe

- ` set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin) ` => Define onde gerar o .libDefine onde gerar o .lib

- Adiciona a pasta, indicando que aonde tem as bibliotecas, dispensando o uso de path's completos posteriormente:

```
include_directories(${PROJECT_SOURCE_DIR}/[dll name])

link_directories(${PROJECT_SOURCE_DIR}/[dll name])
```

- ` add_executable(ExecutableName ExecutableSource.cpp) ` => Adiciona o código para compilar


- ` target_link_libraries(ConnectionTest [ddl name].lib) ` => Adiciona a lib, que é necessária no código fonte para a compilação

#
- cria a pasta "build"
- ` cd build `
- ` cmake .. -G "NMake Makefiles" ` => cria os arquivos necessários para a compilação
- ` nmake ` => compila