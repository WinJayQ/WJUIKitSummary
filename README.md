# WJUIKitSummary
#UIKit的外观属性及方法汇总
  
  转自楚天舒的简书-->http://www.jianshu.com/p/3a4353339822
  
  开发中经常会碰到要设置UI的某个生僻的外观属性，虽然在头文件中都能查到，但一是每个控件的头文件比较分散繁杂，二是每个头文件里有太多不用到的方法和属性，所以这里将UIKit的外观属性及方法从头文件中抽取出来，以便查找及熟悉。（更新到iOS 8.0，从A-Z排序）
##UIActivityIndicatorView
@property (readwrite, nonatomic, retain) UIColor *color NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

##UIBarButtonItem
// 背景图片相关
- (UIImage *)backgroundImageForState:(UIControlState)state barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
- (void)setBackgroundImage:(UIImage *)backgroundImage forState:(UIControlState)state style:(UIBarButtonItemStyle)style barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;
- (UIImage *)backgroundImageForState:(UIControlState)state style:(UIBarButtonItemStyle)style barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

- (void)setBackgroundVerticalPositionAdjustment:(CGFloat)adjustment forBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR; 
- (CGFloat)backgroundVerticalPositionAdjustmentForBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (void)setTitlePositionAdjustment:(UIOffset)adjustment forBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
- (UIOffset)titlePositionAdjustmentForBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

// 返回键 ：图片、文字
- (void)setBackButtonBackgroundImage:(UIImage *)backgroundImage forState:(UIControlState)state barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
- (UIImage *)backButtonBackgroundImageForState:(UIControlState)state barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (void)setBackButtonTitlePositionAdjustment:(UIOffset)adjustment forBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
- (UIOffset)backButtonTitlePositionAdjustmentForBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (void)setBackButtonBackgroundVerticalPositionAdjustment:(CGFloat)adjustment forBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR; 
- (CGFloat)backButtonBackgroundVerticalPositionAdjustmentForBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

##UIBarItem
// 标题富文本
- (void)setTitleTextAttributes:(NSDictionary *)attributes forState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
- (NSDictionary *)titleTextAttributesForState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

##UIButton
// 内边缘间距

@property(nonatomic) UIEdgeInsets contentEdgeInsets UI_APPEARANCE_SELECTOR; // default is UIEdgeInsetsZero

// 标题颜色、阴影颜色、背景图片
- (void)setTitleColor:(UIColor *)color forState:(UIControlState)state UI_APPEARANCE_SELECTOR; // default if nil. use opaque white
- (void)setTitleShadowColor:(UIColor *)color forState:(UIControlState)state UI_APPEARANCE_SELECTOR; // default is nil. use 50% black
- (void)setBackgroundImage:(UIImage *)image forState:(UIControlState)state UI_APPEARANCE_SELECTOR; // default is nil

##UINavigationBar
@property(nonatomic,retain) UIColor *barTintColor NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR; // default is nil

// 背景图片相关 - 默认是张白色图片
- (void)setBackgroundImage:(UIImage *)backgroundImage forBarPosition:(UIBarPosition)barPosition barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;
- (UIImage *)backgroundImageForBarPosition:(UIBarPosition)barPosition barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;
- (void)setBackgroundImage:(UIImage *)backgroundImage forBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
- (UIImage *)backgroundImageForBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

// 阴影图片 - 即分割线

@property(nonatomic,retain) UIImage *shadowImage NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic,copy) NSDictionary *titleTextAttributes NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

// 
- (void)setTitleVerticalPositionAdjustment:(CGFloat)adjustment forBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
- (CGFloat)titleVerticalPositionAdjustmentForBarMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

// 
@property(nonatomic,retain) UIImage *backIndicatorImage NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;
@property(nonatomic,retain) UIImage *backIndicatorTransitionMaskImage NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;

##UIPageControl
// 分页小圆点颜色

