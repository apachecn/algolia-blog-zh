# 作为语义搜索一部分的查询放松和范围界定

> 原文：<https://www.algolia.com/blog/ux/query-relaxation-and-scoping-as-part-of-semantic-search/>

正确的搜索查询是金发姑娘式的努力:不要太具体以至于没有结果，也不要太宽泛以至于有太多结果。与此同时，语义搜索就是要理解搜索者在搜索框中输入了什么。换句话说，有了语义搜索，我们在搜索者所在的地方遇见他们，而不是要求他们在我们所在的地方遇见我们。

输入查询放宽和查询范围。

通过同义词、查询词移除和查询范围界定等技术，搜索引擎让搜索者马上找到正确的内容。我们避免遗漏那些不会出现的相关信息，并且忽略那些不相关的信息。

查询放松和范围界定与精度和召回的概念紧密相关。Precision 是返回的结果是否相关的度量，recall 是返回的结果是否相关。提高召回率的一个具体方法是通过查询扩展。

## [](#query-expansion)查询扩展

查询扩展就是扩展查询匹配的内容，希望得到更好的结果。搜索引擎可能应用查询扩展的主要原因是由于没有查询扩展的“基本”搜索结果对于搜索者来说是不令人满意的。

在本系列中，我们已经看到了一些扩展查询的方法。 [错别字容忍、复数忽略、词干化和词条化](https://www.searchenginejournal.com/nlp-nlu-semantic-search/444694/?itm_source=site-search&itm_medium=site-search&itm_campaign=site-search) 都是提高检索召回率的方法。

我们已经看到的那些查询扩展方法是搜索的基石，但是其他的查询扩展方法也同样重要。

其实《搜索引擎杂志》2008 年的一篇文章就讲过 [Google 如何进行查询扩展](https://www.searchenginejournal.com/what-is-google-query-expansion-cases-and-examples/7924/) ！这篇文章不仅讨论了词干和错别字容差，还讨论了翻译、单词删除和同义词。

## [](#synonyms-and-alternatives)同义词和替代品

乔治·奥威尔在他的小说《1984 年中引入了 *新话* ，这是有原因的，也是为什么它在一个关于生活完全被控制到平淡无奇的故事中引起了共鸣。语言的丰富性是由用不同的单词和短语说同样的事情或几乎同样的事情的能力驱动的。“伟大”可以是“令人敬畏的”，“低成本”是“便宜”的近邻

与此同时，这些不同的单词可以帮助我们更准确地指代除了最小的方面之外都相似的项目。事实上，这些差异有时非常小，以至于这种精确性反而会滋生混乱，使我们不太可能找到我们想要的东西。想要摇椅的顾客可能不知道是否要寻找“摇椅”、“摇椅”或简单的“椅子”

这就是同义词和替代词提供价值的地方。它们帮助我们在搜索结果中扩大回忆。

同义词和替代词相似，但不相同。(你可以说它们不是同义词。)同义词是指表示同一事物的两个单词或短语。替代词指的是相似但有一定程度差异的单词或短语。

### [](#synonyms)同义词

通常，同义词通过同义词列表进入搜索引擎。这些列表可以来自预定义的列表，例如通用电子商务术语。预定义列表的问题在于，适用于一家公司搜索引擎的同义词不一定适用于另一家公司。快问:什么是控制台？你可能会立即想到视频游戏，但其他人可能会想到汽车或音乐。

由于这个原因，许多同义词列表都是内部创建的。在搜索实现过程的开始，内部主题专家会考虑所有可能是其他单词同义词的单词，并将它们添加到搜索引擎配置中。(实际上，这通常是对发生的事情的理想化看法。创建同义词列表的人通常不是主题专家，而是实现搜索引擎的人。)

一般来说，这个初始列表将提供一个很好的起点，但肯定会有遗漏的同义词。发现你的搜索者会使用哪些术语的唯一真正方法是让他们去搜索。

#### 使用分析发现同义词

您将很快在您的分析查询中看到可以使用新同义词的内容。这些查询返回 0 个结果，表明搜索者正在寻找他们找不到的东西。

现在，并不是所有这些查询都会给你一个新的同义词。有时候，搜索者在寻找你没有的东西。尽管如此，你会看到这样的查询，你会立刻想到，“哦，我们有那个”和“我不知道人们会这样问。”

有时查询会返回结果，但不是搜索者想要的。如果你追踪所谓的“搜索优化”，这些查询也能给你同义词的灵感搜索细化表示搜索者何时搜索，然后再次搜索。这意味着搜索者第一次没有找到他们想要的东西，并再次试图找到更好的东西。搜索“Dell laptop”并接着搜索“Dell notebook”的搜索者说“laptop”和“notebook”是相关的，但是“laptop”的搜索结果是不充分的。

虽然手动浏览你的分析来寻找这些趋势没有错(慢慢进入工作周可能是一个好的活动)，但如果你有一个主动为你寻找这些趋势的系统，你会更有效率。有些系统甚至会代表您应用同义词，但这并不总是有用的。人类可以发现没有显示有效同义词的细化，或者可以看到系统正在建议不正确的同义词类型。

#### 同义词的类型

没错:同义词有不同的类型。这个概念乍一看似乎很奇怪，但它可能与大多数人对他们的看法相差不远。

“双向”是第一类同义词。这些同义词可以直接相互替换。“小”和“迷你”是彼此的双向同义词。然而，这些词不需要完美的替换，但可以足够接近，人们可能会用一个替换另一个。例如，“绳子”和“绳子”并不描述完全相同的东西，但它们足够接近，是值得的双向同义词。

考虑通过使用同义词创建的查询可能是有用的。如果我们对“小奶酪披萨”进行查询，并将其展开，您现在可以将该查询想象为“(小或迷你)奶酪和披萨。”

“单向”是同义词的下一种类型。这种类型通常用于指代属于更大类别的对象的单词。“PlayStation”是一种视频游戏“控制台”，但“控制台”不是一种“PlayStation”。如果在搜索配置中添加一个单向同义词，那么每当有人搜索“控制台”时，PlayStations 就会显示出来

为什么这两个术语之间没有一个双向同义词？因为双向同义词是可传递的。如果术语一和术语二是双向同义词，术语二和术语三是双向同义词，那么术语一和术语三是双向同义词。在一个更直接的例子中，“PlayStation”和“console”以及“Xbox”和“console”作为两组双向同义词将意味着“PlayStation”和“Xbox”是同义词，搜索者在搜索 Xbox 时会看到 PlayStation，反之亦然。

“替代修正”是最终类型。当单词之间不能精确替换，并且您希望精确匹配的单词比替换单词显示得更高时，可以使用这些选项。例如，你可能会说“裤子”是“短裤”的替代词，但是当有人搜索“短裤”这个词时，所有的短裤都应该比裤子高。

所有同义词类型，就其本质而言，都是扩展回忆。然而，对精度的影响应该是最小的，因为这些同义词是指向相似概念的“指针”。总的来说，你会期望最终用户有更好的搜索体验。

## [](#query-word-removal)查询词移除

有时搜索者会使用不返回任何内容的查询，因为该查询过于具体，或者使用了任何记录中都不存在的单词。从查询中删除一个或两个单词，就会返回非常好的结果。这是使用查询词删除的好时机。

#### 停止字

或许最常见的查询词移除步骤是移除“停用词”停用词是非常常见的词，为交流提供意义，但对检索没有帮助。诸如“the”或“an”之类的词可以删除原本很好的匹配。这在更面向自然语言的查询中更常见，比如语音搜索查询。

在产品搜索引擎上搜索“一件橙色衬衫”就是一个例子。如果搜索引擎搜索标题、颜色和类别，可能会有大量记录将“衬衫”作为类别，将“橙色”作为颜色，但没有一个记录包含单词“an”现在，真的，单词“an”在这里提供任何有用的信息吗？不，它没有，搜索引擎可以安全地删除它，而不会损失任何精度。

与同义词不同，你通常不想创建自己的停用词表，大多数搜索引擎都为每种语言内置了停用词表。但是，有时您会希望扩展内置列表，例如，如果您有一个非常常见的行业术语，它不会为查询提供任何值。

#### 如果没有结果，删除单词

然后是所有单词都有价值的查询，但是一起搜索它们不会返回任何结果。通常，搜索者会对不太精确的结果感到满意，以此来换取更高的回忆率。在这些情况下，我们希望删除单词，这样我们就可以将结果呈现在用户面前。

有两种主要的方法可以做到这一点:让所有的查询单词都可选，或者从查询中删除单词。

如果您在没有结果时将所有查询词设为可选，则您依赖于这样的假设，即匹配更多词的记录更相关，其他条件相同。

另一种方法是逐个删除查询词，直到找到匹配的记录，或者查询中不再有词。你可以先去掉第一个单词，或者去掉最后一个单词。去除最后一个单词更常见。

让所有的查询词都是可选的，然后根据匹配词的数量进行排序通常是更好的方法，尤其是在与停用词的删除一起使用时。然而，当精度很重要时，这是一种不太理想的方法，并且您希望表明，实际上没有匹配所有查询词的结果。一个人可能会因为查询“古驰 v 领毛衣”而看到优衣库 v 领毛衣，而另一个人则认为这些结果完全不相关。

当然，另一种情况是知道哪些单词实际上为查询提供了最大的价值，并将它们标记为可选的。这在基于关键字的搜索引擎中通常是看不到的，但是已经有一些搜索引擎会对停用词采取类似的方法。例如，一些搜索引擎在过去已经试验过使用逆向文档频率，在没有停用词列表的情况下自动折扣常用词。

与同义词一样，查询词移除将再次扩大召回范围，通常不会影响精确度。因为停用词对结果没有太大的价值，所以你不会因为不包括它们而失去好的结果。类似地，当没有结果时删除单词不会降低精确度，因为没有可能精确的结果。

## [](#query-scoping)查询范围界定

我们主要研究了搜索者过于精确，搜索引擎需要扩展查询以提高召回率的情况。同样，有时搜索引擎可以理解用户意图，查询范围可以提高精确度。

搜索专家 Daniel Tunkelang 称 [查询范围](https://queryunderstanding.com/query-scoping-ed61b5ec8753) “捕捉查询意图的最有效方法之一。”他确定了查询范围的两个主要步骤。首先是查询标记，其次是范围本身。

查询标记用它们可能属于的属性来识别查询的部分。例如，“Marcia”最有可能匹配“name”属性，而“The Brady Bunch”映射到“show title”属性。查询范围采用这种映射，然后限制这些查询部分的属性搜索。搜索引擎不会在“姓名”属性中搜索“布雷迪”，也不会在“演出名称”属性中搜索“玛西娅”。

这种查询范围减少了召回，因为我们不会看到在其他属性中包含该文本的结果。然而，结果应该是我们有更高的精度，因为我们没有搜索不相关的属性。

事实上，我们可以通过已知属性值过滤结果来进一步提高精确度。这甚至不需要机器学习，因为搜索引擎可以在查询中的方面值和文本之间进行简单的匹配。这极大地降低了召回率，所以我们也可以找到一个很好的平衡，用匹配值而不是过滤来提高结果。提升后的结果往往是最匹配的，因为查询过滤匹配给你一个信号，这就是搜索者想要的。

如果你通过分析或实践经验发现，你的搜索没有达到用户意图，需要搜索“恰到好处”，那么查询扩展和查询范围是校准你的精确度和召回率的两种方法。这些方法会让应该出现的结果出现，而把不应该出现的结果排除在外。