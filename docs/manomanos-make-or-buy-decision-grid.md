# 马诺马诺的“制造或购买”决策网格

> 原文：<https://www.algolia.com/blog/customers/manomanos-make-or-buy-decision-grid/>

![Pierre Fournier](img/45ccd3a3156881ebd7432ee61c736208.png)

**马诺马诺首席产品官皮埃尔·富尼埃的客座博文**

当我们能在我们的网站上展示客户时，这总是很特别的。今天，我们很高兴有一个来自马诺马诺首席产品官皮埃尔·富尼埃的客座博文，“所有 DIY 和园艺的一站式商店”——直接送货上门。作为英国和欧洲 DIY 消费者的领先市场，ManoMano 的网站需要执行、扩展并帮助买家和卖家找到彼此。今天 Pierre 的文章首先出现在[媒体](https://medium.com/manomano-tech/manomanos-make-or-buy-decision-grid-3e82eb8c0b4a)上。请与您的网络分享 Pierre 的智慧和见解，尤其是在他们考虑构建还是购买新技术时。

随着 SaaS 编辑在科技界的崛起，你现在有了一个可以满足任何需求的工具(搜索、市场、聊天、内容管理、支付……)。如果您选择了正确的工具，它可以成为一个不可思议的加速器，但当事情出错时(迁移、集成、数据所有权……)，它也会变成一场噩梦。**因此,“制造还是购买”的决策成为产品经理工作中最重要的决策之一。**

以下是我们在马诺马诺评估标准的总结(MM):

*   **数据所有权**属于 MM，不用于共同改善工具
*   **功能的商品化**并没有使其成为 MM 的战略
*   **定制**允许我们根据 MM 的特殊需求调整工具
*   向后兼容性让我们可以自由地重新考虑我们的选择
*   **编辑的生存能力**允许长期合作
*   如果使用量增加，成本不应该激增

作为奖励，我们还分享了一些在为购买策略选择工具时成功运行 RFP(征求建议书)的技巧。

![Make vs Buy: ManoMano and Algolia ](img/0e19de93568f1f928ec9f0a8f98a8ee6.png)

## [](#preliminary-thoughts-about-%e2%80%9cmake-or-buy%e2%80%9d-strategy)关于“制造或购买”战略的初步想法

做决定或购买决定可能是非常艰难的决定，我认为这种情况在未来会越来越多。在我职业生涯的初期，你几乎没有 SaaS 工具(更不用说互操作性问题了)，你必须自己开发几乎所有的东西。以下是根据 10 年来参加 buzz、trends 和参与 RFP(提案请求)的经验，对做出购买决定的一些想法…

*   **是否有新的“自制和购买”选项？**D2D 的崛起(开发人员对开发人员)基础技术层将继续发展，并为纯粹的“现成”解决方案提供替代方案，开启一条“制造和购买”的新路。例如，Twilio 提供了构建聊天等交流工具的基础。
*   **开发内部解决方案仍然有意义:**任何第三方工具功能通常只使用几个范围(假设 20%，甚至可以更少)。这就是为什么即使在今天，开发内部解决方案仍然是可能的。让我给你举个例子:我成立了一家食品科技公司，允许网上订购。我们花了 18 个月的时间来构建一个像样的解决方案。我们的一个同事在不到两周的时间里为一个餐馆老板构建了一个完美的解决方案…另一个主张决策的标准是成本:当量变大时，现成的工具可能就不那么有趣了。
*   **您的资金将主要用于营销和销售:**在第三方工具中，很大一部分成本通常用于资助编辑的营销和销售…您必须意识到这一点。Zoho 提供了一个很好的[的例子](https://www.zoho.com/perspectives/pricing.html)，一家公司在产品上投资很多，而不是在销售和营销上(相比于像 Adobe 或 Salesforce 这样的美国巨头)。根据 Zoho 的说法，高达 50%的收入可以分配给销售和营销…从长远来看，将这笔钱投资到产品上可以产生很大的影响！
*   **最佳策略可能变得更有意义:**拥有几种专业工具而不是一劳永逸是人们通常花费大量时间做出的另一个决定。请记住，大编辑(通常是提供一体化解决方案的人)通常通过外部收购来开发他们的产品。将新收购的产品集成到现有的产品套件中是一项非常艰巨的任务，需要很长时间…有时这种情况从未发生过！因此，一体化解决方案最终可能会成为平庸的最佳选择。此外，API 现在是一个标准，简化了几种产品的集成(此外，如果你使用像 [Segment](https://segment.com/) 这样的数据中心)。
*   **没有完美的工具:**适应工具而不是让它适应你自己的需要，总是抱怨这不是你本来会做的方式。否则，开发您的内部解决方案！请记住，编辑除了他们的软件专业知识之外，还通过他们拥有的几十个客户开发了过程专业知识。通过购买第三方工具，您也可以从这一流程专业知识中受益。

## [](#criterion-1-data-ownership-belongs-to-manomano-and-is-not-mutualized-to-improve-the-tool)标准 1:数据所有权属于 ManoMano，不用于共同改善工具

这可能是最具战略性的标准之一。通过该工具的 MM 数据不应该被用来改进编辑器的工具和潜在的竞争对手的表现。工具的价值应该来自算法本身或者工具提供的特性。

例如，ManoMano 使用 [Algolia](https://www.algolia.com/) 为其搜索提供动力。我们选择阿尔戈利亚有两个主要原因。他们的相关性算法将总是比我们现在能够做的更好，并且没有利用我们的数据来改进。此外，与弹性搜索(之前我们用于搜索的技术栈)相比，他们的界面使开发者或产品经理更容易改变相关性规则。

然而，我们拒绝了另一个提供查询聚类的 SaaS 解决方案，因为他们的算法会利用我们的查询数据来改进他们自己的聚类，这对我们的竞争对手有潜在的好处。

## [](#criterion-2-commoditization-of-the-feature-does-not-make-it-strategic-for-manomano)标准 2:功能的商品化并不能使其成为马诺马诺的战略

当 MM 的需求与行业中的其他人一样时，重新开发解决方案就没有价值了，因为它不会带来额外的价值。我们更喜欢将我们的技术资源分配到开发不同的软件上。对于 Algolia 来说，相关性，或者更确切地说是文档搜索，在语义基础上在每个行业都遵循相同的规则(在下一段中，你会看到行为相关性在我们的 DIY 行业中是不同的)。你应用相同的词干规则，停用词删除，使用相同的算法(TF-IDF)，你有相同的速度需要回答一个查询…

对我们来说，一个反例可以是我们选择内部开发的 CMS(内容管理系统)(即使我们求助于低层次的现有砖块，如 WYSIWYG 编辑器、角色和行政管理)。它主要用于提供提示表，以帮助我们的用户选择正确的产品。因为我们希望将它连接到我们的目录(产品建议)，连接到我们的分类(重用我们在过滤器中创建的属性，例如从提示表中解释它们，并允许我们的用户在浏览提示表时缩小产品范围)。

你可能需要定期重新考虑市场，因为变化发生的速度很快。例如，我们在 2016 年提前通过社区提供聊天建议。当时没有令人满意的解决方案，所以我们决定在内部开发一个专用平台。3 年后，市场已经成熟，现成的工具已经可用。后退有多难，我们不得不做出这个决定，因为转移到第三方工具上会大大加快关键功能的发布。这将允许团队在这些基本功能的基础上专注于更具战略性的额外功能。这就把我们带到了下一个标准:定制。

## 标准 3:定制允许我们调整工具以适应 ManoMano 的特定额外需求

我们关注的一个关键点是我们调整工具的能力。一般来说，我们 80%的需求是与我们行业的其他竞争对手共享的，并且可以通过现成的工具来解决。但是，出于战略考虑，我们通常还有 20%的特定需求。因此，我们必须能够在第三方工具的基础上开发这些特定的功能。它通常依赖于使用我们的数据来个性化用户体验(搜索、建议……)。因此，以编程方式管理该工具(通过 API)的能力至关重要。例如，Algolia 允许我们通过 API 覆盖原生排名算法，使我们能够基于行为数据提供个性化结果。Iadvize 提供了利用 ManoMano 的数据(如产品推荐)定制本地小工具或在聊天基础设施上添加我们自己的计费系统的机会。

## [](#criterion-4-backward-compatibility-keeps-us-free-to-reconsider-our-choice-after-a-few-years)准则 4:向后兼容让我们在几年后可以自由地重新考虑我们的选择

向后兼容性是一个重要的标准，因为事情会变化得非常快(参见上面的聊天例子)。新技术可以产生阶跃变化(例如，当 Nosql 技术出现时，见数据库管理),新编辑可以从中受益，在短时间内产生大的变化。这就是为什么你需要能够以合理的成本拔掉一个解决方案(它总是需要努力)。当然，您需要能够取回您的所有数据(因为这是一项需要时间来重建的重要资产，请参见数据所有权部分)，并且您需要尽可能多地限制专用于该特定工具的开发。你花越多的时间和精力编写专用于工具定制的代码，你就越不能重用它。然而，如果您构建定制的内部 API 来调整该工具，您应该能够轻松地重用它们，对 transferts 格式进行一些更新。同样，在我们的 Algolia 例子中，如果我们想要重新内部化搜索，我们为查询重新排序构建的所有代码都可以重用。

## [](#criterion-5-viability-of-the-editor-allows-a-long-term-collaboration)准则五:编辑允许长期协作的生存能力

当你的公司达到临界规模时(ManoMano 是欧洲 DIY 的在线领先平台)，你必须确保你的合作伙伴在 3 年内仍会在那里。因为您将投入时间和精力来集成其解决方案。与此同时，风投们每个月都会资助几家科技公司，这些公司会来看你，假装它们是下一个大事件，给你带来疯狂的竞争优势。有些人可能会死，但大多数人会在两年内死去。
这是否会妨碍你与开发尖端技术但尚未形成规模的年轻初创公司合作？我会说你可以，但前提是:

*   市场上不存在其他选择(例如，我们选择与一家年轻的初创公司合作延期付款，因为没有其他编辑存在)
*   风投的支持足够强大，足以确保至少 2 年的发展(我建议该公司至少处于 B 系列的创始地位)

这需要双方利益相关者表现出非常成熟的行为。客户不能拆整个路线图，否则编辑器将无法开发。编辑必须非常透明，能够拒绝一些功能，并在其经济可行性受到威胁时发出警告。

## [](#criterion-6-costs-shouldn%e2%80%99t-be-exploding-if-usage-grows)标准 6:如果使用量增加，成本不应激增

同样，这一项对大公司来说是有意义的。作为一家初创公司，你的销量会很低，所以成本不是太大的问题。在马诺马诺，我们的月访问量达到近 5000 万独立访客。要知道大多数解决方案都是按量计费的，这在某些时候会变得非常昂贵。这通常是公司重新内部化第三方工具的原因之一。这并不意味着解决方案必须便宜。我们知道一个产品团队(项目经理、开发人员、设计师……参见本文[的](https://medium.com/manomano-tech/why-do-all-tech-companies-converge-towards-the-same-product-organization-manomanos-case-d6f235743ae2)了解我们的比率)每年大约花费 50 万€，如果这个工具让你腾出相当于一两个功能团队的时间，这意味着你每年可以支付高达 100 万€。要带来经济价值，应该少 30 到 50%。还考虑到自己做需要维护，与第三方工具相反，你可能不会从最新的技术更新中受益，等等。与编辑协商也是关键，尤其是当工具基于每卷时的阈值。体积越大，价格应该越便宜*边际*。

我们就 PIM 解决方案(产品信息管理)进行了多次讨论。PIM 在许多行业都很常见，功能总是相同的，现成的解决方案是存在的。但最终我们决定自己制作，因为我们认为这是一项战略资产(高质量的数据和产品信息)，而且与我们向卖家收取的佣金相比，解决方案的成本会相当高。

## [](#bonus-how-to-run-a-successful-rfp-to-select-a-tool)奖金:如何运行一个成功的 RFP 来选择工具？

在选择第三方工具时，公司通常会经历一个 RFP(提案请求)流程，解释他们的需求、他们当前的堆栈、他们需要的功能……我建议尽量简化。以下是我的建议:

**1/专家应该协助最终用户，而不是相反**。事情通常是这样发生的:来自 IT、产品甚至采购部门的项目经理有权负责运行 RFP。他将对一些最终用户进行几次采访。然后他会写决策表，衡量每个标准，采访编辑…我认为这是错误的。应该相反:最终用户应该是 RFP 的核心，由专家(架构师、产品经理、项目经理、开发人员……)支持。您应该从最终用户组中指定一个人作为项目经理。
**2/让尽可能多的人参与每辆受影响公交车的 RFP** 。我知道这听起来违背直觉(我们通常试图让最少的人参与进来以保持敏捷)，但是通过使用例如[释放结构](https://www.liberatingstructures.com/)格式，你应该能够做到。它将通过以下方式为您节省大量时间:

*   增加工具符合操作用户需求的可能性
*   减轻未来用户的负担(而不是像“这是我们选择的新工具，我们可爱的 150 个客户服务代理对您来说太棒了！让我们给你解释一下为什么！”)

**3/尽可能通过概念验证测试解决方案。来自编辑器的销售代表经常撒谎(无意识地)，因为他们离技术团队很远，所以你必须在真实条件下测试该工具。有些人会说这需要时间。确实如此，但比实现错误的工具要少。最大限度减少花费时间的方法是大幅缩小范围。通过测试该解决方案，您将快速评估技术文档、API、技术员工的质量以及工具的可用性…**

**4/选择构成交易破坏者的 3 个关键标准。**不要在一百个标准需求网格中陷入混乱。你很容易陷入一个无休止的加权评分决策网格中。即使它能让你感到放心，它也是没有用的，因为你可能会错过将这个选择变成一个大错误的关键特征。

## [](#final-thoughts)最后的想法

在每个公司内部，技术资源都是有限的。相反，商业创意是无限的。“购买”策略可以减轻对技术的依赖，尤其是对销售和营销的依赖，并帮助企业更快地发展。至少一开始是这样。如果做得不明智，几年后可能会变得一团糟，您最初获得的所有灵活性可能会在无休止的迁移和改造中丢失。所以不要急着做决定。此外,“制造或购买”策略也将取决于你的公司 DNA 和雄心。你是亚马逊那样的科技公司吗？还是主要靠营销？马诺马诺本可以使用像 Mirakl 这样现成的工具来建立自己的市场。这样会更快。但是当数量变得如此之大时，工具的成本就会成为一个真正的问题。我们知道，如果我们想建造独一无二的东西，我们必须靠自己。

> 如果你想加入马诺马诺的产品团队，请随时申请[职位，我们在每个级别都有空缺职位(如果没有一个“官方”职位符合你的需要，仍然申请精确你正在寻找你想要的职位)](https://jobs.lever.co/manomano?department=PRODUCT)

要了解 ManoMano 如何使用 Algolia，请[阅读这里的故事](https://resources.algolia.com/customer-stories/manomano)