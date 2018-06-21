# SWKit
快速开发APP的工具

## 通用
```
extern CGFloat SCREEN_WIDTH;
extern CGFloat SCREEN_HEIGHT;
extern CGSize  SCREEN_SIZE;
extern CGRect  SCREEN_FRAME;
extern CGPoint SCREEN_CENTER;

```
## 快速创建UI
```
/**label 背景色 字体颜色 对齐方式 行数 字体大小 文字*/
+(UILabel *)labelWithBackgroundColor:(UIColor *)backgrountColor textColor:(UIColor *)textColor textAlignment:(NSTextAlignment)textAlignment numberOfLines:(NSInteger)numberOfLines fontSize:(float) size font:(UIFont *)font text:(NSString *)text;

/**textField 背景色 字体颜色 是否密文 字体大小 文字 默认文字 文字对齐方式*/
+(UITextField *)textFieldWithBackgroundColor:(UIColor *)backgrountColor textColor:(UIColor *)textColor secureTextEntry:(BOOL)secureTextEntry fontSize:(float)size font:(UIFont *)font text:(NSString *)text placeholder:(NSString *)placeholder textAlignment:(NSTextAlignment)textAlignment;

/**textView 背景色 字体颜色 字体大小 文字 文字对齐方式*/
+(UITextView *)textViewWithBackgroundColor:(UIColor *)backgrountColor textColor:(UIColor *)textColor fontSize:(float)size font:(UIFont *)font text:(NSString *)text  textAlignment:(NSTextAlignment)textAlignment;

/**UIButton 背景色 默认文字颜色 默认文字 选中文字颜色 选中文字 字体大小 默认背景图片 选中背景图片 图片 选中图片*/
+(UIButton *)buttonWithBackgroundColor:(UIColor *)backgrountColor titleColorForNormal:(UIColor *)titleColorForNormal titleForNormal:(NSString *)titleForNormal titleForSelete:(NSString *)titleForSelete titleColorForSelete:(UIColor *)titleColorForSelete  fontSize:(float)size font:(UIFont *)font backgroundImageForNormal:(NSString *)backgroundImageForNormal backgroundImageForSelete:(NSString *)backgroundImageForSelete imageForNormal:(NSString *)imageForNormal imageForSelete:(NSString *)imageForSelete;


/**UIButton 默认文字颜色 默认文字 选中文字颜色 选中文字 字体大小 默认背景图片 选中背景图片*/
+(UIButton *)buttonWithTitleColorForNormal:(UIColor *)titleColorForNormal titleForNormal:(NSString *)titleForNormal titleForSelete:(NSString *)titleForSelete titleColorForSelete:(UIColor *)titleColorForSelete  fontSize:(float)size font:(UIFont *)font backgroundImageForNormal:(NSString *)backgroundImageForNormal backgroundImageForSelete:(NSString *)backgroundImageForSelete;

/**UIButton 背景色 默认文字颜色 默认文字 选中文字颜色 选中文字 字体大小 图片 选中图片*/
+(UIButton *)buttonWithBackgroundColor:(UIColor *)backgrountColor titleColorForNormal:(UIColor *)titleColorForNormal titleForNormal:(NSString *)titleForNormal titleForSelete:(NSString *)titleForSelete titleColorForSelete:(UIColor *)titleColorForSelete  fontSize:(float)size font:(UIFont *)font imageForNormal:(NSString *)imageForNormal imageForSelete:(NSString *)imageForSelete;

/**UIButton 背景色 默认文字颜色 默认文字 选中文字颜色 选中文字 字体大小*/
+(UIButton *)buttonWithBackgroundColor:(UIColor *)backgrountColor titleColorForNormal:(UIColor *)titleColorForNormal titleForNormal:(NSString *)titleForNormal titleForSelete:(NSString *)titleForSelete titleColorForSelete:(UIColor *)titleColorForSelete  fontSize:(float)size font:(UIFont *)font;

/**UIButton 默认背景图片 选中背景图片*/
+(UIButton *)buttonWithBackgroundImageForNormal:(NSString *)backgroundImageForNormal backgroundImageForSelete:(NSString *)backgroundImageForSelete;

/**UIButton 背景色 图片 选中图片*/
+(UIButton *)buttonWithBackgroundColor:(UIColor *)backgrountColor imageForNormal:(NSString *)imageForNormal imageForSelete:(NSString *)imageForSelete;


/**快速创建文字按钮 */
+ (UIButton *)buttonWithTitle:(NSString *)title titleColor:(UIColor *)normalColor hilightedColor:(UIColor *)hilightedColor fontSize:(CGFloat)fontSize frame:(CGRect)frame;

/**快速创建图片按钮 */
+ (UIButton *)buttonWithImage:(UIImage *)image hilightedImage:(UIImage *)hilightedImage frame:(CGRect)frame;

/**UIImageView 背景色 是否可触摸 图片名字*/
+(UIImageView *)imageViewWithBackgroundColor:(UIColor *)backgrountColor userInteractionEnabled:(BOOL)userInteractionEnabled imageName:(NSString *)imageName;

/**UIImageView 背景色 是否可触摸 图片*/
+(UIImageView *)imageViewWithBackgroundColor:(UIColor *)backgrountColor userInteractionEnabled:(BOOL)userInteractionEnabled image:(UIImage *)image;

/**UIScrollView 背景色 是否可滑动 容量大小 是否可翻页滑动 是否显示横向滑动条 是否显示竖向滑动条*/
+(UIScrollView *)scrollViewWithBackgroundColor:(UIColor *)backgrountColor scrollEnabled:(BOOL)scrollEnabled contentSize:(CGSize)size pagingEnabled:(BOOL)pagingEnabled showsHorizontalScrollIndicator:(BOOL)showsHorizontalScrollIndicator showsVerticalScrollIndicator:(BOOL)showsVerticalScrollIndicator;

/**UITableView 背景色 是否可滑动 cell分割样式*/
+(UITableView *)tableViewWithBackgroundColor:(UIColor *)backgrountColor scrollEnabled:(BOOL)scrollEnabled separatorStyle:(UITableViewCellSeparatorStyle)separatorStyle;

/**UICollectionView 背景色 是否可滑动 item大小 滚动方向 四周边距 item之间间距 行距 自定义cell的class identifier*/
+(UICollectionView *)collectionViewWithBackgroundColor:(UIColor *)backgrountColor scrollEnabled:(BOOL)scrollEnabled itemSize:(CGSize)size scrollDirection:(UICollectionViewScrollDirection)scrollDirection sectionInset:(UIEdgeInsets)sectionInset minimumInteritemSpacing:(float)minimumInteritemSpacing minimumLineSpacing:(float)minimumLineSpacing cellClass:(NSString *)cellClass identifier:(NSString *)identifier;

//切圆角
+(UIView *)ViewcornerRadius:(float)radius andColor:(UIColor *)color andWidth:(float)width :(UIView *)view;

```
## 设备有关
```

//获取系统版本
+ (CGFloat)systemVersion;
//当前手机是否支持PhotoKit照片库框架
+ (BOOL)canUsePhotiKit;
//拨打电话
+ (void)callPhoneNumber:(NSString *)phone;
//复制字符串到系统剪贴板
+ (void)copyToPasteboard:(NSString *)string;
//获取APP 名称
+ (NSString *)appName;
//获取APP Scheme
+ (NSString *)getApplicationScheme;
//设置网络活动指示符可见(导航栏旋转图标)
+ (void)setNetworkActivityIndicatorVisible:(BOOL)visible;
//保存图片到系统相册
+ (void)saveImageToPhotoAlbum:(UIImage *)image;
//保存视频到系统相册
+ (void)saveVideoToPhotoAlbum:(NSString *)videoPath;
//设备型号名称
+ (NSString *)deviceModelName;
//获取根视图
+ (UIViewController *)rootViewController;
//获取window
+ (UIWindow *)currentWindow;
//可获取window并且添加showInWidow弹窗
+ (UIWindow *)popOverWindow;
//获取当前控制器所在
+ (UIViewController *)getCurrentVC;
//添加一个View到Window
+ (void)addViewToPopOverWindow:(UIView *)view;
//从window移除View
+ (void)removeViewFromPopOverWindow:(UIView *)view;
//获取Appdelegate
+ (AppDelegate *)appDelegate;
//获取当前View所在的控制器
+ (UIViewController *)viewControllerForView:(UIView *)view;
//移除控制器上所有的子视图以及其他控制器
+ (void)removeViewControllerFromParentViewController:(UIViewController *)viewController;
//开始观察runloop
+ (void)startObserveRunLoop;
//开始停止runloop
+ (void)stopObserveRunLoop;


```



