# Validator-Swift

Simple Swift Validator 

Allows you to check if some `String` compare to `ValidatorRule` you created by adding `validated(with: ValidatorRule)` extension to `String`.

Usage example

```swift
  let word = "word"
  var dynamicWord = "dynamic"
  let dynamicRule = ValidatorRulePattern(dynamicString: {return dynamicWord})
  let result = word.validated(with: dynamicRule)
  switch result {
  case .invalid(let error):
    print(error)
  case .valid:
    print("valid")
  }
```
