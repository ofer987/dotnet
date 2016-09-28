# Installation

## .NET Core

Download the binaries from the [.NET Core webpage](https://www.microsoft.com/net/core)

### macOS

Using a MacBook? You might need to install OpenSSL if it is not already there.

1. Downlaod and install [HomeBrew](http://brew.sh/)
2. `brew install openssl`
3. `ln -s /usr/local/opt/openssl/lib/libcrypto.1.0.0.dylib /usr/local/lib/`
4. `ln -s /usr/local/opt/openssl/lib/libssl.1.0.0.dylib /usr/local/lib/`

### Windows

You have several options

1. Install the binaries at url to use from the command line
2. Install Visual Studio Community Edition (free!), or
3. Install Visual Studio (paid editions) Update 3

## Text Editor

Are you not using Visual Studio? Want to try [Visual Studio Code](https://code.visualstudio.com/)? Love regular text editors? Prefer Emacs and Vi? Great! It is easy to develop C# applications with any editor today.

1. Download OmniSharp Server for Roslyn `git checkout git@github.com:OmniSharp/omnisharp-roslyn.git`
2. Compile and build by following the instructions at https://github.com/OmniSharp/omnisharp-roslyn
3. Integrate with your favourite text editor by following the instructions at http://www.omnisharp.net/

# First Application

## Yeoman as a Generator

- It is much easier to start programming on a templated application.
- Install Yeoman `npm install -g yeoman`
- Install the generators for .NET Core `npm install -g generator-aspnet`
- Install the Docker generator `npm install -g generator-docker`

## Create Your First Project

`yo aspnet`

### Docker Containers

Want to create a container image of your application? 

1. Install Docker, several methods:
  - (macOS) `brew install docker docker-machine docker-compose`
  - (All) From the [website](https://www.docker.com/products/overview)
1. Install wrapper scripts for Docker by executing `yo docker` from the project directory
2. `./dockerTask.sh build release` (Linux or macOS) or `./dockerTask.ps1 build release` (Windows)
