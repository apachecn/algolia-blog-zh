# 探索搜索和索引:实时索引场景

> 原文：<https://www.algolia.com/blog/product/an-exploration-of-search-and-indexing-real-time-indexing-scenarios/>

我们并不总是写搜索的数据或内容方面，我们称之为索引。老实说，我们认为索引是理所当然的。我们说，“将您的数据发送给我们”，然后，一旦解决了这个问题，您就可以开始关注关键部分了，即构建强大的面向客户的搜索界面、提高转化率、客户参与度和目录发现。

并不是说主要写如何构建一个伟大的商业价值搜索 UI/UX 有什么错。但是，由于没有谈论 Algolia 如何索引您的数据，我们跳过了一个位于我们提供的核心的步骤，并且为您的企业创造了与您构建的搜索界面一样多的价值。

搜索索引的价值在于 它可以 **将任何和所有后台数据和文件类型转换为可搜索的数据** ，支持在全球范围内任何设备上对任何用户(客户、合作伙伴和员工)进行快速和相关的搜索。一旦将大量数据放入后端和前端之间的单一接触点，您就可以利用 Algolia 的全功能搜索& AI 在[业务](https://www.algolia.com/industries-and-solutions/enterprise/)的各个方面处理任何用例，无论是内部还是在线。

## [](#indexing-as-a-middle-layer-between-the-front-and-back-ends)索引作为前端和后端之间的中间层

在这方面，我们可以认为索引与搜索和推荐是同等的。

*   首先，您所做的一切都与我们的 [搜索](https://www.algolia.com/products/search-and-discovery/hosted-search-api/) 和 [推荐](https://www.algolia.com/products/recommendations/) 产品引用回我们的快速索引和云基础设施

*   我们的搜索速度取决于我们在服务器上索引内容和存储数据的方式

*   我们在幕后管理、发送和存储您的数据的方式是安全、稳健、可靠的，并且能够在所有 B2C、B2B 和系统对系统使用案例中充当所有系统和所有潜在用户之间的中间层

大多数公司都有一个或多个通用数据库，用于存储产品数据、销售历史、客户、库存和财务信息等业务关键内容。Algolia 不是这些数据最初存储的地方。Algolia 不是一个通用存储数据库。它也不是管理特定业务功能的应用程序，如客户关系或产品和库存管理。

我们并不期望每笔销售都送到阿尔戈利亚。我们不提供这种搜索。这是专用 POS 系统的领域。但是 Algolia在后台办公室中有作用吗:它被构建来与每一个真实的来源接口，以提供由 *任何* 后台办公室系统馈送的快速且相关的可搜索数据集。其云基础设施提供了一个可靠、安全的可搜索数据层，位于后台数据源和任何向用户提供数据的前端之间。

阿果的力量在于帮助 *表面* 这些后台系统中的内容，将用户引向原始信息。例如，Algolia 可以用来存储足够的产品信息——价格、图像、描述、可用数量和受欢迎程度，以帮助客户购买或员工管理。在这个用例中，点击一个产品应该把用户带回一个产品页面，这个页面的细节直接来自原始数据源。

## [](#instantaneous-search-fast-indexing)瞬时搜索，快速索引

为了满足所有前端搜索需求，Algolia 提供一个坚实的索引基础是非常重要的。我们将很快发布一系列关于“无头搜索”的文章，在这些文章中，我们将讨论我们的 API 优先索引如何将后端与前端分离，以创建可搜索数据的中间层。通过订阅我们的新闻简报 ，率先了解这些文章以及其他当前和未来的内容 [。](https://go.algolia.com/subscription_newsletter/)

让我们来分析一下 Algolia 的搜索和索引选项与产品之间的差异。

### [](#search)搜索

我们对 Algolia 进行了设计和优化，以提供 [**即时搜索结果**](https://www.algolia.com/industries-and-solutions/ecommerce/) ，因此在输入信件和获得即时回复之间没有延迟。我们的 SLA 是确保搜索在 99.99%的时间内可用。以下是我们软件承诺和提供的一些细节:

*   实时搜索
*   相关性
*   高级功能
*   人工智能相关性
*   前端 UI/UX 库
*   商业利益——增加转化率和客户参与度

### [](#indexing)标引

每一次搜索的背后都隐藏着一个简单的索引框架——一个简单的调用就能以完全 [灵活的格式](https://www.algolia.com/blog/engineering/facets-and-faceted-search-making-every-attribute-count/) 发送来自任何系统的任何数据。

*   灵活性——我们可以为搜索目的构建任何数据
*   大小——当托管在我们云架构中的多个实例上时，我们提供无限的数据容量
*   安全
*   全球可用
*   可靠 SLA，始终可用

### [](#search-vs-indexing)搜索 vs 索引

*   搜索优先–每当请求搜索时，搜索优先于任何索引
*   索引旨在返回速度最快、信息丰富且可随时显示的搜索结果
*   良好的索引实践可以在不到 1 秒或长达 5 到 10 秒的时间内处理数据

为什么我们让搜索优先于索引？两个主要原因:

*   为了满足用户的期望，即当他们键入查询时会立即得到结果
*   不要错过任何一个搜索请求，因为每次搜索都是一次潜在的转化

## [](#a-typical-search-and-indexing-use-case)典型的搜索和索引用例

典型的搜索和索引过程如下:

1.  用户搜索一个公司的产品目录，最终想要转化(购买)。
2.  用户在线或在商店购买产品。
3.  在线或店内 POS 应用程序处理交易，并将数据发送到后端服务器。
4.  后台销售软件(POS)存储交易。
5.  根据公司的使用情况，后台会定期更新 Algolia 中的数据。也就是说，后台 POS 系统向 Algolia 发送新产品或更新的产品数据，如可用性和受欢迎程度数据，从而在用户不断输入搜索查询时影响向用户显示的新内容。

注意，重索引需要是 *常规* ，而不是每笔买卖。一次销售不会改变目录。一天之内很少会发生重大变化，更不用说几分钟了。价格、可用性、促销活动和自定义排名(如受欢迎程度)需要时间来调整。

因此，我们的客户最关心的是确保 *所有的* 搜索都是成功的和即时的，并且后端更新足够定期和响应，以便及时考虑重大变化。通常，这意味着每 30 分钟，甚至 1 小时，或者一整夜。每个公司都为其不同的用例选择最佳的时间框架。

然而，有一些活跃的时间框架，公司需要 10 秒钟的更新，甚至是即时更新。让我们来讨论这些独特的用例。

## [](#advanced-search-and-indexing-use-cases)高级搜索和索引用例

我们先来看一个定义再开始吧。

**实时** 可以表示:

*   一旦在现实世界中发生，就会被考虑(在搜索中)的实际更新。这是一个股票市场的场景。
*   更新发生后每 X 秒 考虑一次 **，其中 X 通常是一个较小的数字。**

以下用例将需要其中一个。

### [](#fast-indexing-in-a-crisis)临危不乱

这场危机始于一艘集装箱船陷入苏伊士运河的河床。它不仅无法运送自己的货物，还阻碍了其他集装箱船，因此也阻碍了世界上很大一部分货物的供应。在销售方面，世界各地的电子商务公司必须立即重新考虑他们的库存，以避免缺货订单。他们还不得不寻找替代品，调整促销活动，以保持在线目录像危机前一样吸引人。当他们的 IT 部门重新索引在线目录以删除被屏蔽的商品时，他们的采购员开始采购替代商品并重新考虑他们的促销活动。

在等式的另一边，批发供应商必须通过从他们的 B2B 目录中删除被封锁的商品来匹配新的需求，并将不同的产品推给他们的买家。

索引显示为三个部分:

*   移除被阻止的项目
*   添加新项目
*   调整他们的促销活动

### [](#fast-indexing-in-a-sudden-surge-of-buying-and-selling-e-g-black-friday)快速指数化在突然激增的买卖中(如黑色星期五)

另一种需要快速索引响应的情况发生在黑色星期五和圣诞节结束之间的 5 周内。在这种情况下，公司需要不断监控他们的库存，并保持领先于市场，以确保他们能够履行每一个订单，并通过每次搜索和促销，以最好和最重要的商品响应客户的需求。在这种情况下，他们相当频繁地进行监控，有些公司一天要监控多次。

### [](#fast-indexing-in-a-constantly-changing-online-catalog-e-g-a-marketplace)在不断变化的在线目录(如市场)中快速索引

在这个场景中，我们有一个大型市场，独立供应商不断更新他们的库存。在大多数情况下，这些供应商并不拥有全部的物品库存；相反，他们拥有每种产品中的一种。因此，一次销售可能会导致产品无法销售，因此他们需要在销售完成后立即移除物品。一些市场允许用户暂时保留添加到愿望列表中的对象。

每个市场网站都想出了一个策略来管理这种不可预测且快速变化的缺货和产品持有量。以下是一些策略:

*   UI 明确提醒用户是否有货(在商品旁边显示“只剩 1 件商品”)。
*   如果用户将商品放入购物车，用户界面允许供应商暂停该商品。
*   用户界面明确地告诉其他用户某个项目是否处于暂停状态。他们可以将其添加到愿望列表中，并在该项目变得免费或不可用时收到通知。

易贝增加了一个额外的复杂性，物品的买卖通过拍卖和出价来改变价格。处理这种实时更新的方式取决于用户界面。然而，这种情况非常接近于需要对搜索 *和* 索引进行实时数据处理。让我们仔细看看最后一个用例。

### [](#real-time-indexing-in-a-real-time-market)实时行情中的实时指数

这里的情况是，每次供应商对产品(尤其是价格)进行更改时，他们都希望用户立即看到这一更改(以及任何相关的计算)。因此，它与典型的股票市场工具没有什么不同，你可以看到价格像闪烁的灯光一样变化。考虑一个在股票价格变化时买卖股票的自动化交易工具。任何延迟都会影响系统的竞争力，并可能造成巨额损失。

人们可能会怀疑是否有任何 B2C 场景需要实时索引。价格变化这么大，这么快吗？大量的人和系统基于最小的价格变化买卖商品吗？

也许 B2B 需要显示即时价格变化更合适。供应商很有可能实时出价高于对方。

在任何投标领域，我们可以将易贝加入其中，拥有最快的索引响应时间至关重要。

这就是我们对 *快速标引* 的用心之处。任何搜索引擎的索引速度会和它的搜索功能一样快吗？也就是说，虽然搜索引擎提供商在合同上承诺在用户键入时显示即时结果，但它不以同样的方式承诺“即时”或接近实时的索引。这是因为，为了实现实时搜索(以毫秒为单位的搜索)，您必须以某种不可避免地需要时间的方式来索引数据(1 到 10 秒，取决于索引的大小和索引请求中的更新次数)。

Algolia 重视比数据库更快的搜索(毫秒),代价是比数据库更慢的索引过程(秒)。正如在上面的高级用例中所看到的，即使在危机或不断变化的库存/定价环境中，我们的索引引擎的速度也是可靠的、反应灵敏的，并且超出了预期。

## [](#next-readings)下一个读数

本文提供了标准和高级索引用例的高级概述。我们的下一篇文章将带您了解[索引最佳实践](https://www.algolia.com/blog/engineering/search-indexing-best-practices-for-top-performance-with-code-samples/)和标准索引过程的实现细节。接下来是一篇关于如何在高级用例中优化索引的文章。

我们剩余的文章将为我们讨论的一些高级索引用例提供前端和后端代码，从实时定价开始。

要了解 Algolia 强大的索引和云基础设施如何转变您的数字战略， [免费注册](https://www.algolia.com/users/sign_up) ，亲自体验。或者 [今天就从我们的搜索专家那里获得一个定制的演示](https://www.algolia.com/demorequest/) 。