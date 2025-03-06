Version: 0.2.0

# RPlusIOSLibrary

The minimum ios supported version is 10.0.

## Installation
1. Copy the **RPlusIOSLibrary** folder to your project's root path.
2. Add the dependecy in Podfile:

```ruby
pod 'RPlusIOSLibrary', :path => './RPlusIOSLibrary/'
```

3. Run `pod install`

## How To Use

### Import the library

```ruby
import RPlusIOSLibrary
```

### Start rplus Method

RPlus Cofiguration
```	javascript
public class RPlusConfiguration {
    // rplus client id
    public var clientId: String
    // rplus client key
    public var clientKey: String
    // rplus userAuth
    public var userAuth: String
    // rplus global configuration
    public static let configuration: RPlusConfiguration
}
```

RPlus Manager
```javascript
public class RPlusManager {
    /*
        Start rplus
        Parameters:
        - config: The configuration for rplus, default is `RPlusConfiguration.configuration`. 
        - rootVC: The viewcontroller to present rplus flow. default is current viewcontroller.
        - completion: The callback block.
    */
    public func startRPlus(withConfig config: RPlusConfiguration? = nil, 
                                      rootVC: UIViewController? = nil, 
                                  completion: RPlusCompletion<Bool>? = nil)
}
```

### Example for start plus flow

```ruby
    let config = RPlusConfiguration.configuration
    config.clientId = "xxx"
    config.clientKey = "xxx"
    config.userAuth = "xxx"

    RPlusManager.shared.startRPlus { _, error in
        if let error { print("Error: \(error.description)") }
    }
```
