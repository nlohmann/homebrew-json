# JSON for Modern C++ (Homebrew formula)

[![asciicast](https://asciinema.org/a/0ewqttgassj17lr8f2gxi055d.png)](https://asciinema.org/a/0ewqttgassj17lr8f2gxi055d)

[![Build Status](https://travis-ci.org/nlohmann/homebrew-json.svg?branch=master)](https://travis-ci.org/nlohmann/homebrew-json)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/nlohmann/homebrew-json/master/LICENSE.MIT)

This [Homebrew](http://brew.sh) formula installs the header-only [JSON for Modern C++](https://github.com/nlohmann/json) library to your system.

TL;DR: Just execute `brew tap nlohmann/json` and `brew install nlohmann_json`.

## Usage

To use the JSON library, add

```cpp
#include <json.hpp>
```

to your code and add

```
-I/usr/local/homebrew/Cellar/nlohmann_json/1.1.0/include
```

to your compiler flags.

## Tests

With `brew test nlohmann_json` you can check if the formula is working properly. Note the formula needs to be installed before it can be tested.
