# How do I use different versions of the sub dependencies like the support libraries?

This can be really easy achieved by providing a resolutionStrategy to your build.

## Sample code
Simple add the following to your modules build.gradle. It allows you to define whatever version you need for the sub dependencies. 

```xml

configurations.all {
    resolutionStrategy.force "com.android.support:support-v4:${versions.androidX}"
    resolutionStrategy.force "com.android.support:appcompat-v7:${versions.androidX}"
    resolutionStrategy.force "com.android.support:cardview-v7:${versions.androidX}"
    resolutionStrategy.force "com.android.support:recyclerview-v7:${versions.androidX}"
    resolutionStrategy.force "com.android.support:design:${versions.androidX}"
    resolutionStrategy.force "com.android.support:support-annotations:${versions.androidX}"
}
```

https://github.com/mikepenz/MaterialDrawer/blob/develop/app/build.gradle
