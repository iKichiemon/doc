# Tips for iOS

## only INTERFACE_BUILDER

```
class View: UIView {
  #if TARGET_INTERFACE_BUILDER
  override func prepareForInterfaceBuilder() {
      super.prepareForInterfaceBuilder()
      // do something
  }
  #endif
    
  override func awakeFromNib() {
      super.awakeFromNib()
      // do something
  }
}
```







