# 通过搜索微服务 发现难以访问的媒体档案

> 原文：<https://www.algolia.com/blog/product/internal-search-unleashing-media-content-at-scale-with-headless/>

《华盛顿邮报》 [每天发布大约 1200 篇报道、图片和视频](https://www.theatlantic.com/technology/archive/2016/05/how-many-stories-do-newspapers-publish-per-day/483845/) 。你没看错:每天有 1200 条内容。这相当于每年将近 50 万条内容。这是一个多产的产品，但没什么不寻常的。《华尔街日报》和《纽约时报》每天都会发表大约 240 篇文章和博客文章。BuzzFeed 是一家以高产出闻名的公司，每天发布 220 篇文章、博客、文章和视频。

重点是:报纸产生了大量的材料。不仅仅是报纸。大多数媒体公司—无论是广播、新闻、出版物、音频还是流媒体—都制作和管理着庞大的内容库。他们的档案通常保存在自制的内容管理系统(CMS)上，这是有充分理由的。

媒体公司有非常特殊的需求:特定的内容目录、独特的编辑工作流程和特定的出版策略。几乎没有现成的解决方案既强大又灵活，能够满足所有需求。所以公司建造，而不是购买。以生产出版为目的，他们自建 CMS 做工作。但是他们无意中把内容锁在了不可访问的档案中。

自建平台内的原生搜索一直很差。相关性不够，用户界面拥挤，高级功能缺乏——如果有的话。通常，搜索功能将在简单的关键字匹配上运行，这对于小型搜索索引来说很好，但对于庞大的媒体库来说不太合适。

假设一名记者每周写一篇关于他们国家低碳技术的更新。如果他们在自己的 CMS 上搜索 *低碳* ，一个基本的关键词搜索就会返回成百上千个结果。《卫报》上的一个快速实验显示了超过 32，000 个结果。这种高压手段会产生太多的结果，无法人工筛选。除非有问题的记者中了头彩，否则他们不会偶然发现他们要找的东西。但是过时的搜索技术并不是唯一的挑战。数据一致性也加重了内部搜索的负担。

很少有媒体公司在内部制作所有内容。报纸刊登来自外部记者的电讯报道。杂志刊登来自合作伙伴出版物的联合报道。电视网从无数制作公司购买节目。音乐流媒体服务合并了数百家独立唱片公司的回溯目录。毫无疑问，每个源都有不同的元数据结构。也不能保证创作者(记者、电影制作人、编辑)会坚持他们的内部结构。不一致的元数据意味着不能保证您搜索的是整个内容库。

对于许多媒体公司来说，这两个挑战(搜索技术和元数据一致性)使得内部搜索不可靠，甚至误导和虚假。但是这有什么关系呢？

## [](#time-productivity-and-impact)时间、生产率和影响

回想一下那位记者报道的 低碳技术 。这是一篇简单、直白的文章，但是有很多丰富的机会。记者可以附上一张图表，显示各行业的低碳推广统计数据，或者嵌入他们最近对一位生物技术专家的采访。他们可以链接到早期的建模项目，或者交叉链接到关于脱碳策略的意见文章。

但是记者只能做到 *如果* 他们能在他们的档案中找到旧的内容。

动力不足的搜索以三种方式伤害组织。

第一，员工损失时间。如果一个旧的内容对于一个新的故事来说是必要的，那就不要无休止的滚动和搜索，一页接一页，一个接一个的搜索。人们通常会求助于在谷歌上使用站点搜索操作符查询(site:example.com“搜索术语”)。请记住，我们谈论的是高技能、有创造力的专业人士——记者、电影制作人、编辑等等。组织真的想付钱给他们，让他们花时间在琐碎的信息收集任务上吗？几乎可以肯定不是。

第二个后果是生产率下降。当员工在寻找工作上浪费时间时，连锁效应会更加广泛。吃力地浏览没完没了的搜索结果是令人沮丧和耗费精力的。它让人们感到脱离和缺乏灵感。在竞争残酷的媒体世界里，这是你最不想要的事情。

最后，公司失去了发挥影响力的机会。媒体公司就像冰山:你只能看到它们质量的一小部分。《华盛顿邮报》每天发表 1200 篇报道，但其档案却有数千万条。面对一个不成熟的搜索功能，很多人会走开，放弃重用、丰富和添加的机会。再想想那些放弃寻找完美图表的记者。这是一种巨大的浪费。这意味着媒体公司正在让他们的档案无所作为、无效、闲置和无利可图。

但是搜索并不一定是一个阻碍者。

事实上，现代搜索服务可以释放媒体库和档案，让信息和内容触手可及。

## [](#your-technology-stack-better-search-technology)你的技术栈。更好的搜索技术。

搜索和发现的未来不在于改进 CMS 的原生搜索。不可能建立一个现成的平台来满足每个人的需求——更不用说一个具有强大搜索功能的平台了。相反，像《泰晤士报》和 POLITICO 这样的领先媒体公司正在转向像 Algolia 这样的搜索微服务。

将微服务视为可以附加到现有技术的构建模块。他们扩大你的内容管理系统的狭窄功能，而不是大规模取代它。这意味着你可以在不中断编辑工作流程的情况下革新你的内部搜索(也可能是面向用户的搜索)。

考虑一下欧洲政治。早在 2010 年，他们就推出了 POLITICO Pro，整合新闻、数据和工具，为政策专业人士提供实时情报和分析。该平台每天发布 500 篇文章，面临着与大多数媒体公司相同的挑战:如何以这样一种方式管理如此庞大的内容库，使其易于访问？

长话短说，他们为客户部署了现代搜索微服务。它与他们现有的技术堆栈相集成，统一了他们的媒体库，并允许用户一次查询多个内容索引。一夜之间，付费用户获得了一种直观有效地搜索“2400 万张选票、70 万条修正案、1.6 万名立法者和 700 万个可搜索项目”的方法。但有趣的是:开始使用这项服务的不仅仅是 POLITICO Pro 的付费用户。

POLITICO Europe 的工作人员记者开始利用新的搜索功能来了解该平台庞大的档案。突然之间，他们可以让长期丢失的洞察力和曾经隐藏的数据点浮出水面。这有助于他们更好更快地完成工作。

这是搜索的未来。类似于我们在关于[后台搜索](https://www.algolia.com/blog/product/unlock-organizational-knowledge-with-searchable-company-wide-data/)的文章中描述的，它创造了一种类似谷歌的体验——只是更好。第三方搜索引擎拥有、控制和隐藏搜索算法。你受到他们的突发奇想和实验的支配。另一方面，搜索服务向你揭示了机器和手控的内部工作原理。如果你想优先考虑最近，你可以。如果你想推广某些来源的内容，你可以。如果你想按受欢迎程度排列作品，你可以。你控制着搜索体验。

## [](#empower-human-led-creation)授权人类主导创作

媒体处于人类主导和机器主导创作的十字路口。虽然算法和自动推荐已经彻底改变了内容发布，但让人类控制仍然有一些神奇之处。媒体公司需要加倍努力，让员工能够搜索他们的媒体库和有价值的内容。我们已经拥有这样做的技术。所需要的只是敢于冒险的领导力。

[了解更多媒体行业搜索](https://www.algolia.com/search-solutions/media/) 。