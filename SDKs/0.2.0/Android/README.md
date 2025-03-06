Version: 0.2.0
# RPlus Android Library

## Getting Started

### Installation

1. Put **rplus_android** dir on your project root path
2. Add the maven local repository to project build.gradle or settings.gradle in the any way of following:

```
dependencyResolutionManagement {
        repositories {
            maven {
                url "file:///${rootProject.projectDir}/rplus_android/"
            }
    }
}
```

or

```
allprojects {
    repositories {
        maven {
            url "file:///${project.rootDir}/rplus_android/"
        }
    }
}
```

3. Add dependency to app gradle file

```
dependencies {
    implementation("com.lotusflare.rplus:rplus-android:0.2.0")
}
```

### How To Use

1. Import the class

```
import com.lotusflare.rplus.RPlusSDK
```

2. Use the method to start rplus flow

```
    /**
     * Start rplus
     * @param context applicationContext for start rplus
     * @param clientId rplus client id
     * @param clientKey rplus client key
     * @param userAuth rplus userAuth
     * @param onSuccess success callback
     * @param onError error callback
     * @returns Unit
     */
    fun startRPlus(
        context: Context,
        clientId: String,
        clientKey: String,
        userAuth: String,
        onSuccess: (Boolean) -> Unit,
        onError: (Error) -> Unit
    )
```

#### Example for start plus flow
```
    val context = this.applicationContext
    val clientId = "xxx"
    val clientKey = "xxx"
    val userAuth = "xxx"
    RPlusSDK.startRPlus(context, clientId, clientKey, userAuth, onSuccess = { }, onError = { })
```
