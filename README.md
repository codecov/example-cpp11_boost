# [Codecov][1] qmake_gcc_cpp11_boost_test_gcov Example
[![Travis CI logo](TravisCI.png)](https://travis-ci.org)
![Whitespace](Whitespace.png)
[![Codecov logo](Codecov.png)](https://www.codecov.io)

[![Build Status](https://travis-ci.org/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test_gcov.svg?branch=master)](https://travis-ci.org/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test_gcov)
[![codecov.io](https://codecov.io/github/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test_gcov/coverage.svg?branch=master)](https://codecov.io/github/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test_gcov?branch=master)

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
## Caveats
### Private Repos
Repository tokens are required for (a) all private repos, (b) public repos not using Travis-CI, CircleCI or AppVeyor. Find your repository token at Codecov and provide via `codecov --token=:token` or `export CODECOV_TOKEN=":token"`
## Other builds
### More complex builds
 * Use C++14: [travis_qmake_gcc_cpp14_boost_test_gcov](https://www.github.com/richelbilderbeek/travis_qmake_gcc_cpp14_boost_test_gcov)

### Less complex builds
 * No code coverage: [travis_qmake_gcc_cpp11_boost_test](https://www.github.com/richelbilderbeek/travis_qmake_gcc_cpp11_boost_test)


## Support

### Contact
- Intercom (in-app messanger)
- Email: [support@codecov.io](mailto:support@codecov.io)
- Slack: [slack.codecov.io](https://slack.codecov.io)
- [gh/codecov/support](https://github.com/codecov/support)

1. More documentation at https://docs.codecov.io
2. Configure codecov through the `codecov.yml`  https://docs.codecov.io/docs/codecov-yaml

[1]: https://codecov.io/
