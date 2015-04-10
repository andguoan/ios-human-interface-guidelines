# 适应性和布局

## 一切为了适应性

人们通常希望能在不同的地方使用他们最喜欢的 app。在 IOS8 及之后的版本中，通过定义屏幕的布局、视图控制器和会根据显示环境改变的视图（显示环境 display environment 是指整个屏幕或者屏幕的一部分，例如弹出框或分视图控制器的主视图部分），开发者可以使用尺寸类和自动布局技术来满足跨平台的适应性。

IOS 定义了两种尺寸类：常规和紧凑。常规尺寸类有着广阔的空间可用，而紧凑尺寸类对空间的使用有限制。为了突出显示环境的特点，你可以定义一个水平尺寸类和一个竖直尺寸类。正如你所想的，一个 IOS 设备可以使用横竖两种使用模式。

当一个显示环境改变时，IOS 可以自动改变成不同的布局。例如，当竖直尺寸从紧凑变为常规时，导航栏和工具栏会自动变长。

当你可以做到依靠尺寸类改变布局时，你的 app 会在不同的显示环境中有出色的表现。想学习如何在界面开发中使用尺寸类，请点击[Size Classes Design Help](https://developer.apple.com/library/ios/recipes/xcode_help-IB_adaptive_sizes/_index.html#//apple_ref/doc/uid/TP40014436)。

>**提示**
>在一种尺寸类中，你可以继续使用自动布局进行小的布局调整，例如拉伸和固定内容。

下面的例子可以帮助你理解尺寸类是如何在多种设备上突出显示环境的。例如，iPad 在不同方向上都使用常规尺寸，换句话说，iPad 的显示环境总是横版或竖版的常规尺寸。

水平样式

![](images/ipad_size_class_v_2x.png)

竖直样式

![](images/ipad_size_class_h_2x.png)

iPhone 的 显示环境会根据设备和方向的不同而变化。

![](images/iphone02_size_class_v_2x.png)

竖屏时，iPhone6 Plus 使用的是常规高度和紧凑宽度类型。

![](images/iphone02_size_class_h_2x.png)

横屏时，iPhone6 Plus 使用的是紧凑高度和常规宽度类型。

所有其他的 iPhone 设备，包括 iPhone 6，使用相同模式的尺寸。

![](images/iphone01_size_class_v_2x.png)

竖屏时，iPhone 6，iPhone 5 和 iPhone 4S 使用的是紧凑宽度和常规高度。

![](images/iphone01_size_class_h_2x.png)

横屏时，这些设备在宽高上使用的都是紧凑类型。


## 为每一种环境提供完美的体验

当你学会了利用适应性，你就可以保证你的 UI 会根据显示环境做出合理的变化。遵守这些指导，你的 app 就可以在所有设备的不同方向上给用户很好的体验。

**在所有环境下都要关注主体内容。**这是最重要的。人们使用你的 app 是为了看他们感兴趣的内容。如果在改变环境的同时，关注点也变化了，这会误导使用者并使他们感到对你的 app 失去了控制力。

**避免不必要的布局变化**当使用者改变设备方向或更换设备使用相同的 app 时，不同环境间的体验差异可以使用户维持他们的使用模式。例如，如果你在一个水平的常规环境下使用网格显示图片，那么在水平紧凑模式下，你就不必再显示相同的信息了，虽然你有可能调整了网格的尺寸。

**如果你的 app 只支持一个方向，请注意**人们期待可以在不同的方向上使用你的 app，你最好可以实现这个功能。但如果不能，请注意：

* **避免使用会暗示用户旋转设备的 UI 元件。**让应用清晰地运行在支持的方向下，这会让用户明白应该旋转设备，不要添加不必要的 UI 引起用户混乱。
* **支持多种方向。**例如，如果一个 app 只能水平运行，那么无论 home 键是在左边还是在右边，人们都应该可以使用。并且，如果人们在使用 app 时将设备旋转了 180 度，那么你 app 中的内容也最好可以旋转 180 度。

**如果你的 app 将设备的方向变化视为一种用户输入，那么就按照程序方式来处理旋转。**例如，一个需要用户通过转动设备来移动的游戏不能再对旋转屏幕而产生其他响应。在这种情况下，你应该支持这两种方向转换的方式并且允许用户切换这两种方式直到他们开始执行 app 的主体部分。一旦用户开始程序的主体内容，就使用程序方式来处理旋转。


## 通过使用布局交流
布局不仅仅意味着 app 界面的 UI 元素的样式。通过使用布局，你可以向你的用户展示什么是最重要的，他们的选择是什么，以及事情是如何联系起来的。

**强调重要的内容和功能易于使用户注意到 app 的主要任务。**有一些很好的方法可以做到这个，在屏幕靠近上边和左边的位置放置重要的项目。

![](images/focus_on_main_task_2x.png)

**使用图标或字体的大小与位置来表现屏幕中元素的相对重要性。**大图标会首先吸引人的关注，所以大图标会比小图标显得更重要。更大的图标也意味着更好点击，这在 app 中是十分有用的，例如通话和计时，这使得用户即使在嘈杂的环境中也能关注到。

![](images/phone_hangup_button_2x.png)

**使用对齐使阅读更舒服，让分组和层次间更有秩序。**对齐能使 app 看起来整洁、有组织，并且这可以使用户在滑动浏览时能关注重点。不同信息的缩进和对齐可以使用户明白内容间的联系，也会让查找特定内容变得简单。

**确保用户可以在默认尺寸下看到最重要的内容。**例如，用户不需要滑动屏幕就可以看到重要的内容和图像。

**做好变化文本大小的准备。**用户期盼大多数 app 都可以调整字体的大小到他们喜欢的尺寸。为了适应字体大小的变化，你也许需要调整布局。想查看更多关于字体调整的信息，请点击[Text Should Always Be Legible](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/ColorImagesText.html#//apple_ref/doc/uid/TP40006556-CH58-SW3)

**尽量避免 UI 图形的不一致性。**在一般情况下，功能相似的图标看起来也很像。当你的图标不太相似时，用户会认为这一定是有原因的，并且会想尽办法知道为什么。

**给每个需要交互的图标足够的空间，从而简化用户的操作。**常用的可点击的控件大小是 44 x 44 点。

推荐样式

![](images/interact_with_content_r_2x.png)

不推荐样式

![](images/interact_with_content_nr_2x.png)