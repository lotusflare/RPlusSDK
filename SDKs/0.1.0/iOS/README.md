Version: 0.1.0

# RPlusIOSLibrary

## Installation
1. Copy the **RPlusIOSLibrary** folder to your project's root path.
2. Add the dependecy in Podfile:

```ruby
pod 'RPlusIOSLibrary', :path => '../'
```

3. Run `pod install`

## How To Use

#### Import the library

```ruby
import RPlusIOSLibrary
```

#### Use the method to start rplus flow

```ruby
    let config = RPlusConfiguration.configuration
    config.clientId = "xxx"
    config.clientKey = "xxx"
    config.userAuth = "xxx"
    RPlusManager.shared.startRPlus(withConfig: config) { _, error in
        if let error { print("Error: \(error.description)") }
    }
```
