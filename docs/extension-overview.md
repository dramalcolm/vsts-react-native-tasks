[React Native](http://facebook.github.io/react-native/) is an exciting new technology that allows you to bring awesome native app experiences to Android and iOS using a consistent developer experience based on JavaScript and React. Visual Studio Team Services (formerly Visual Studio Online) and Team Foundation Services (TFS) 2015 can be used for building and testing React Native apps in a Continuous Integration (CI) environment thanks to a new [cross-platform agent](http://go.microsoft.com/fwlink/?LinkID=533789) that supports OSX. 

# Visual Studio Team Services Extension for React Native
When you are developing your React Native app you'll be able to take advantage of the React Native packager but in a CI environment or for actual app deployments you'll want to create an offline "bundle".

This extension provides a "React Native Bundle" task to simplify setup and deal with two specific problems: 
1. Node.js version headaches - The task will fetch a compatible version of Node.js if not in use
2. Preventing the "Packager" from starting up as a daemon process and hanging your CI build.

## Quick Start

1. After installing the extension, upload your project to VSTS, TFS, or GitHub.

2. Go to your Visual Studio Online or TFS project, click on the **Build** tab, and create a new build definition (the "+" icon).

3. Click **Add build step...** and select **npm** from the **Package** category

3. Click **Add build step...** and select **React Native Bundle** from the **Build** category

3. Click **Add build step...** and select **Xcode Build** or **Android Build** from the **Build** category

4. Configure the three build steps - *Check out the tool tips for handy inline documentation.*

*Note: Be sure you are running version 0.3.10 or higher of the cross-platform agent and the latest Windows agent as these are required for VS Team Services extension to function. The VSTS hosted agent and [MacinCloud](http://go.microsoft.com/fwlink/?LinkID=691834) agents will already be on this version.*

## Installation for TFS 2015 Update 1 or Earlier

See the [source code repository](https://github.com/Microsoft/vsts-react-native-tasks) for instructions on installing these tasks on TFS 2015 Update 1 or earlier.

## Contact Us
* [File an issue on GitHub](https://github.com/Microsoft/vsts-react-native-tasks/issues)
* [View or contribute to the source code](https://github.com/Microsoft/vsts-react-native-tasks)
