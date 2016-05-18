[![Build Status](https://travis-ci.org/nlohmann/homebrew-json.svg?branch=master)](https://travis-ci.org/nlohmann/homebrew-json)

# Setup

```
brew tap nlohmann/json
```

# Install

```
brew install nlohmann_json
```

To install the bleeding-edge version:

```
brew install nlohmann_json --HEAD
```

# Usage

To use the installed JSON library, add the following string to your compiler call:

```
-I/usr/local/homebrew/Cellar/nlohmann_json/1.1.0/include
```

Ff you installed the HEAD version, use the following:

```
-I/usr/local/homebrew/Cellar/nlohmann_json/HEAD/include
```

# Test

```
brew test nlohmann_json
```

The formula needs to be installed before it can be tested.
