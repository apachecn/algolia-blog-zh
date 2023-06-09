# 4 种类型的联合搜索

> 原文：<https://www.algolia.com/blog/product/federated-search-types/>

所有的搜索方法并不都是平等的。在网站上搜索越容易(也越快)，你的用户就越有动力留在网站上，浏览你的内容，成为回头客。

联合搜索是提高网站搜索可用性和性能的好方法。联合搜索是站点搜索的一种形式，它从多个数据源提取各种类型的信息，并将其呈现在一个公共界面上供用户浏览。

当联合搜索被很好地实现和设计时，它鼓励用户超越他们正在搜索的内容。他们可以浏览、发现和消费比以往更多的关于你的业务和产品的信息。此外，在网站上进行的搜索越多，公司就能收集越多关于流行产品的有价值的数据，并将其纳入关于产品路线图的决策中。

但是设计一个强大、直观的搜索功能需要选择 *右* 的方法来进行联合搜索。正确的方法取决于您的网站、当前数据的组织和存储方式，以及您的网站和业务的总体目标。

## [](#different-approaches-to-federated-search)联合搜索的不同方法

联合搜索包括两个基本过程:索引和搜索。

首先，数据被索引。索引包括收集、解析和存储数据，以实现简化、高效的搜索。对于典型的站点搜索解决方案，索引需要以特定的时间间隔更新，这取决于添加新数据的频率以及新数据变得可搜索的速度。

接下来，搜索数据。搜索过程包括查询索引，以正确的顺序返回正确的信息。

每个联合搜索工具都是基于索引和搜索的。但是根据您的业务需求，有三种不同的索引和搜索方法可供选择:搜索时间合并、索引时间合并和混合联邦搜索。

**1。搜索时间合并**

