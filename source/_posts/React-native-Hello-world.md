---
title: React-native - Hello world
date: 2017-01-29 09:16:57
tags: react-native
---
#### Step1  
```bash
brew install node
```
Using Homebrew to install Node.js.

#### Step2  
```bash
brew install watchman
```
Watchman is monitor tool from Facebook, We can use Watchman to monitor the change from code. 

#### Step3  
```bash
npm install -g react-native-cli
```
nam is Node Package Manager, it’s like Maven. It’s can help you to download the depend package for you project.

#### Step4
```bash
cd to your directory
react-native init #projectName
```
\#projectName is your project name.
react-native init will create a new React Native project. We can use #projectName.xcodeproj to open from Xcode.

{% asset_img 'messy.png' %}

#### Step5
Click to #projectName/ios/#projectName.xcodeproj 
(If you have permission problem, you can use chmod -R to change to permission)

Click Building...
(Don’t forget to select your device)

