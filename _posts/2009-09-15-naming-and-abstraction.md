---
layout: post
title: "命名与抽象"
description: ""
category: "work"
tags: [thoughtworks]
---
{% include JB/setup %}

好的名字总是能为代码的可读性做出重大贡献，而这种贡献是通过对事物进行抽象实现的。

想想一下我们平常说话时所用的语言，比如说“我家的狗跑的很快”，“家”、“狗”和“跑”都是抽象，它们分别代表了不同的含义，如果不适用这几个抽象的词汇，而是直接说它后面所代表的含义，恐怕几十句话都说不完。不信的话，你可以试试定义一下什么是狗，什么是跑，保证不是那么容易的事。

抽象可以说是软件设计和开发中的核心概念，对变量、方法、类、接口、包等元素的命名，都包含了抽象过程。例如方法，方法的名字应等价于方法内部所有代码的功能，也就是说方法的名字是方法内代码功能的抽象。于是，不管是在交流还是记忆上，我们都可以使用方法名来指代它内部的功能。

由于人的记忆力和理解能力都是有限的，据研究称，人最多之能同时处理7个左右的事物。因此对于复杂的软件系统，抽象就成为让人能够理解的重要手段。在代码量较小的系统中，可能抽象也比较少，理解起来比较容易，变量、方法和类基本就能处理了；而在大一些的系统中，由于抽象较多，因此需要更多的抽象层次，使得在每一个抽象层次上都能有比较少的抽象概念，以利于理解，于是出现了诸如分层、子系统、组件、库等等。同时在类和方法内部，也会有分层次的抽象，继承就是类的一个抽象层次关系，而方法之中调用其它方法，也是抽象层次的一种表现。

例如，狗这个类可以有很多不同子类，每一种代表不同品种的狗。从上往下看，子类是父类的泛化，是在父类上添加更多的细节；而从下往上看，父类则是子类的抽象，集合了更多子类的相同之处。在类的层次结构中，每一级的父类都会包含更多的抽象和更少的细节。因此往往父类比子类更能表达这个层次结构的核心概念，也就应该更谨慎的选择一个好的名字，来表达这种核心概念。同时子类的名字应该能够体现它的子类的共性，同时还应能够区分与其它同级子类的不同。

而在方法中，我们有一种使方法更具可读性的方式，就是让方法中的每一行代码都处于相同的抽象级别。例如，“我家的那只会叫的哺乳类四腿……动物跑的很快”这句话就很难理解，因为你的思维需要在不同的抽象级别上跳来跳去，“家”和“跑”都是可以马上理解的概念，而“会叫的哺乳类四腿……动物”则是需要思考一下才能理解的。因此比较简单的做法就是将这个细节抽象称一个名字“狗”，将之提取出来，形成另一个概念（也就是方法）。于是，系统中的方法本身也就有了不同的抽象层次，有些关注与调用语言和平台的API来实现某些操作，有些则会调用这些方法实现更高层次的逻辑。在面向过程的设计中，最后的结果就是main函数，而在OO设计中，可能是某个类的public方法。

命名好坏对可读性的影响，实际上是抽象方式对人的思维方式造成的影响。如果你找不到一个好的名字，通常就意味着你对问题的抽象是不恰当的，隐含的意思就是你对问题的理解不够深入或者理解错误。
