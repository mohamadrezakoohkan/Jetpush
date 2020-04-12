# Jetpush
Jetpush is a Continues Deployment tool for iOS distribution with automatic signing.  
Also Jetpush can create GitHub and GitLab CI configuration.

<img src="https://github.com/mohamadrezakoohkan/Jetpush/blob/master/jetpush.gif">

## How it works
Jetpush using xcodebuild commandline tool to `archive` and `export` project to an IPA file.  
Jetpush communicate with `jetpush-config.env` which contains project constants.
Jetpush export-configurations reads from known `ExportOptions.plist` from `jetpush-config.env`, At last it commit and push result to git with message of IPA information.

## Requirements 
- macOS
- Xcode 10.2+

>  Also fully compatible with GitHub and GitLab runners

## Installation
1. Clone the repo:  

       https://github.com/mohamadrezakoohkan/Jetpush

2. Change directory to `Jetpush`:  
   
       cd Jetpush

3. Install jetpush:  
   
       ./jetpush install 

> This line will create an executable refrence in /usr/local/bin, Then you can directly call jetpush everywhere

1. Go to your xcode project directory:  
   
       cd mySample

2. Open xcode:  
 
       open mySample.xcworkspace

4. In the project setting select your target, then open Signing & Capabilities And turn on: 
    
       `Automatically manage signing`

5. Back too `Terminal` and initialize `jetpush-config.env` using:  

       jetpush init

6. Open `jetpush-config.env` and fill the configurations as need.
       > If you have xcworkspace just include WORKSPACE  
       
       PROJECT=""
       WORKSPACE="mySample.xcworkspace"
       SCHEME="mySample"
       CONFIGURATION="Release" # Or Debug, ...
       EXPORT_OPTIONS="ExportOptions.plist" # You can name your export-options whatever you like

7. Run jetpush in terminal to see the magic 
    
       jetpush

## Contact
Follow and contact me on [Instagram](https://www.instagram.com/mohamadreza.codes/),  [Github](https://github.com/mohamadrezakoohkan), [LinkedIn](https://www.linkedin.com/in/mohammad-reza-koohkan-558306160/) and [stack overflow](https://stackoverflow.com/users/9706268/mohamad-reza-koohkan?tab=profile). If you find an issue [open a ticket](https://github.com/mohamadrezakoohkan/Jetpush/issues/new). You can send me email at mohamad_koohkan@icloud.com .

## License
Plister is released under the [MIT license](https://github.com/mohamadrezakoohkan/Jetpush/blob/master/LICENSE.md).