@property(nonatomic,retain) UIColor *pageIndicatorTintColor NS_AVAILABLE_IOS(6_0) 
UI_APPEARANCE_SELECTOR;

@property(nonatomic,retain) UIColor *currentPageIndicatorTintColor NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

##UIProgressView
@property(nonatomic, retain) UIColor* progressTintColor NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic, retain) UIColor* trackTintColor NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic, retain) UIImage* progressImage NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic, retain) UIImage* trackImage NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

##UIRefreshControl
@property (nonatomic, retain) NSAttributedString *attributedTitle UI_APPEARANCE_SELECTOR;

##UISearchBar
@property(nonatomic,retain) UIColor *barTintColor NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR; // default is nil

@property(nonatomic,retain) UIImage *backgroundImage NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic,retain) UIImage *scopeBarBackgroundImage NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic) UIOffset searchFieldBackgroundPositionAdjustment NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic) UIOffset searchTextPositionAdjustment NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (void)setPositionAdjustment:(UIOffset)adjustment forSearchBarIcon:(UISearchBarIcon)icon NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;- (UIOffset)positionAdjustmentForSearchBarIcon:(UISearchBarIcon)icon NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

//
- (void)setBackgroundImage:(UIImage *)backgroundImage forBarPosition:(UIBarPosition)barPosition barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR; // Use UIBarMetricsDefaultPrompt to set a separate backgroundImage for a search bar with a prompt

- (UIImage *)backgroundImageForBarPosition:(UIBarPosition)barPosition barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;


- (void)setSearchFieldBackgroundImage:(UIImage *)backgroundImage forState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (UIImage *)searchFieldBackgroundImageForState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;


- (void)setImage:(UIImage *)iconImage forSearchBarIcon:(UISearchBarIcon)icon state:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (UIImage *)imageForSearchBarIcon:(UISearchBarIcon)icon state:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;


- (void)setScopeBarButtonBackgroundImage:(UIImage *)backgroundImage forState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR; 

- (UIImage *)scopeBarButtonBackgroundImageForState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;


- (void)setScopeBarButtonDividerImage:(UIImage *)dividerImage forLeftSegmentState:(UIControlState)leftState rightSegmentState:(UIControlState)rightState NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (UIImage *)scopeBarButtonDividerImageForLeftSegmentState:(UIControlState)leftState rightSegmentState:(UIControlState)rightState NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;


- (void)setScopeBarButtonTitleTextAttributes:(NSDictionary *)attributes forState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (NSDictionary *)scopeBarButtonTitleTextAttributesForState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

##UISegmentedControl
// 背景图片
- (void)setBackgroundImage:(UIImage *)backgroundImage forState:(UIControlState)state barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR; 

- (UIImage *)backgroundImageForState:(UIControlState)state barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

//分割线图片 
- (void)setDividerImage:(UIImage *)dividerImage forLeftSegmentState:(UIControlState)leftState rightSegmentState:(UIControlState)rightState barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (UIImage *)dividerImageForLeftSegmentState:(UIControlState)leftState rightSegmentState:(UIControlState)rightState barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

// 文字富文本
- (void)setTitleTextAttributes:(NSDictionary *)attributes forState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (NSDictionary *)titleTextAttributesForState:(UIControlState)state NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

// 位置相关
- (void)setContentPositionAdjustment:(UIOffset)adjustment forSegmentType:(UISegmentedControlSegment)leftCenterRightOrAlone barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

 - (UIOffset)contentPositionAdjustmentForSegmentType:(UISegmentedControlSegment)leftCenterRightOrAlone barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

##UISlider
// 已滑过的线颜色

@property(nonatomic,retain) UIColor *minimumTrackTintColor NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
// 未滑过线颜色

@property(nonatomic,retain) UIColor *maximumTrackTintColor NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;
// 滑动圆片颜色

@property(nonatomic,retain) UIColor *thumbTintColor NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

