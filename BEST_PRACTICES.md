# Dos and don'ts

## Simplified closure syntax

### What
Use the simplified closure syntax when possible. 

### Reasoning
We avoid adding code that is not needed the same way we don't use semicolons or `internal`.

### Example

#### Do
```swift
present(alert, animated: true) {
    // .. do something
}
```


#### Don't
```swift
present(alert, animated: true, completion: {
    // .. do something
}
```
