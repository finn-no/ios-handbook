# Dos and don'ts

## SDKs tag versioning

### What?
After merging any PR to any SDK's master, please don't forget to make a new release (at least patch) using `bundle exec fastlane` script.
After creating a new SKD's tag please bump it's version on ios-app. If you have any blockers to do so - please make a note inside PR you closed.

### Why?
All releases should be done automatically to avoid breaking team's release guidelines. Also it is very important to keep all tag's inside all SDKs owners up to date after releasing new features. Otherwise it could lead us in situation when it's hard to identify why tags are different in different places of the project and a developer should investigate the issue (= waste of time). 

## Trailing closures

### What?
Avoid using trailing closures.

### Why?
The closure name can provide valuable information on how it should be used hence is better to have it than to remove it even though that means having extra code. Finally, you can't use the simplified version for all closures (or would like to), making the rule on when it's a good idea to use trailing closures complex and error prone.

### Example

#### Do
```swift
present(alert, animated: true, completion: {
    // .. do something
})
```

#### Don't
```swift
present(alert, animated: true) {
    // .. do something
}
```

## Naming

### What?
- Use `Kind` instead of `Type` when naming enums, structs, etc.
- Use `kind` instead of `type` when naming variable names unless it's actually to store and refer to Swift types.

### Why?
To keep consistency and avoid confusion since `Type` is a metatype in Swift. Read about metatypes [here]( https://docs.swift.org/swift-book/ReferenceManual/Types.html#).


# FinniversKit or FinnUI?
Should you add UI code to FinniversKit or FinnUI? 
- If it is to be used as a component and from many places it belongs in FinniversKit
- Is it to be used from the main app repo and it is a "feature" or has a single use (within forseeable future) it should go in FinnUI. If it later is supposed to be reused you can move it to FinniversKit.
- Is it to be used from another repository than the main app repo and it is a "feature" or has a single use (within forseeable future) it should go in go in that repository. If it later is supposed to be reused you can move it to FinniversKit.
