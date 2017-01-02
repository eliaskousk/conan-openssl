[![Build Status](https://travis-ci.org/lasote/conan-openssl.svg?branch=release/1.0.2j)](https://travis-ci.org/eliaskousk/conan-openssl)

# conan-openssl

[Conan.io](https://conan.io) package for OpenSSL library

The packages generated with this **conanfile** can be found in [conan.io](https://conan.io/source/OpenSSL/1.0.2j/eliaskousk/stable).

## Build packages

Download conan client from [Conan.io](https://conan.io) and run:

    $ python build.py
    
## Upload packages to server

    $ conan upload OpenSSL/1.0.2j@eliaskousk/stable --all
    
## Reuse the packages

### Basic setup

    $ conan install OpenSSL/1.0.2j@eliaskousk/stable
    
### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*

    [requires]
    OpenSSL/1.0.2j@eliaskousk/stable

    [options]
    OpenSSL:shared=true # false
    # Take a look for all available options in conanfile.py

    [generators]
    txt
    cmake

Complete the installation of requirements for your project running:

    conan install .

Project setup installs the library (and all his dependencies) and generates the files *conanbuildinfo.txt* and *conanbuildinfo.cmake* with all the paths and variables that you need to link with your dependencies.
