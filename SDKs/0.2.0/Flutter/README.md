Version: 0.2.0

# flutter_rplus

## Installation

1. Copy the **flutter_rplus** folder to your project's root path.

2. Add the dependency in pubspec.yaml

```
...
dependencies:
  ...
  flutter_rplus:
    path: ./flutter_rplus
```

3. Run `flutter pub get`.

## How To Use

### Import the library

```javascript
import "package:flutter_rplus/rplus.dart";
```

### Use the method to start rplus flow

#### Start rplus Method

```javascript
/**
 * Start rplus
 * @param clientId rplus client id
 * @param clientKey rplus client key
 * @param userAuth rplus userAuth
 * @returns true: success, false: fail
 */
  static Future<bool?> startRPlus(String clientId, String clientKey, String userAuth)
```

#### Example for start plus flow

```javascript
  RPlus.startRPlus('xxx','xxx','xxx').then( (result) {

  }).catchError((error) {

  });
```
