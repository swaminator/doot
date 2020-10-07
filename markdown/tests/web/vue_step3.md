Amplify dependencies are installed through CoacoaPods. Open a terminal window and navigate to the location of the Xcode project for your app.


Initialize CoacoaPods:
```
pod init
```

Update the Podfile to include the following pods:
```
target 'Todo' do
    use_frameworks!

    pod 'Amplify'
    pod 'Amplify/Tools'
    pod 'AmplifyPlugins/AWSAPIPlugin'
    pod 'AmplifyPlugins/AWSDataStorePlugin'

end
```
 

Install the Amplify pod into your project:
```
pod install --repo-udpate
```

Open the *.xcworkspace* file
![](https://raw.githubusercontent.com/cslogan-red/doot/main/markdown/tests/ios/images/swift_step3_lowres.png)
