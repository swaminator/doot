Go to your project's Build Phases and create a new Run Script.

Rename the run script to "Run Amplify tools" and move it to the "Compile Sources" script.

![](/images/swift_step4_1_lowres.png)

Paste the following code into the newly created run script:

```
amplify pull -id 24fd5cb-328f2-488fdc-b09a92
amplify codegen
```


Go to *AppDelegate.swift* and add the following lines to initialize Amplify libraries:
```
import Amplify
import AmplifyPlugins
 
    let dataStorePlugin = AWSDataStorePlugin(modelRegistration: AmplifyModels())
        do {
    try Amplify.add(plugin:dataStorePlugin)
    try Amplify.configure()
    print("Initialized Amplify")
        } catch { 
            print("Could not nitialize Amplify: \(error)")
        }
```