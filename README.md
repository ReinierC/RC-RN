# Running React Native for the first time - Reinier Caron
React Native, first project.

I'm running Linux Mint.18 64m Installation will differ on other systems.

## Step 1: Install NodeJs & NPM

### Install NodeJs

Run this in your terminal:

$``` curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -```

### Install Latest Nodejs and NPM

$``` sudo apt-get install -y nodejs```

***_Optional:_*** _There are development tools such as gcc-c++ and make that you need to have on your system, in order to build native addons from npm._

$```sudo apt-get install -y build-essential```

### Testing Latest Nodejs and NPM

To have a simple test of nodejs and NPM, you can just check the versions installed on your system by using the following commands:

$ ```nodejs --version```

$ ```npm --version```

That is it, Nodejs and NPM are now installed and ready for use on your system.

_I found this walkthrough at [tecmint.com](https://www.tecmint.com/install-nodejs-npm-in-centos-ubuntu/). They also describe the same procedure for RHEL, CentOS, Fedora, Debian and Ubuntu._

## Creating a React Native App

I followed the steps taken on the [Facebook.github.io/react-native](https://facebook.github.io/react-native/docs/getting-started.html) website.

 1. Assuming that you have Node installed, you can use npm to install the create-react-native-app command line utility:
 
    $ ```sudo npm install -g create-react-native-app```  
     
 2. Then run the following commands to create a new React Native project, in my case: "RCProject":
 
    $ ```create-react-native-app RCProject```  
    $ ```cd RCProject```  
    $ ```npm start```  
    
    This will start a development server for you, and print a QR code in your terminal.
     > At the time I am writing this,  
     create-react-native-app does not work  
     with NPM 5. I downgraded to 4.X  
     to make it work. 
    
### Running your React Native application

1. Install the [Expo](https://expo.io/) client app on your iOS or Android phone and connect to the same wireless network as your computer.
   Using the Expo app, scan the QR code from your terminal to open your project.  
     * I had to enable USB debugging on my phone
     * Start a WiFi Hotspot on my phone
     * open 3 ports in my laptop's firewall
     
   ***_OR_***
   
   Install the Desktop Development Tool: XDE  
   XDE stands for Expo Development Environment. It is a standalone desktop app that includes all dependencies you’ll need to get started.
   
   Download the latest version of XDE for [macOS](https://xde-updates.exponentjs.com/download/mac), [Windows (64-bit)](https://xde-updates.exponentjs.com/download/mac), or [Linux](https://xde-updates.exponentjs.com/download/linux-x86_64).

   * On Linux, open with:  
  ```chmod a+x xde*.AppImage``` and ```./xde*.AppImage```  
  
   When I first ran _./xde*.AppImage_  
   XDE threw the following error:  
   _Warning: Not using the Expo fork of react-native. See https://docs.expo.io/_
  
   This was solved changing the ***package.json*** file:
   ```
   "dependencies": {
   "expo": "^20.0.0",
   "react": "16.0.0-alpha.12",
   "react-native": "https://github.com/expo/react-native/archive/sdk-20.0.0.tar.gz"
   ```

2. now to install [genymotion](https://www.genymotion.com) Modifying your app  

   Now that you have successfully run the app, let's modify it.  
   Open App.js in your text editor of choice and edit some lines.  
   The application should reload automatically once you save your changes.  
   
***That's it!***

Congratulations! You've successfully run and modified your first React Native app.
