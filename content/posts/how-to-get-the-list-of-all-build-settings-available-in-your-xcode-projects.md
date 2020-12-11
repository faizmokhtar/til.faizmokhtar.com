---
title: How to get the list of all build settings available in your Xcode projects
date: 2020-12-11T07:57:35.296Z
comments: true
---
I learn a command from my senior, Joseph this week that can print all available build settings available in your Xcode project. 

This is super helpful when you have to write a custom run script or when you have to edit a 3rd party library install script (like what I experienced this week 😭)

Anyway to print the list, run the following command in your project root:

````
xcodebuild -showBuildSettings -project SampleApp.xcodeproj
````

Or if you're using workspace, use the following. `-scheme` have to be define for workspace.

````
xcodebuild -showBuildSettings -workspace SampleApp.xcworkspace -scheme 'SampleApp'
`````

If you want build settings that's specific to certain configuration, ie: `Release` or `Debug`

````
xcodebuild -showBuildSettings -workspace SampleApp.xcworkspace -scheme 'SampleApp' -configuration Release
````

Finally, to make it easier for you to go through the whole list, you can pipe the output to a text file. For example

````
xcodebuild -showBuildSettings -workspace SampleApp.xcworkspace -scheme 'SampleApp' -configuration Release | tee ~/Desktop/build.txt
````

Then you can file the generated files at `~/Desktop/build.txt`

That's it. Hope you will find this useful when debugging.  
