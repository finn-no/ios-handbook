# Dos and don'ts

## Libraries/SDKs versioning

### MAJOR.MINOR.PATCH
When making a new release/version keep in mind how to update the version number. It is very important to be aware of if the change is a major/breaking change or not to avoid wasting other developers time as they try to figure out why the build breaks.
- Major: The change you are making is a breaking change, meaning that "users" of it can't update without also making code changes.
- Minor: You added something new or updated something but it does not require code changes.
- Patch: Fix for a bug or error in a way that is internal to the library/SDK.

## Working process guide
After merging a PR to master, please don't forget to make a new release. There should be a script to do this (`bundle exec fastlane`), never update version numbers inside a PR because you can't be sure of the order PRs get merged when creating them.

#### Breaking changes
When you do a breaking change the "users" of that repo should be updated ASAP. The recommended approach is to open PRs on those repositories as well and wait for all of them to be approved before merging and making a new major release.

#### Minor/patch changes 
If you will be following up with more PRs you can wait and make a new minor/patch release after they are all merged, provided you know that no one else will make changes in the meanwhile. Do not forget to update ios-app (or other "owners") after making the new version. If you will/can not do this directly leave a note of it in the PR you closed.

### Why?
All releases should be done automatically to avoid breaking team's release guidelines. Also it is very important to keep all tags inside all SDKs "users" up to date after releasing new features. Otherwise it could lead us in situation when it's hard to identify why tags are different in different places of the project and a developer needs to investigate the issue (= waste of time). 

## Trailing closures

### What?
Avoid using trailing closures if the closure name can provide valuable information on how it should be used.

### Why?
If closure name provides valuable information on how it should be used it is better to have it than to remove it - even though that means having extra code. 

### Example

#### Do
```swift
present(alert, animated: true, runBeforeAnimation: {
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
