# Cepheus
A powerful watchOS full-keyboard.

![:name](https://count.getloli.com/get/@Garden785-Cepheus?theme=rule34)

As the release of Apple Watch Series 7, full-keyboard seems to be quite useless. But old series such as Series 5 or SEs are still unable to type freely.

We developed Cepheus, allowing all users to type with a full-keyboard.

## Features
- Basics
  - Able to enter Latin letters, Arabic letters and symbols.
  - Elegant interface makes Cepheus beauty while still useful.
  - Supports Shift & Caps Lock key which allows capital letters to be typed in.
- Emojis
  - Review in lists that helps preview to be quick.
  - Review in groups and subgroups helps users to find the emoji simply.
  - Recent Usage are collected and can be easily accessed.
  - Text field also editable when emoji keyboard is displayed.
- Chinese Pinyin
  - Around 8,453 characters collected for pinyin type-in.
  - Safe Insert make sure indexes will not be out of arrays.
  - Input ignorable allows users to type in Latin letters.
  - Full-sized chinese punctuations are supported in keyboard.

## Parameters
```swift

    public var titleKey: LocalizedStringKey
    public var text: Binding<String>
    public var isSecure = false
    public var inputMethods: [CepheusInputMethods] = CepheusInputMethods.allCases
    public var allowEmojis = true
    public var onSubmit: () -> Void = {}
CepheusKeyboard("Email Address", text: $text, isSecure: false, inputMethods: [.english], allowEmojis: false, onSubmit: {
    print("Email address submitted")
})
```

### titleKey
`_: LocalizedStringKey` tells users what the text field is.

### text
`text: Binding<String>` indicates what the input text is.

### isSecure
`isSecure: Bool` indicates if the keyboard is used for typing privacy-sensitive contents.

When set to `true`, the keyboard will goes like `secureField`. `allowEmojis` is ignored and will always not allow emojis.

Default as `false`.

### inputMethods
`inputMethods: [CepheusInputMethods]` defines what input methods can be used.

There is only two values, `.english` and `.chinesePinyin`.

Default as `CepheusInputMethods.allCases`.

### allowEmojis
`allowEmojis: Bool` indicates if emojis are allowed.

Default as `true`.

### onSubmit
`onSubmit: () -> Void` receives actions and will be run when Confirm is pressed.

This acts like `onSubmit` in the native SwiftUI.

Default as `{}`.


## Requirements
### Declarement
You are responsible for adding one of the following description to your app, where ever it is as long as it could be found.

Just one of them.

> Powered by Cepheus

> Powered by Qastor Cepheus

If Cepheus is unable to be enabled, such as watchOS 9, then this text could be removed.

### About
`CepheusSettingsView()` could be called simply. We recommend to put this somewhere in the your app settings.

This is optional, which means you could not show this. 

`CepheusCreditView()` is also available if you wanted to call it.

We do not wish you to remove credit from the source code. (*You could remove if you really wanna do that.*)

## Other Available Structures
### CepheusSettingsView
`CepheusEnablingToggle: View` is the same view as where the "about" link in the language sheet takes you to.


## Credits
**ThreeManager785**
- Develop
- Data Collection
- Design

**WindowsMEMZ**
- Chinese Dictionary Sorting
- Debug
- Inspiration

**Linecom**
- Feedbacks

**Captain Log**
- Chinese Character List in Frequency
> 转自船长日志, 本文链接地址: http://www.cslog.cn/Content/word-frequency-list-of-chinese/

**Every Developer & User**
- Really appreaciate for every developer supporing Cepheus, thank you for your patient reading README and using Cepheus.
- And appreaciate for users, which gives me confident to do development further. 

## Privacy
Cepheus collects emojis that are recently used and could be turned off manually.

No any other datas are collected. No data are shared or uploaded to neither other devices nor the Internet.

Cepheus won't be able to know what you've typed.

## Links

https://youtu.be/KvmheS6RhJw

https://www.bilibili.com/video/BV1aw4m1X7m9/?spm_id_from=..search-card.all.click&vd_source=56037b56048bedd71c28cd497f5de805

