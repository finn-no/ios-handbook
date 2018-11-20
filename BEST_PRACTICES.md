# Dos and don'ts

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
}
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
