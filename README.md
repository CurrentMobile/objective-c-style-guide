ios-style-guide
===============

The MobileX Labs style guide for Objective-C/iOS development. 

Send in any improvements as pull requests and/or issues!

- Favor delegates over blocks for view elements.
- Put the space before the asterix (except for constants). e.g.

```
NSString *myString;
```
Not:

```
NSString* myString;
// or
NSString * myString;
 ```
- Put commas between property attributes. E.g.

```
@property (readonly, assign, nonatomic) MXLPullDownViewState viewState;
```
- Define all properties as readonly in the header, unless external readwrite access is required.
- Provide multi-line comment before each method definition. It should explain the method, then each parameter, then any returned result. E.g.

```
/**
    Sets the vertical distance in points from the top of the pulldown to 
    the content display.
 
    @param offset
    The vertical distance in points to offset the content.
 */
- (void)setContentViewOffsetFromTop:(CGFloat)offset;

```

- Structure of constant names shuld be: ```kMXLClassNameConstantName```. E.g.

```
const CGFloat kMXLPullDownViewTabHeightDefault = 10;
```
- When setting float values, always append "f". E.g.:

```
CGFloat myFloat = 20.0f;
```
Not

```
CGFloat myFloat = 20;
```
- Put a space between the method scope (+/-) and return value. e.g.

```
- (void)myMethod;
```
- Use NS_ENUM for declaring typedefs. [Read here](http://nshipster.com/ns_enum-ns_options/).
- Typedef items should be structure: ```MXLTypeDefNameOptionName```, even if it doesn't read as well. For example:


```
typedef NS_ENUM(NSUInteger, MXLAppSwitcherStyle) {
    MXLAppSwitcherStyleOpen,
    MXLAppSwitcherStyleClosed
};

```
Not:


```
typedef NS_ENUM(NSUInteger, MXLAppSwitcherStyle) {
    MXLAppSwitcherOpenStyle,
    MXLAppSwitcherClosedStyle
};

```