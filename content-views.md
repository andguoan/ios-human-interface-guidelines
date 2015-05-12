#内容视图 - Content Views
##活动菜单 - Activity 
每个活动菜单表示一个系统提供的服务或定制服务——它可以通过访问活动视图控制器(Activity view controller)来作用于某些特定的内容。

 
>提示   
想要了解如何在代码中定义标签栏，请参考[UIActivity Class Reference](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/check_2x.png).
想要了解如何把一个活动视图控制器添加到应用程序中，请参考[Activity View Controller](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH13-SW121).
行动和共享的扩展也在活动视图控制器中显示。要了解关于这些扩展更多的信息，请参考[Share and Action Extensions](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW3). 
 
活动菜单：
-	是指一种代表当前应用所支持服务的对象。
-	由一种类似于按钮的图标来表示。  
 
用户通常通过点击控制器中的活动图标来启动某样活动。点击之后该项服务通常会立刻执行，除非这项服务过于复杂，此时系统将会进一步索取更多的信息之后才会为用户执行该服务。
使用活动菜单来让用户执行你的应用所提供的服务。请注意，iOS 本身提供了若干内置的服务和应用扩展，如打印，转发到 Twitter，发送信息和 Airplay 等等，你不需要再另外创建它们。
为你应用的各种服务设计一套精简的模版图标(Template image)。模板是iOS使用的一种形象，来创建最后用户看到的图标。如果想制作出好看的模版图标，设计的时候可以遵循以下原则：
-	使用透明度适当的黑色或白色
-	不要使用阴影
-	进行抗锯齿处理  

一个活动模版图大小应该保持在70×70像素左右(高分辨率下)，在区域里居中显示。  
为每一个活动菜单设计清晰简练的文字标题。标题将会出现在活动菜单图标的下方。短标题通常效果最好，因为它在屏幕上的显示效果更好并且更容易本地化。如果你的标题文字过长，iOS会将缩小文本，仍然过长的话则会被截断。一般而言，最好能避免在活动标题中提及你的公司或产品名称。

##活动视图控制器 - Activity View Controller 
活动视图控制器是一个临时视图，当中罗列了一系列可以针对页面特定内容的系统服务和自定义服务。  

