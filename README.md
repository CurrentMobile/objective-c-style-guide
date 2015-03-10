ios-style-guide
===============

The MobileX Labs style guide for Objective-C/iOS development. 

Send in any improvements as pull requests and/or issues!

- Favor delegates over blocks for view elements.
- Put the space before the asterix (except for constants). e.g.

```objc
NSString *myString;
```
Not:

```objc
NSString* myString;
// or
NSString * myString;
 ```
- Put commas between property attributes. E.g.

```objc
@property (readonly, assign, nonatomic) MXLPullDownViewState viewState;
```
- Define all properties as readonly in the header, unless external readwrite access is required.
- Provide multi-line comment before each method definition. It should explain the method, then each parameter, then any returned result. Use the plugin [VVDocumenter](https://github.com/onevcat/VVDocumenter-Xcode) to automatically build this. E.g.

```objc
/**
 *  Calculates whether the the vertical distance from the top of
 *  the pulldown is significant enough to result in the cell
 *  being redrawn.
 * 
 *  @param offset The vertical distance in points to offset the content.
 *  @return A BOOL to indicate whether the cell should update, based on top offset.
 */
- (BOOL)shouldSetContentViewOffsetFromTop:(CGFloat)offset;

```

- Structure of constant names shuld be: ```kMXLClassNameConstantName```. E.g.

```objc
const CGFloat kMXLPullDownViewTabHeightDefault = 10;
```
- When setting float values, always append "f". E.g.:

```objc
CGFloat myFloat = 20.0f;
```
Not

```objc
CGFloat myFloat = 20;
```
- Put a space between the method scope (+/-) and return value. e.g.

```objc
- (void)myMethod;
```
- Use NS_ENUM for declaring typedefs. [Read here](http://nshipster.com/ns_enum-ns_options/).
- Typedef items should be structure: ```MXLTypeDefNameOptionName```, even if it doesn't read as well. For example:


```objc
typedef NS_ENUM(NSUInteger, MXLAppSwitcherStyle) {
    MXLAppSwitcherStyleOpen,
    MXLAppSwitcherStyleClosed
};

```
Not:


```objc
typedef NS_ENUM(NSUInteger, MXLAppSwitcherStyle) {
    MXLAppSwitcherOpenStyle,
    MXLAppSwitcherClosedStyle
};

```

- Favor dot-syntax over bracket-based message passing.
- All methods should be defined somewhere. Either publicly in the header, or privately as an interface extension in the .m file. The definition of the method is where the documenting comment should be located.
