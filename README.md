[![Build Status](https://travis-ci.org/eliaskousk/conan-openssl.svg?branch=release/1.0.2j)](https://travis-ci.org/eliaskousk/conan-openssl)

# conan-openssl

[![badge](https://img.shields.io/badge/conan.io-OpenSSL%2F1.0.2j-green.svg?logo=data:image/png;base64%2CiVBORw0KGgoAAAANSUhEUgAAAA4AAAAOCAMAAAAolt3jAAAA1VBMVEUAAABhlctjlstkl8tlmMtlmMxlmcxmmcxnmsxpnMxpnM1qnc1sn85voM91oM11oc1xotB2oc56pNF6pNJ2ptJ8ptJ8ptN9ptN8p9N5qNJ9p9N9p9R8qtOBqdSAqtOAqtR%2BrNSCrNJ/rdWDrNWCsNWCsNaJs9eLs9iRvNuVvdyVv9yXwd2Zwt6axN6dxt%2Bfx%2BChyeGiyuGjyuCjyuGly%2BGlzOKmzOGozuKoz%2BKqz%2BOq0OOv1OWw1OWw1eWx1eWy1uay1%2Baz1%2Baz1%2Bez2Oe02Oe12ee22ujUGwH3AAAAAXRSTlMAQObYZgAAAAFiS0dEAIgFHUgAAAAJcEhZcwAACxMAAAsTAQCanBgAAAAHdElNRQfgBQkREyOxFIh/AAAAiklEQVQI12NgAAMbOwY4sLZ2NtQ1coVKWNvoc/Eq8XDr2wB5Ig62ekza9vaOqpK2TpoMzOxaFtwqZua2Bm4makIM7OzMAjoaCqYuxooSUqJALjs7o4yVpbowvzSUy87KqSwmxQfnsrPISyFzWeWAXCkpMaBVIC4bmCsOdgiUKwh3JojLgAQ4ZCE0AMm2D29tZwe6AAAAAElFTkSuQmCC)](http://www.conan.io/source/OpenSSL/1.0.2j/eliaskousk/stable)

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