搜索时间合并(有时也称为查询时间合并)包括为您想要包含在联邦搜索中的每个数据源维护一个单独的索引。然后，要执行搜索，需要针对给定的搜索词分别搜索每个索引。您可能还需要[](https://www.algolia.com/blog/engineering/inside-the-engine-part-7-better-relevance-via-dedup-at-query-time/)通过识别从冗余数据源提取的结果来删除重复数据。最后，搜索结果被聚集以产生最终结果的列表。

#### **搜索时间合并的优缺点**

搜索时间合并的主要优点是它是实现起来最简单的联邦搜索方法。因为它不要求您为所有数据源创建中央索引，所以您可以使用每个数据源中已有的索引快速设置搜索时间解决方案。

此外，搜索时间合并可以更简单地设置，因为不需要标准化您的索引。一个索引的数据结构可能不同于另一个索引的数据结构，但是搜索时间合并对两者都适用。

另一方面，使用搜索时间合并进行的搜索的性能速率往往比其他联合搜索方法慢。独立搜索多个索引效率较低的是[](https://www.algolia.com/blog/engineering/inside-the-algolia-engine-part-1-indexing-vs-search/)。如果一个索引响应特别慢，整个搜索就会延迟。最后，为汇总结果列表建立一个令人满意的相关性可能非常具有挑战性，因为这涉及到比较苹果和橙子

### [](#2-index-time-merging)**2。索引时间合并**

联合搜索的另一种方法是索引时间合并。使用这种方法，您可以为所有数据源创建一个中央索引，然后解析该索引以执行搜索。

#### **指数时间合并的优缺点**

因为你只需要搜索一个索引，索引时间合并通常会比搜索时间合并更快。这是索引时间合并的主要优点。索引时间合并还允许您包含没有自己的搜索功能的数据源，因此不能与搜索时间合并一起使用。

索引时间合并的主要缺点是需要更多的努力来实现。您不能解析索引集合，而是必须为所有数据源创建一个中央索引，并在数据源发生变化时更新该索引。另外，如果您的一些数据源的格式与其他数据源不同，您需要将所有数据标准化为相同的格式。类似于搜索时间合并，它仍然需要你为所有不同类型的内容决定一个独特的相关性策略，这不是最佳的。

### **3。混合联邦搜索**

您还可以通过将搜索时间和索引时间合并中的一些方法结合起来，采用一种混合方法来进行联合搜索。

对于混合联邦搜索，您可以为尽可能多的数据源创建一个中央索引，就像索引时间合并一样。但是，如果您的数据源不容易用中央索引表示，那么您可以为它们维护单独的索引。当您执行搜索时，您会搜索所有的索引—您的中央索引，以及存在于中央索引中未出现的任何其他数据源的附加索引。基于所有索引的搜索结果被聚合以创建一个最终列表，就像搜索时间合并一样。

#### **混合联邦搜索的优缺点**

通过减少需要搜索的索引数量，混合联邦搜索提供了比搜索时间合并更好的性能。但是，与此同时，它并不要求您为所有数据源创建一个索引。

混合联邦搜索技术的主要缺点是，因为仍然有多个索引要搜索，所以性能通常比只有一个索引时要慢。

### [](#4-the-federated-search-interface)**4。联邦搜索界面**

这种方法与搜索时间合并方法类似，但它不是将结果聚集在一个结果列表中，而是在一个统一的界面中为每种类型的内容呈现一个结果列表。

#### **联合搜索界面的优缺点**

联合搜索界面不仅提供了卓越的性能，还允许网站所有者独立微调每种内容类型的相关性。然而，实现这些好处确实需要一些深谋远虑。最终界面的设计应该反映网站所有者希望访问者拥有的体验，因此需要一些战略规划。此外，并不是所有的搜索网站工具都能显示联合搜索界面。因此，网站所有者需要确保他们的网站搜索解决方案能够在不同的索引中索引不同类型的内容，并以最用户友好的方式呈现这些信息。

## [](#how-to-choose-a-federated-search-approach)如何选择联合搜索方式

有四种不同的联合搜索技术可供选择，您如何决定哪一种最适合您的业务需求？有几个因素需要考虑。

### [](#data-environment)**数据环境**

你应该考虑你拥有的数据类型，以及哪些工具可以用来操作、索引和搜索它们。如果您的数据源包含各种各样的格式，那么搜索时间方法通常最有意义。如果您的每个数据源都可以很容易地独立搜索，那么搜索时间也会更长，如果数据的结构一致，情况就是这样。另一方面，如果可以很容易地将所有数据标准化到一个数据库中，那么索引时间合并是一个更好的解决方案。但是，如果您有一系列不同的内容形式，并且您的搜索解决方案支持联合搜索界面，那么这应该是首选方法。

### [](#developer-needs)**开发者需求**

您的开发人员也是决定使用哪种联合搜索方法的一个重要因素。如果您有一个大型开发团队和构建中央索引所需的资源，索引时间合并可能非常适合您。但是对于较小的开发团队来说，搜索时间合并可能是一个更实际的选择，因为它需要较少的努力来实现。如果您的开发团队在构建搜索应用程序方面没有太多经验，第三方联合搜索解决方案可能也是一个有吸引力的选择。

### [](#user-needs-and-experience)**用户需求和体验**

归根结底，搜索的主要目的是将你的内容与用户的意图联系起来。在决定采用哪种联合搜索方法时，用户体验需求应该是优先考虑的。如果用户期望异构结果的单一列表(想想 Google Drive)，搜索时间或索引时间合并是根据您的数据环境和资源做出选择的好解决方案。如果用户已经知道他们在寻找什么，但可以从额外的内容或结构化的结果布局中受益，那么联合搜索界面是正确的解决方案。

## [](#federated-search-and-algolia)联邦搜索和阿果

无论您采用哪种方法，Algolia 都能帮助您加快联邦搜索的实施。凭借极快的搜索结果、对几乎任何类型数据源的支持以及定制搜索 ui 以帮助指导用户的能力，Algolia 可以轻松地将联合搜索功能添加到您的网站中。通过[注册一个免费账户](https://www.algolia.com/users/sign_up)来亲眼看看吧。