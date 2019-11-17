# JSON for Modern C++ (Homebrew formula)

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

## Update formula

```sh
export VERSION=3.7.2
export URL=https://github.com/nlohmann/json/archive/v$VERSION.tar.gz
wget $URL
export SHA=$(shasum -a 256 v$VERSION.tar.gz | awk '{ print $1 }')
rm v$VERSION.tar.gz
echo "class NlohmannJson < Formula" > nlohmann_json.rb.tmp
echo "  desc \"JSON for Modern C++\"" >> nlohmann_json.rb.tmp
echo "  homepage \"https://github.com/nlohmann/json\"" >> nlohmann_json.rb.tmp
echo "  url \"$URL\"" >> nlohmann_json.rb.tmp
echo "  sha256 \"$SHA\"" >> nlohmann_json.rb.tmp
tail -n+6 nlohmann_json.rb >> nlohmann_json.rb.tmp
mv nlohmann_json.rb.tmp nlohmann_json.rb
git add nlohmann_json.rb
git commit -m "v$VERSION"
git push
```
