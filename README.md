# [Codecov](https://codecov.io) qmake_gcc_cpp11_boost_test_gcov Example

[![codecov.io](https://codecov.io/github/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test_gcov/coverage.svg?branch=master)](https://codecov.io/github/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test_gcov?branch=master)
[![Build Status](https://travis-ci.org/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test_gcov.svg?branch=master)](https://travis-ci.org/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test_gcov)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fcodecov%2Fexample-cpp11_boost.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fcodecov%2Fexample-cpp11_boost?ref=badge_shield)

This GitHub is part of [the Travis C++ Tutorial](https://github.com/richelbilderbeek/travis_cpp_tutorial).

The goal of this project is to have a clean Travis CI build, with specs:
 * Build system: `qmake`
 * C++ compiler: `gcc`
 * C++ version: `C++11`
 * Libraries: `STL` and Boost, demonstrating Boost.Test
 * Code coverage: yes
 * Source: multiple files

## Guide
### Travis Setup

Add to your `.travis.yml` file.
```yml
language: cpp
compiler: gcc
addons:
  apt:
    packages: libboost-all-dev

before_install:
  - sudo pip install codecov

script:
  - ./build_test.sh

after_success:
  - codecov
```

### Produce Coverage Reports
#### gcov-5
```sh
gcov-5 main_test.cpp
gcov-5 my_functions.cpp
```

### Private Repo
Repository tokens are required for (a) all private repos, (b) public repos not using Travis-CI, CircleCI or AppVeyor. Find your repository token at Codecov and provide via appending `-t <your upload token>` to you where you upload reports.

## Links
- [Community Boards](https://community.codecov.io)
- [Support](https://codecov.io/support)
- [Documentation](https://docs.codecov.io)


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fcodecov%2Fexample-cpp11_boost.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fcodecov%2Fexample-cpp11_boost?ref=badge_large)