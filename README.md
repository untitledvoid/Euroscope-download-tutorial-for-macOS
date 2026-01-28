# EuroScope on macOS (via Sikarugir)

This guide explains how to run EuroScope on macOS using Sikarugir (Wine-based).
It can also be adapted for Linux with fewer requirements.

## Hardware Requirements

- Computer running macOS or any Linux distro

## Software Requirements

### macOS only
- Xcode  
  - Install from the App Store  
  - OR download a compatible version from:
    https://developer.apple.com/xcode/resources/ (Additional Tools)

- Xcode Command Line Tools (xcode-select)

### macOS & Linux
- Homebrew
- Sikarugir
- EuroScope installer

> Linux users do NOT need Xcode or xcode-select

## Installation

### 1. Install Xcode (macOS only)

Install Xcode from the App Store (≈10 GB)  
Or download a compatible version from Apple Developer Resources if you have an older macOS version.

### 2. Install Xcode Command Line Tools (macOS only)

Open Terminal and run:

xcode-select --install

### 3. Install Homebrew

Paste the following into Terminal:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

### 4. Install Sikarugir

Run:

brew upgrade
brew install --cask Sikarugir-App/sikarugir/sikarugir

### 5. Install EuroScope in Sikarugir

1. Open Sikarugir
2. Create a new engine (latest version available)
3. Create a blank wrapper
4. Open Winetricks for the wrapper
5. Install the following packages:

dotnet40  
dotnet45  
dotnet46  
dotnet461  
dotnet462  
dotnet472  
dotnet48  
iertutil  
msls31  
msxml6  
urlmon  
vcrun2010  
vcrun2022  
winine  

6. Run the EuroScope .msi installer inside the wrapper.


## Notes

- Installation may take a long time due to multiple .NET versions
- Restart the wrapper if EuroScope does not launch on first attempt
- Euroscope VCCS will not work with this setup due to software limitations

   

