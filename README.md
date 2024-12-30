### Installation with Swift Package Manager (Xcode)

[Swift Package Manager](https://swift.org/package-manager/) (SwiftPM) is a tool for managing the distribution of Swift code as well as C-family dependency. From Xcode, SwiftPM got natively integrated with Xcode.

RangersAppLog support SwiftPM from version 5.3.0. To use SwiftPM, you should use Xcode to open your project. Click `File` -> `Swift Packages` -> `Add Package Dependency`, enter [RangersAppLog repo's URL](https://github.com/volcengine/datarangers-sdk-ios-spm). Or you can login Xcode with your GitHub account and just type `datarangers-sdk-ios-spm` to search.

After select the package, you can choose the dependency type (tagged version, branch or commit). Then Xcode will setup all the stuff for you.

If you're a framework author and use RangersAppLog as a dependency, update your `Package.swift` file:

```swift
let package = Package(
    // 5.3.0 ..< 6.0.0
    dependencies: [
        .package(url: "https://github.com/volcengine/datarangers-sdk-ios-spm", .upToNextMajor(from: "0.0.1"))
    ]
)
```
