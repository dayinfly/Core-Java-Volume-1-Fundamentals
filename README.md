# Core-Java-Volume-1-Fundamentals
record my java learning way


2018/10/27日受V2er启发，想与今日开始记录学习《Java核心技术》这本书，说是记录，其实是做一个摘录，目的是为了让自己学习的时候能够集中精神，也相信好记性不如烂笔头，说干就干，能否坚持，拭目以待。
                    第一章 Java程序设计概述
         ·Java程序设计平台
         ·Java发展历史
         ·Java"白皮书"的关键术语
         ·关于Java的常见误解
         ·Java applet与Internet
   1996年Java第一次发布就引起了人们的极大兴趣。关注Java的人士不仅限于计算机出版界，还有诸如《纽约时报》《华盛顿邮报》《商业周刊》这样的主流媒体。Java是第一种也是唯一一种在National Public Radio上占用了10分钟时间来进行介绍的程序设计语言，并且还得到了$100 000 000的风险投资基金。这些基金全部用来支持这种特别的计算机语言开发的产品。重温那些令人兴奋的日子是很有意思的。本章将简要低介绍Java语言的发展历史。
   1.1Java程序设计平台
   本书的第一版是这样描写Java的:"作为一种计算机语言，Java的广告词确实有点夸大其辞。然而，Java的确是一种优秀的程序设计语言。作为一个名副其实的程序设计人员，使用Java无疑是一个好的选择。有人认为：Java将有望成为一种最优秀的程序设计语言，但还需要一个相当长的发展时期。一旦一种语言应用于某个领域，与现存代码的相容性问题就摆在了人们面前。"
   我们的编辑手中有许多这样的广告词。这是Sun公司高层的某位不愿意透露姓名的人士提供的(Sun是原先开发Java的公司)。Java有许多非常优秀的语言特性，本章稍后将会详细地讨论这些特性。由于相容性这个严峻的问题确实存在于现实中，所以，或多或少地还是有一些“累赘”被加到语言中，这就导致了Java并不如想象中那么完美无暇。
   但是，正像我们在第一版中已经指出的那样，Java并不只是一种语言。在此之前出现的那么多种语言也没有能够引起那么大的轰动。Java是一个完整的平台，有一个庞大的库，其中包含了许多可重用的代码和一个提供诸如安全性、跨操作系统的可移植性以及自动垃圾收集等服务的执行环境。
   作为一名程序设计人员，常常希望能够有一种语言，它具有令人伤心悦目的语法和易于理解的语义（C++不是这样的）。与许多其他的优秀语言一样，Java完全满足了这些要求。有些语言提供了可移植性、垃圾收集等，但是，没有提供一个大型的库。如果想要有奇特的绘图功能、网络连接功能和数据库存取功能就必须自己动手编写代码。Java具备所有这些特性，它是一种功能齐全的的出色语言，是一个高质量的执行环境，还提供了一个庞大的库。正是因为它集多种优势于一身，所以对广大的程序设计人员有着不可抗拒的吸引力。
   1.2Java“白皮书”的关键术语
   Java的设计者已经编写了颇有影响力的“白皮书”，用来解释设计的初衷以及完成的情况，并且发布了一个简单摘要。这个摘要用下面11个关键术语进行组织：
   1）简单性        2）面向对象
   3）分布式        4）健壮性
   5）安全性        6）体系结构中立
   7）可移植性      8）高性能
   9）解释型        10）多线程
   11）动态性
   1.2.1 简单性
   人们希望构建一个无需深奥的专业训练就可以进行编程的系统，并且要符合当今的标准惯例。因此，尽管人们发现C++不太适用，但在设计Java的时候还是尽可能地接近C++，以便系统更易于理解。Java剔除了C++中许多很少使用、难以理解、易混淆的特性。在目前看来，这些特性带来的麻烦远远多于其带来的好处。
   的确，Java语法是C++语法的一个“纯净”版本。这里没有头文件、指针运算（甚至指针语法）、结构、联合、操作符重载、虚基类等。然而，设计者并没有试图清除C++中所有不适当的特性。列如，switch语句的语法在Java中就没有改变。如果你了解C++就会发现可以轻而易举地转换到Java语法。
   Java发布时，实际上C++并不是最常用的程序设计语言。很多开发人员都在使用Visual Basic和它的拖放式编程环境。这些开发人员并不觉得Java简单。很多年之后Java开发环境才迎头赶上。如今，Java开发环境已经远远超出大多数其他编程语言的开发环境。
   简单的另一个方面是小。Java的目标之一是支持开发能够在小型机器上独立运行的软件。基本的解释器以及类支持大约仅为40KB；再加上基础的标准类库和对线程的支持（基本上是一个自包含的微内核）大约需要增加175KB。
   在当时，这是一个了不起的成就。当然，由于不断地扩展，类库已经相当庞大了。现在有一个独立地具有较小类库地Java微型版（Java Micro Edition）,这个版本适用于嵌入式设备。
   1.2.2面向对象
   简单地讲，面向对象设计是一种程序设计技术。它将重点放在数据（即对象）和对象的接口上。用木匠打一个比方，一个“面向对象的”木匠始终关注的是所制作的椅子，第二位才是所使用的工具；一个“非面向对象的”木匠首先考虑的是所用的工具。在本质上，Java的面向对象能力与C++是一样的。
   开发Java时面向对象技术已经相当成熟。Java的面向对象特性与C++旗鼓相当。Java与C++的主要不同点在于多重继承，在Java中，取而代之的是更简单的接口概念。与C++相比，Java提供了更丰富的运行时自省功能。
  1.2.3分布式
  Java有一个丰富的例程库，用于处理像HTTP和FTP之类的TCP/IP协议。Java应用程序能够通过URL打开和访问网络上的对象，就像和访问本地文件一样方便，在1995年，主要还是从C++或Visual Basic程序连接Web服务器。
  1.2.4健壮性
  Java的设计目标之一在于使得Java编写的程序具有多方面的可靠性。进行早期的问题检测、后期动态的检测，并消除了容易出错的情况。Java和C++最大的不同在于Java采用的指针模型可以消除重写内存和损坏数据的可能性。
  1.2.5安全性
  Java适用于网络/分布式环境。为了达到这个目标，在安全方面投入了很大的精力。使用Java可以构建防病毒、防篡改的系统。
  从一开始，Java就设计成能够防范各种攻击，其中包括：
  运行时堆栈溢出。如蠕虫和病毒最常用的攻击手段。
  破坏自己进程空间以外的内存。
  未经授权读写文件。
  1.2.6体系结构中立
  编译器生成一个体系结构中立的目标文件格式，这是一种编译过的代码，只要有Java运行时系统，这些编译后的代码可以在许多处理器上运行。Java编译器通过生成与特定的计算机体系结构无关的字节码指令来实现这一特性。精心设计的字节码不仅可以很容易地在任何机器上解释执行，而且还可以动态地翻译成本地机器代码。
  虚拟机有一个选项，可以将执行最频繁地字节码序列翻译成机器码，这一过程被称为即时编译。
  Java虚拟机还有一些其他地优点。它可以检测指令序列地行为，从而增强其安全性。
  1.2.7可移植性
  与C和C++不同，Java规范中没有“依赖具体实现”地地方。基本数据类型地大小以及有关运算都做了明确的说明。
  在Java中，数据类型有固定地大小，这消除了代码移植时令人头痛的主要问题。二进制数据以固定的格式进行存储和传输，消除了字节顺序的困扰。字符串使用标准的Unicode格式存储的。
  不过，除了与用户图形界面有关的部份外，所有其他Java库都能很好地支持平台独立性。你可以处理文件、正则表达式、XML、日期和时间、数据库、网络连接、线程等，而不用操心底层操作系统。不仅程序可移植的，JavaAPI往往也比原始API质量更高。
  1.2.8解释型
  Java解释器可以在任何移植了解释器的机器上执行Java字节码。。由于链接是一个增量式且轻量级的过程，所以，开发过程也变得更加快捷，更加具有探索性。
  1.2.9高性能
  尽管对解释后的字节码性能已经比较满意，但是有些场合下还是需要更加高效的性能。字节码可以动态地翻译成对应运行这个应用的特定CPU的机器码。
  性能就是适用性更强。
  1.2.10多线程
  多线程可以带来更好的交互响应和实时行为。
  如今，我们非常关注并发行，因为摩尔定律行将完结。我们不再追求更快的处理器，而是着眼于获得更多的处理器，而且要让它们一直保持工作。
  并发程序设计绝非易事，不过Java在这方面表现很出色，可以很好地管理这个工作。
  1.2.11动态性
  从各种角度看，Java与C或C++相比更加具有动态性。它能够适应不断发展的环境。库中可以自由地添加新方法和实例变量，而对客户端却没有任何影响。在Java中找出运行时类型信息十分简单。
  当需要将某些代码添加到正在运行的程序中时，动态性将是一个非常重要的特性。
