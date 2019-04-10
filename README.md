# PIDatePicker

⚠️ **This repository is no longer maintained or supported by the original author. However I've made the code compiling in Swift 5. Installation via Cocoapods will yield the old code, but using "pod install" inside the example project will work. To use in your own project, just copy the files from the Pod/Classes directory.** ⚠️

![PIDatePicker](https://raw.github.com/prolificinteractive/pidatepicker/master/Images/PIDatePicker.gif)

## Description
Partial implementation of a UIDatePicker object that allows design
customization of various user interface attributes such as font, color, etc.
This pod aims to replicate the default UIDatePicker functionality while adding
additional customization in the user interface.

Only supports picking the date, doesn't support other modes like date/time or
stopwatch.

## Customization

There are several options available for customizing your date picker:

| Property              | Type      | Description                                                                                                       |
|:----------------------|:----------|:------------------------------------------------------------------------------------------------------------------|
| font			        | UIFont    | Sets the font that the date picker will use to display the dates. By default, it uses a system font of size 15.   |
| textColor             | UIColor   | Set the color of the text. By default, it uses `UIColor.blackColor()`.                                            |
| backgroundColor       | UIColor   | Set the background color of the date picker. By default, it is a clear color.                                     |
| minimumDate 		    | UIDate    | The minimum selectable date allowed by the date picker. Defaults to `NSDate.distantPast()`.                       |
| maximumDate		    | UIDate    | The maximum selectable date allowed by the date picker. Defaults to `NSDate.distantFuture()`.                     |
| locale		        | NSLocale  | The locale of the calendar used for formatting the date. By default, this uses the device's locale.               |

The following public methods are available for calling in your module:

| Method                					| Description                                           |
|:------------------------------------------|:------------------------------------------------------|
| reloadAllComponents() 					| Reloads all of the components of the date picker.		|
| setDate(date: NSDate, animated: Bool)     | Sets the current date of the date picker.             |

## Delegate

A class can implement `PIDatePickerDelegate` and the following method to respond to changes in user selection.

```swift
func pickerView(pickerView: PIDatePicker, didSelectRow row: Int, inComponent component: Int)
```

## License

PIDatePicker is available under the MIT license. 


