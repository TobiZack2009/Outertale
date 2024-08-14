# Project Spacetime Source Code

This file outlines the process of utilizing this source code. You may browse as you wish, but to run or build the game, the guide below will be necessary.

## Pre-Requisites (In Order)
1. Packages
   - **1A** node 16 (newer versions may not work properly)
      - see https://github.com/nvm-sh/nvm for easy install
   - **1B** arch linux packages (or equivalents for your platform) `android-tools asar git gradle jdk11-openjdk sudo wine zip`
---
2. Environment Variables
   - **2A** `ANDROID_HOME` environment variable
      - try `export ANDROID_HOME=/opt/android-sdk`
      - can be appended to `~/.bashrc`
   - **2B** `JAVA_HOME` environment variable
      - try `export JAVA_HOME=/usr/lib/jvm/java-11-openjdk`
      - can be appended to `~/.bashrc`
   - **2C** `PATH` environment variable
      - try `export PATH=${PATH}:$ANDROID_HOME/platform-tools:$ANDROID_HOME/tools:$ANDROID_HOME/tools/bin:$JAVA_HOME/bin`
      - can be appended to `~/.bashrc`
---
3. Tooling
   - **3A** yarn package manager
      - installed with `npm install -g yarn`
   - **3B** android build tools version 33.0.2
      - installed with `sudo sdkmanager --install "build-tools;33.0.2"`

## Run Without Building
1. Install Pre-Requisites **1A** and **3A**
2. Open this folder in a terminal and use `yarn install`
3. Open this folder in two terminals, use `yarn serve <port>` in the first one, use `yarn test <port>` in the second one (the ports used must match)

## Run Without Building (Web Version)
1. Install Pre-Requisites **1A** and **3A**
2. Open this folder in a terminal and use `yarn install` and `yarn serve <port>`
3. Open `localhost:<port>` in your web browser

## Build
1. Install All Pre-Requisites
2. Open this folder in a terminal and use `yarn build`
3. Builds will be created in `app/dist`
