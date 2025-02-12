# YAPlacePicker

[![CI Status](https://img.shields.io/travis/7633277@gmail.com/YAPlacePicker.svg?style=flat)](https://travis-ci.org/7633277@gmail.com/YAPlacePicker)
[![Version](https://img.shields.io/cocoapods/v/YAPlacePicker.svg?style=flat)](https://cocoapods.org/pods/YAPlacePicker)
[![License](https://img.shields.io/cocoapods/l/YAPlacePicker.svg?style=flat)](https://cocoapods.org/pods/YAPlacePicker)
[![Platform](https://img.shields.io/cocoapods/p/YAPlacePicker.svg?style=flat)](https://cocoapods.org/pods/YAPlacePicker)

![](preview.gif)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first. Also you need to provide APIKEY inside ViewController.

## Requirements

You need to have APIKEY for Google Maps and Google Places. If you don't have it please check here: https://developers.google.com/maps/documentation/ios-sdk/get-api-key

## How to use?

Add this to Info.plist

```xml
<key>NSLocationWhenInUseUsageDescription</key>
<string>Your location is required to see places close to you</string>
```
Add this code where you want YAPlacePicker to be opened

```swift

//baseVC - UIViewController from which you want to open YAPlacePicker

YAPlacePickerBuilder(baseVC: self, gmsApiKey: ".........", completion: { place in
print(place)
}).show()
```

Available customizations (Optional)

```swift
YAPlacePickerBuilder(baseVC: self, gmsApiKey: ".........", completion: { place in
print(place)
})
.searchPlaceholder("Please start typing")
.chooseButtonTitle("Choose")
.chooseButtonColor(UIColor.red)
.show()
```

## Installation

YAPlacePicker is available through [CocoaPods](https://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'YAPlacePicker'
```

## Author

Nikita Khudorozhkov, 7633277@gmail.com

## License

YAPlacePicker is available under the MIT license. See the LICENSE file for more info.

## Contribute

Please feel free to contribute with improvements.
