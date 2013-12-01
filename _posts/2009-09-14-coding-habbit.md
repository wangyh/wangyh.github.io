---
layout: post
title: "代码习惯"
description: ""
category: "work"
tags: [thoughtworks]
---
{% include JB/setup %}

前天在AgileChina2009上听了Fred George的演讲，他说他以前拿自己的代码给Kent Beck看，结果Kent说这代码很垃圾，你去看看我写的Smalltalk best practice patterns吧。然后Fred George就看了这本书并且完全按照书上的要求去做，5年后当他再给Kent看自己的代码时，Kent说很漂亮的代码。

考虑到Fred比Kent要老，可以看出Fred是非常虚心的，听了Kent的评价不仅没有生气，而且还完全听从了建议。当然这也可能是Kent太出名的缘故，若是我说他的代码不好，或许他就不会这样做了。

这让我联想到有一次和8x一起面试，8x的手工重构让我很是惊讶。虽然我也看过《重构》，虽然我平时也重构，但是不论从步伐还是安全性上，都相差深远。我读《重构》的时候对如此小步伐的改变是不太赞同的，因为效率比较低。我认为书中之所以把条目分的很详细，每个条目的步骤很小很谨慎，完全是为了可以让支持重构的工具得以实现，对于人来说，保持这样小的步骤太难了，不管是从记忆还是从操作的角度来看。然而8x的表现让我改变了看法，不仅速度并不慢，而且安全性非常的高。回想起我的重构经常出现改错以后没法返回的问题，不禁感叹－－差距啊。

经常在国内的论坛上看到各种讨论设计、架构的帖子，然而每每show代码的时候却发现一塌糊涂。当然他们自己不觉得，可是我觉得很不好。最近Kent Beck和Robert C.Martin出的两本书《Implementation Patterns》和《Clean Code》都是讨论一些很细节的东西的，如何命名、方法应该要多长、注释怎么写、格式怎么排等等，这些东西早在《The Element of Programming
Style》中其实都有对应的东西，只不过语言不同了，细节方面也不同。然而为何这么多年来，一直有人不停的写本质上相同的东西呢？我觉得还是大家不重视，没有养成良好的习惯，自然就需要有人去写这些东西，反反复复的提醒大家。

这里再一次很惭愧的说，我没有好好去读，也没有按照书中的东西认真去做，总是以为大概了解个概念，知道怎么回事，然后差不多做到了就行了。然而现在想来，却完全不是那么回事。记得XP中有很多非常“极限”的要求，都是“一定”要如何如何，可实际上很多人都不以为然，认为太过激进，实际操作不现实或者不必要，因此在实施的时候，做了一些妥协和变通，最后失败了还说XP不好。当然XP不可能是包治百病的灵丹，在某些情况下确实也不应该用它，但是很多人明明可以从中获益，却因为没有领悟到其中的精髓而早早放弃。

比如说TDD，看起来与一般的单元测试的不同只是把写测试的工作放在了写代码之前，而Pair
Programming也不过就是两个人坐在一起写程序罢了。然而在实际应用中，却会发现TDD并不是那么简单，它带来的好处是你在使用之前完全想不到的，甚至很多都和Test是无关的。而Pair也不简单的就是两个人干一份工，如何根据技能的不同组合Pair，两人如何分工都有很大的讲究，甚至一般的对于Pair目的的理解可能也是错误的。因此要想证明一件东西能不能起作用，首先要完全按照他要求的方式去做，等到你真的把该遇到的问题都遇到了，你才能真正知道它是什么，能做什么，不能做什么，最后才知道它到底能解决什么问题，不能解决什么问题。

在说回到代码习惯的问题，软件开发中包含太多东西了，需求的、设计的、测试的、管理的、文化的、心里的、沟通的……要想掌握这么多东西是很大的挑战。如何将一件事记住而不忘掉，最好的办法就是将之变成习惯，就像呼吸一样自然，不需要刻意去想就能做到。良好的代码习惯是一个开发人员最基本的技能，使之成为习惯，会获益很多。

决定在看一遍《重构》和《实现模式》并完全按照其中的要求去做，争取也能在5年之内将之养成习惯。