>提示  
想要了解如何在代码中定义活动视图控制器，请参考[UIActivityView Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIActivityViewController_Class/index.html#//apple_ref/doc/uid/TP40011976).想要知道怎么设计一个提供用户服务的活动菜单，请参考[Activity](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIActivityViewController_Class/index.html#//apple_ref/doc/uid/TP40011976). 

活动视图控制器: 
-	显示一个可配置的任务列表,用户可以执行指定的内容
-	可以根据环境发出某一个动作  

**使用活动视图控制器来为用户提供一系列针对当前内容的服务。**这些服务可以是系统自带的，比如复制，分享到twitter，打印等等，也可以是自定义的。活动视图控制器通常用作让用户把他们选中的内容复制到他们的社交媒体账户上。  
**不要创建一个自定义按钮来触发活动视图控制器。**用户更习惯点击分享按钮后使用系统提供的服务。你应该学会如何更好地利用用户这一既定习惯，而不是强迫他们以一种全新的方式来完成同样的事情。  
**确保控制器中的操作适用于当前场景。**你可以适当地在活动视图控制器中增减系统操作，或增加自定义操作。例如，如果你不希望用户打印某张图片，你可以把打印功能从活动视图控制器中删除。  
>注意  
你不能改变系统默认服务在活动图像控制器中的顺序。同时，所有系统服务都应出现在自定义服务之前。

##集合视图 - Collection View 
集合视图用于管理一系列有序的项，并以一种自定义的布局来呈现它们。  
 
>提示   
想要了解如何在代码中定义集合视图，请参考[Collection View Programming Guide for iOS](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/CollectionViewPGforIOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40012334).  

集合视图: 
-	可以包含可选视图视觉上区分的项目子集或提供装饰用品，如自定义背景
-	支持布局之间的自定义动画的过渡 （默认情况下，当用户插入、 移动或删除的项目集合视图提供动画）
-	支持手势识别器来执行自定义操作的加法。默认情况下，集合视图可选择和编辑相关项目。  

**使用集合视图来让用户查看和操作一系列不适合以列表形式呈现的项。**由于集合视图的布局不是一个严格的线性布局，因此尤其适合用来展示一些尺寸不一致的项。
**集合视图支持广泛的自定义，因此我们要尽量避免把心思都放在进行全新的设计上。**集合视图是用来帮助用户更好地完成任务的，视图本身并不是用户体验的焦点所在。以下指导会帮你创建人们喜爱的集合视图。  
**可以使用表格视图(Table View)的时候，不要使用集合视图。**有时候用户会觉得以列表呈现的信息更容易阅读和理解，例如将文本信息放在滚动列表中滚动列表中的时候，用户阅读和处理起来会更为简单和高效。  
**让视图中的项更容易点击。**如果用户很难点中集合视图中的项，他们是不会愿意用你的应用的。跟所有用户可以点击的UI对象一样，请确保你的集合视图中每一个项的最小点击区域有44×44pt，尤其是在iPhone上。  
**当你要让整个布局进行动态变化时，请务必谨慎。**集合视图允许你在用户浏览和操作项的时候调整视图的布局。但当你决定调整它的时候，请确保这个动态变化是有意义并且容易理解的。没有明确目的而贸然改变集合视图的布局会让用户对应用留下难用、不符合预期等负面的印象。更有甚者，如果用户此时关注的项在变化中消失了，用户会觉得这个应用超出了他们的控制能力。  

##容器视图控制器 - Container View Controller
容器视图控制器采用自定义的方式来管理和呈现它的视图控制器或一系列子视图。系统定义的容器视图控制器包括标签栏视图控制器([Tab bar view controller](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW52))、导航视图控制器([Navigation Bar](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW3))和对分视图控制器([split view controller](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW3)).
>提示   
想要了解如何在代码中定义容器视图控制器，请参考[UIViewController Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIViewController_Class/index.html#//apple_ref/doc/uid/TP40006926)
  
容器视图控制器不存在任何预先定义好的外观或者行为。  
如果你在自定义容器视图控制器对象的时候把UIViewController归为子类，你可以自己规定它里头应该包含多少子类，以及它们将如何展现出来。  
**先问问你自己是不是必须用到容器视图控制器。**用户会更习惯诸如对分视图、或者是标签栏视图这类他们所熟知的东西。你必须确保你设计的控制器的优点不会由于用户不熟悉、不认识、不会用而白费功夫。  
**确保你的容器内容控制器在横屏与竖屏模式都可用。**你的容器视图控制器无论在横屏还是竖屏中，体验都应该是一致的。  
**一般来说，避免太过花哨的转场动画。**如果你采用了故事板(storyboard)的设计方法来设计你的视图内容控制器，你往往自然而然地会为它自定义一些动画。但绝大多数情况下，这些花哨的转场动画会让用户分心，让他们忘记了当前要做的事，还可能降低你的应用整体的美感。  

##图片视图 - Image View
图片视图用以展示一张单独的图片，或者一系列动态图片。

>提示   
想要了解如何在代码中定义图片视图，请参考[image views](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIViewController_Class/index.html#//apple_ref/doc/uid/TP40006926).
  
图片视图: 
-	图片视图不存在任何预先定义好的外观，同时在默认状态下它不支持用户的交互行为。 
-	图片视图可以检测图片本身及其父视图(parent view)的属性，并决定这个图片是否应该被拉伸、缩放、调整到适合屏幕的大小，或者固定在一个特定的位置。  
在iOS 7里，包含了模版图片(template image)的图片视图会把当前的色调(tint color)应用到图片上。
请务必确保图片视图中的每一张图片都保持相同的尺寸和比例。如果你的图片尺寸各不相同，图片视图将会逐一对它们进行调整；而当你的图片比例不一，渲染的时候很可能会出错。

##地图视图 - Map View
地图视图呈现地理数据，同时支持系统内置地图应用的大部分功能（如下图所示）。

>提示   
想要了解如何在代码中定义地图视图，请参考[Map Kit Framework Reference](https://developer.apple.com/library/ios/documentation/MapKit/Reference/MapKit_Framework_Reference/index.html#//apple_ref/doc/uid/TP40008210).
  
地图视图: 
-	地图视图通常以标准地图、卫星图像、或两者结合的形式来展示地理区域。
-	地图样式还会标注单一的地点(annotations)，描绘路径和二维区域的轮廓。
-	用户可以缩放和移动地图视图——除非你在应用中禁用了这些动作——你也可以在编程时自定义地图视图的缩放和移动。  

利用地图视图可以给用户提供一个可交互的地理区域视图。如果你在开发一个导航类应用(routing app)，可以使用地图视图来展示你给用户的路径。
一般来说，允许用户在视图中进行交互行为。用户习惯了在系统内置地图中进行交互，因此他们会有预期，能在你所提供的地图中进行类似的行为。
使用标准的地图标注颜色。地图上标注了一系列地点。因为用户习惯了内置地图的各个标注的颜色，所以最好避免在你的应用中重新定义这些颜色的含义。定义颜色时，请遵循以下这些标准：
-	红色——表示目的地
-	绿色——表示起点
-	紫色——表示用户指定的地点(User-Specified Point)  

##页面视图控制器 - Page View Controller
页面视图控制器通过滚动(Scrolling)或翻页 (Page-curl transition style)来处理长度超过一页的内容。
 
>提示   
想要了解如何在代码中定义页面视图控制器，请参考[Page View Controller](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/PageViewControllers.html#//apple_ref/doc/uid/TP40011313-CH4).
页面视图控制器: 
-	带滚动条的页面视图控制器没有默认的外观
带翻页效果的控制器可以在两页中间增加书脊(book spine)的效果——当用户翻页时，它看起来就像一本真实的书在翻页一样。
-	页面内容控制器可以根据指定的切换效果来模拟出页面切换时的动画。 
使用滚动条效果的时候，当前页面将滚动到下一页；而使用翻页效果时，页面上会出现一个模拟实体书或笔记本翻页效果的翻页动画。
  
使用页面视图控制器来展示那些线性的内容——例如一个故事的文本，或者是一些可以被自然地拆分成块的内容——比如说，日历。
如果需要，可以创建一个让用户实现非线性跳页的方式。页面视图控制器让用户从一页移动到前一页或者后一页，而并不支持用户在并不相邻的页面间快速切换。如果你希望在页面视图控制器中展示一些非线性的内容——比如说字典，或者书籍的目录——那么你就需要自定义一种方式，让用户可以随意地到达不同的内容区块。

## 弹出框 - Popover
弹出框就是一个当你点击某一按钮在屏幕上出现的瞬态区域。
 
>提示   
在ios8和后续版本中，你可以使用[UIPopoverPresentationController](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPopoverPresentationController_class/index.html#//apple_ref/occ/cl/UIPopoverPresentationController)来呈现出弹出框（popover）。UIPopoverPresentationController定义一个代表让你的popover的内容可以适配当先屏幕环境。举个例子，在通常的水平环境下，你的内容可以在popover中滚动显示；而在水平紧凑环境下，你的内容可以完全呈现在屏幕上。
  
弹出框: 
-	是一个独立的模态视图
-	在水平正常的环境下，有一个箭头指向它的来源
-	具有半透明背景，可以模糊背景内容
-	可以包含各种对象和视图，例如：
 -	输出表，图像，地图，文本，网页，或自定义视图
 -	导航栏，工具栏，或标签栏
 -	控件或对象在当前的应用程序视图对物体的行为  
（默认情况下，表观，在弹出的导航栏和工具栏，使用透明背景让弹出的模糊显示通过。）
在一个水平正常的环境下，popover 总是出现在一个弹出菜单中。
使用弹出显示附加信息或一系列的选定对象相关的项目。

>提示   
本节中的指南包括界面和用户是在一个水平正常的环境中显示的用户体验。如果你提出的 popover 是在水平紧凑的环境是全屏显示的，看[Modal View](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Alerts.html#//apple_ref/doc/uid/TP40006556-CH14-SW3)的指导原则，其他全屏幕模式视图模型视图。

避免提供“取消”按钮。当用户不希望继续浏览popover时，它应该自动关闭。确定了当一个popover需要关闭时，考虑下面的情况：

如果弹出框…	那么…
提供的选项影响了主菜单，却不执行检查	只要当用户做出选择或是点击弹出框外的任意空白处，就马上关闭弹出框以及与弹出框有关的控件部分。
执行检察	当用户点击弹出框外的任意空白处，就马上关闭弹出框以及与弹出框有关的控件部分。
这种情况下，不要当用户做出选择就马上关闭它，因为用户可能想做出其他选择或者改变现在选择的属性。
完成一项任务	当用户通过点击弹出框中的按钮（例如“Done”“Cancel”）来完成或取消一个任务时，关闭弹出框。
这种情况下，当用户点击框外的时候可能不希望关闭它，因为它可能对于用户完成或准确的删除某项任务是十分重要的。否则，当用户点击框外区域的时候保存他们的输入内容，就像他们点击了Done一样。

  
一般来说，当用户点击 popover 的外边界时，尽可能减少他们的工作。不是所有人都需要一个“取消”按钮，你的取消按钮可能会给他们带来误会。如果用户点击“取消”按钮，那意味着要删除刚刚完成过的工作。  
使 popover 箭头尽可能直接的元素，显示它。这样做可以帮助人们记住弹出来自什么任务或对象的关联。  
确保人们在看一个 popover 的时候是看不到它背后的应用程序内容的。Popover 要遮挡住它后方的显示内容，而且不能通过拖拽来移动它的位置。  
确保同一时间在屏幕上只显示一个 popover。你不应该在同一时间显示多个popover（或自定义视图的设计看起来像一个popover）。特别是你要避免让一个 popover 中出现另一个 popover。  
不要在 popover 的顶部显示一个弹出模态视图。除了一个警报，什么都不应该在popover中出现。  
如果可能的话，让人们可以在关闭一个 popover 的同时打开另一个 popover。这种行为是特别合适在几种不同的栏按钮都需打开一个 popover时的，因为它让用户不用点击很多次。  
别让 popover 过大了。popover 不应该占满整个屏幕。相反，它应该是足够大，以显示其内容，还指出它来自的地方。popover 弹出的高度是不受约束的，所以你可以用它来显示一个很长的清单。但似乎一般来说，你应该尽量避免在一个弹出菜单，使任务滚动。注意，系统应该可以调整popover的宽度和高度以确保它适合在屏幕上显示。  
在 popover 中使用标准UI控制器和视图。通常来说，当 popover 包含标准控制器和视图时，看上去舒服是用户最简单的理解。  
确保自定义 popover 看上去也是一个普通的弹出框。虽然我们可以用[UIPopoverBackgroundView APIs]()很轻易地自定义 popover 的可视化效果，但还是要避免做出人们难以辨别的 popover。如果你把 popover 的样子改动过多，用户就不能以他们的经验来理解 popover 在应用程序中的作用了。  
如果你修改了 popover 的尺寸那一定要小心。如果你用 popover 同时显示内容和内容的扩展时，你可能希望改变 popover 的尺寸。当你适配了 popover 的尺寸时，它也许是个不错的创新，因为它避免了一个新的 popover 在上一个 popover 中出现。  

## 滚动视图 - Scroll View
滚动视图方便用户浏览尺寸超越滚动视图边界的图片（下图中地球的图片无论是长度还是宽度都超过了）。
 
>提示   
想要了解如何在代码中定义滚动视图，请参考[Scroll Views](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UIScrollView.html#//apple_ref/doc/uid/TP40012857-UIScrollView)。
  
滚动视图: 
-	滚动视图没有预定义的外观。
-	滚动视图刚出现或者当用户在对它进行操作的时候——纵向和横向的滚动指示器会短暂地闪烁，以提示用户在当前视图外仍有更多内容。
-	滚动视图的响应速度和对各个操作手势的识别都应当让用户感到自然。当用户在视图中拖拽内容，内容随之滚动；当用户轻扫屏幕时，内容将快速滚动——直到用户再次触摸屏幕或内容已经到达底部时停止。滚动视图同样可以应用在页模式(paging mode)中，在此模式下用户可以通过拖拽和轻击等手势来浏览一页的内容。
-	你可以使用滚动视图来允许用户在固定的空间内浏览大尺寸或大量的视图。因为在iOS中用户常常会用到滚动视图，所以请确保你的应用中滚动视图的操作与他们的预期相同。
  
适当地支持缩放操作。如果放大和缩小对于当前内容是有用的话，你可以支持用户通过捏或者双击来对当前视图进行缩放。而若是支持了缩放操作的话，你还应当设定在当前情景下允许缩放的最大值和最小值。如果你允许一个字符被放大到充满整个屏幕的话，用户会很难阅读当前内容。
在页模式滚动视图中，可以考虑使用页面控件(page control)。当你想要展示分页、分屏或者分块的内容，最好是让用户知道当前内容一共有多少块，以及他们当前浏览的是第几个——页面控件以圆点的形式来把这个信息告诉用户。同时由于页面控件被广泛用于Safari，股票，天气以及其它系统内置应用中，用户很容易理解它的用途。
当你在滚动视图中使用页面控件的时候，最好禁用同一方向的滚动指示器(scroll indicator)。这样一来用户就有了一种唯一且清晰的方式来浏览当前内容。想要了解更多请参考Page Control.
一般来说，一次只展示一个滚动视图。如果在一屏中同时存在不止一个滚动视图，由于用户滚动屏幕时动作幅度经常都会很大，他们很容易会碰到另一个。如果你确实要在同屏中放两个滚动视图，可以考虑给他们设定不同的滚动方向，来避免用户想要滚动一个视图的时候误操作。比如iPhone上的股票应用，纵向滚动上半部分会展示股票报价，横向滚动下半部分时则展示该公司的特定信息。


## 分离视图控制器 - Split View Controller
分离视图控制器是一个全屏的视图控制器，它管理着两级视图。
 
>提示   
每个子视图控制器负责管理一个窗格的显示。拆分视图控制器本身提出了这些子视图控制器和管理过渡之间的不同取向的转变。要了解更多关于在你的代码中定义一个拆分视图控制器的内容，请参考[UISplitViewController Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISplitViewController_class/index.html#//apple_ref/doc/uid/TP40009277) 和 [Split View Controllers](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/SplitViewControllers.html#//apple_ref/doc/uid/TP40011313-CH7).
  
在ios7和更早的系统中，分离视图控制器只用在 ipad 上。
通常，分离视图控制器使用尺寸类别来安排子视图控制器。例如，分离视图控制器：
-	试图在普通环境下显示窗格水平排列
-	可以在顶部的次要窗格层状主窗格中显示，或隐藏在主窗格中，在需要时显示。它通常在一个水平紧凑的环境。   
你可以通过拆分视图控制器修改优先布局，更加关注需要特别显示的内容。
分离视图控制器可以包含很多的内容和视图，例如：
-	表，图片，地图，文字，网络，或自定义视图
-	导航栏，工具栏，标签栏

>提示   
尽管前一个显示的窗格常被称为是主窗格，第二个显示的被称为次窗格，但这种关系在代码中并不强制要求。
  
**使用拆分视图控制器在主窗格中显示持续性的信息和相关细节，或在二级窗格显示下属信息。**在这种设计模式，当人们选择在主窗格中的一个项目，第二面板应显示与该项目相关的信息。（你要在代码中实现）  
**避免显示的二次窗格，比原窗窄。**如果次级窗格是比主窗格窄，拆分视图控制器便不再充满屏幕，这和整体的外观是不平衡的。  
**避免在两次窗口中都出现导航栏。**这样做会让用户很难区分这两级窗口的关系。  
**通常，让当前的选择在主窗口中长时间显示。**尽管第二窗格的内容是可以改变的，它应始终与保持在主窗格中选定的项目有关。这样的观看体验，帮人们了解在主窗格中的项之间的关系和二次窗格的内容。  
**如果合适的话，给用户一个可选择的方式来访问主窗格中。**通常，只有次级窗格在水平紧凑的环境中显示时，为用户提供一个按钮（通常位于一个导航栏）来显示和隐藏主窗格。拆分视图控制器还支持滑动手势进行显示/隐藏行动。如果你的应用程序使用滑动手势来执行其他功能，你应该让人们点击访问主窗格。  

## 表格视图 - Table View
表格视图以单列多行的形式来展示数据。
 
>提示   
想要了解如何在代码中定义表格视图，请参考[Tabel View Programming Guide for the iOS](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/TableView_iPhone/TableViewStyles/TableViewCharacteristics.html#//apple_ref/doc/uid/TP40007451)以及[Table Views](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UITableView.html#//apple_ref/doc/uid/TP40012857-UITableView).
  
表格视图: 
-	表格视图中的数据是以单列的方式展示的，因此也很容易将它们分段或者分组。 
- 提供一个控制钮让用户可以添加、移除列，选择几个列，看到有关列项目的更多信息，或者显示另一个表格视图。  
iOS定义了两种表格样式:
平铺型（Plain）表格可被分为若干带标签的段落，表格右侧可能会出现垂直的表格索引。每行开头可以有页眉，尾部可以有页脚（也可以没有）。
![]()
   
分组型（Grouped）中至少含有一组列表，而每一组中至少包含一项内容。分组可以有页眉和页脚。与平铺型不同，分组型表格没有索引。
在这两种风格中，当用户点击一个可选择的项目时，表格行高亮显示。如果选择了一个行，跳转到一个新的屏幕，被选的行高亮显示作为新屏幕的出现提示。当用户返回前一个屏幕时，最初选定的行，再变成高亮，简要地提醒用户这是之前选择的内容。（这并不突出）。
  
iOS提供了若干表格视图元素(table-view elements)来扩展表格视图的功能。除了特别标明外，这些元素只适用于表格视图。

视图元素	名称	含义
 ![](image/check_2x.png)	对号	指示这行被选中
 	![](image/disclosure_indicator_2x.png)指示符号	显示另一个与这行相关的表
 	![](image/detail_disclosure_2x.png)细节提示按钮	在新视图中显示与这行有关的更多细节（了解如何运用这个元素，查看[popover](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH13-SW19)）

 	![](image/row_reorder_2x.png)行排序	指示该行可以在表中被拖拽到其他位置。
 	![](image/row_insert_2x.png)增加行	给表加一个新的行
 	![](image/delete_control_2x.png)删除按钮控件	在编辑状态下，显示和隐藏删除一行”按钮。

 ![](image/delete_button_2x.png)	删除按钮	删除行


  
除了以上表格中列举的元素外，iOS定义了刷新控件，让用户可以刷新当前的表格内容。想要了解更多关于刷新控件的用法，可以参考[Refresh Control](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW131). 
iOS定义了在平铺型表格和分组型表格中最常用到的四种单元格布局样式。每种单元格样式都有最适合展示的信息类型。

>提示  
从编程角度来说，这些样式应用于单元格中，用以控制表格里每一列的绘制方式。
   
默认型（Default）([UITableViewCellStyleDefault](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/index.html#//apple_ref/c/econst/UITableViewCellStyleDefault))
默认型样式包括左侧的图标（可选），和图标右边左对齐的文字标题。
默认型样式适合展示一系列无须通过附加信息便可以区分的项。
  
副标题型（Subtitled）([UITableViewCellStyleSubtitle](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/index.html#//apple_ref/c/econst/UITableViewCellStyleSubtitle))
副标题型包括左侧图标（可选），图标右边左对齐展示的文字标题，以及在标题下方同样左对齐展示的副标题。
左对齐的文本标签让用户可以更快速地扫视表格。这种样式适用于列表各项较为相似的情况，用户可以通过副标题中的详细信息来区分列表中的各项。
   
 
Value 1 ([UITableViewCellStyleValue1](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/index.html#//apple_ref/c/econst/UITableViewCellStyleValue1))
在Value 1样式下，标题左对齐，副标题用较细的字体右对齐。
Value 2 ([UITableViewCellStyleValue2](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/index.html#//apple_ref/c/econst/UITableViewCellStyleValue2))
在Value 2样式里，蓝色标题右对齐，副标题左对齐，混排在同一行中。这种样式通常不包含图片。
Value 2的布局中，文本和副标题中间的垂直间距会让用户专注于副标题的第一个单词。
 
>提示  
以上四种单元格样式均支持添加表格视图元素，如勾选或展开标志。添加这些元素会缩小标题以及副标题单元格的可用宽度。
  
使用表格视图可以简洁而高效地展示少量或者大量信息。举例来说，你可以通过表格视图来：
-	展示用户可选的选项列表。你可以使用选中标记来告知用户当前选中了哪些项。
-	展示层级信息。平铺型表格样式非常适合展示层级信息。表格中的每项都指向不同的子信息，这些子信息承载于另一个列表中。用户可以沿着这些层级结构的路径来点击每一层列表中的项。展开标志告知用户点击这一列中的任何位置，都将展开新的列表以展示其子类信息。
-	展示可以在概念上进行分组的信息。平铺型和分组型列表都允许你通过提供页眉和页脚来对信息进行分组和分段。
  
你可以用页眉页脚视图(header-footer view)——即UITableViewHearderFooterView中的一个实例——来展示页眉和页脚的文字，或图片。想要了解如何在代码中定义页眉页脚视图，请参考UITableViewHeaderFooterView Class Reference. 

展示索引来方便查找。平铺型列表支持索引，可以让用户快速地找到需要的内容。索引信息包含一个浮在屏幕右侧的、纵向罗列的条目，内容则通常是字母表中的字母。
如果你使用了索引，要避免在表格右侧使用其它表格视图元素——比如展开指示符——因为它们与索引是冲突的。

使用表格视图时可遵循以下指南：
用户选择列表项时，始终给与反馈。当用户点击可选的列表项时会认为被点击的项都应短暂地高亮一下。在点击后，用户期望出现新的视图，或者出现一个复选标记以表明先前点击的项已经被选中或激活。  
如果表格的内容庞大而且复杂，不要等数据都加载完之后才一起显示出来。可以首先展示文字信息，图片等较为复杂的内容则在加载完后再显示。这样可以将有用的信息立即传达给用户，同时也提高了应用的响应能力。  
在等待信息加载的时候，可以考虑展示“过期”信息。尽管我们并不推荐在数据频繁变化的应用中这样做，它还是可以帮助更多的静态应用程序立即给到用户有用的信息。当然在你这么做之前，请认真衡量你应用中数据的变化频率，并弄清楚你的目标用户有多需要立即获取最新的信息。  
如果信息加载速度很慢或者非常复杂，你需要告诉用户加载正在进行中。如果表格中所有内容都很复杂，我们很难即时地给用户展示任何内容。在这种极端情况下，切勿显示空白的表格，因为这会让用户以为应用挂了。此时应当在屏幕中央展示一个活动指示器(activity indicator)和一个信息标签(information label)，比如“加载中…”，让用户知道加载仍然在进行。  
如果合适的话，为删除按钮自定义一个名称。如果这能让用户更好地理解应用的相关功能的话，你可以创建一个合适的标题，来取代“删除”这个字样。  
尽量使用简洁的文字标签，以避免被截断。繁冗的文字和词组不方便用户浏览和理解。以上所有单元格样式均会自动截断文本，而文本截断所造成的问题可大可小，取决于你采用的单元格样式，以及被截断了哪一部分文字。  
如果你想以一种非标准的形式来布局你的表格，最好是自定义一种单元格样式，而不是在现有的表格样式上进行改动。如何创建自定义单元格样式，请参考Customizing Cells  

##文本视图 - Text View
文本视图可以接收和展示多行文本。
 
>提示  
想了解如何在代码中定义文本视图，参考[Text Views](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UITextView.html#//apple_ref/doc/uid/TP40012857-UITextView).

文本视图: 
-	文本视图是矩形，可定义为任何高度。 
-	当内容太多超出视图的边框时，文本视图支持滚动。
-	如果文本视图支持用户编辑，当用户轻击文本视图内部时，将唤起键盘。键盘的布局和类型取决于用户的系统语言设置。  
你可以控制文本视图中文字的字体、颜色和对齐方式。文本视图的默认字体是系统字体，默认字色是黑色。默认文字对齐方式是左对齐（你可以改为居中或右对齐）。
始终确保文字的易读性。虽然你可以使用属性字符串将不同的字体、字色和对齐方式串联在同一个文本视图内，但保持文本的可读性是必不可少的。最好是可以支持动态文本(Dynamic Type)和[UIFont](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIFont_Class/index.html#//apple_ref/occ/cl/UIFont) method preferredFontForTextStyle来展示文本框中的文本。想要了解动态文本的更多支持引导，参考[Text Should Always Be Legible](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/ColorImagesText.html#//apple_ref/doc/uid/TP40006556-CH58-SW3);编程信息，参考[Text Styles](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/CustomTextProcessing/CustomTextProcessing.html#//apple_ref/doc/uid/TP40009542-CH4-SW65)  
根据输入内容的类型来指定不同的键盘类型。举例来说，你希望用户能更方便地输入网址、密码或者电话号码。但请注意，由于键盘的布局以及输入方法是由用户的系统语言设置决定的，这是你不能控制的。  
iOS提供了各种不同的键盘类型，以便用户输入不同类型的文本。想要了解可用键盘类型，可以参考UIKeyboardType.想要了解如何在管理你的应用中的键盘，请参考iOS App Programming Guide中的Managing the Keyboard部分。  

##网络视图 - Web View
网络视图是一个可以展示丰富的HTML内容的区域。（下图是iPhone自带的邮件应用，网络视图指的是下图中导航栏和标签栏中间的区域）
 
>提示  
想要了解如何在代码中定义网络视图，请参考[Web Views](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UIWebView.html#//apple_ref/doc/uid/TP40012857-UIWebView).

网络视图: 
-	展示网络内容
-	自动处理页面中的内容，比如把页面中的电话号码转化成电话链接。  
如果你经营一个网页或者网络应用，你大约会用网络视图来实现一个简单的iOS App，来对你的网页或者应用进行一个封装。如果你打算用网络视图来访问你所控制的网页内容，请务必阅读Safari Web Content Guide.
不要用网络视图来创建一个看起来像迷你网络浏览器的应用。用户期望使用iOS自带的Safari来浏览网页内容，因此我们并不推荐你在自己的应用中复制这种以被广泛应用的功能。