##UIStepper
// 背景图片
- (void)setBackgroundImage:(UIImage*)image forState:(UIControlState)state NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

- (UIImage*)backgroundImageForState:(UIControlState)state NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

// 分割图片
- (void)setDividerImage:(UIImage*)image forLeftSegmentState:(UIControlState)leftState rightSegmentState:(UIControlState)rightState NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

- (UIImage*)dividerImageForLeftSegmentState:(UIControlState)state rightSegmentState:(UIControlState)state NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

// 增加部分
- (void)setIncrementImage:(UIImage *)image forState:(UIControlState)state NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

- (UIImage *)incrementImageForState:(UIControlState)state NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

// 减少部分
- (void)setDecrementImage:(UIImage *)image forState:(UIControlState)state NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

- (UIImage *)decrementImageForState:(UIControlState)state NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

##UISwitch
@property(nonatomic, retain) UIColor *onTintColor NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic, retain) UIColor *thumbTintColor NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic, retain) UIImage *onImage NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic, retain) UIImage *offImage NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

##UITabBar
@property(nonatomic,retain) UIColor *barTintColor NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR; // default is nil

@property(nonatomic,retain) UIColor *selectedImageTintColor NS_DEPRECATED_IOS(5_0,8_0,"Use tintColor") UI_APPEARANCE_SELECTOR;

@property(nonatomic,retain) UIImage *backgroundImage NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic,retain) UIImage *selectionIndicatorImage NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR; 

@property(nonatomic,retain) UIImage *shadowImage NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic) UITabBarItemPositioning itemPositioning NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic) CGFloat itemWidth NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic) CGFloat itemSpacing NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;

@property(nonatomic) UIBarStyle barStyle NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR;

##UITabBarItem
- (void)setTitlePositionAdjustment:(UIOffset)adjustment NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (UIOffset)titlePositionAdjustment NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

##UITableView
@property (nonatomic) UIEdgeInsets separatorInset NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR; // allows customization of the frame of cell separators

@property (nonatomic, retain) UIColor *sectionIndexColor NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR; // color used for text of the section index

// 索引条背景图片

@property (nonatomic, retain) UIColor *sectionIndexBackgroundColor NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR; // the background color of the section index while not being touched

@property (nonatomic, retain) UIColor *sectionIndexTrackingBackgroundColor NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR; // the background color of the section index while it is being touched

// 分割线 - 实际上是高度1颜色浅灰的UIView

@property (nonatomic, retain) UIColor *separatorColor UI_APPEARANCE_SELECTOR; // default is the standard separator gray

// 

@property (nonatomic, copy) UIVisualEffect *separatorEffect NS_AVAILABLE_IOS(8_0) UI_APPEARANCE_SELECTOR; // effect to apply to table separators

##UITableViewCell
@property (nonatomic) UIEdgeInsets separatorInset NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR; // allows customization of the separator frame

##UIToolBar
@property(nonatomic,retain) UIColor *barTintColor NS_AVAILABLE_IOS(7_0) UI_APPEARANCE_SELECTOR; // default is nil

- (void)setBackgroundImage:(UIImage *)backgroundImage forToolbarPosition:(UIBarPosition)topOrBottom barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (UIImage *)backgroundImageForToolbarPosition:(UIBarPosition)topOrBottom barMetrics:(UIBarMetrics)barMetrics NS_AVAILABLE_IOS(5_0) UI_APPEARANCE_SELECTOR;

- (void)setShadowImage:(UIImage *)shadowImage forToolbarPosition:(UIBarPosition)topOrBottom NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

- (UIImage *)shadowImageForToolbarPosition:(UIBarPosition)topOrBottom NS_AVAILABLE_IOS(6_0) UI_APPEARANCE_SELECTOR;

##UIView
@property(nonatomic,copy) UIColor *backgroundColor UI_APPEARANCE_SELECTOR; // default is nil. Can be useful with the appearance proxy on custom UIView subclasses.
