Version: 0.2.0

# react-native-rplus

## Installation

1. Copy the **react-native-rplus** folder to your project's root path.

2. Add the dependecy in package.json

```
{
  "dependencies": {
	...
    // Add following dependecy
    "react-native-rplus": "file:react-native-rplus"
  },
}
```

3. Run `npm install` or `yarn install`

## How To Use

### Import the library

```javascript
import { startRPlus } from 'react-native-rplus';
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
  startRPlus(clientId: string, clientKey: string, userAuth: string): Promise<Boolean>
```

#### Example for start plus flow

```javascript
  startRPlus("xxx", "xxx", "xxx").then((result) => {});
```
