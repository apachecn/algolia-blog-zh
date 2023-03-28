# 为 Jamstack 选择 API-Algolia 博客

> 原文：<https://www.algolia.com/blog/engineering/choosing-your-apis-for-jamstack/>

所以你想使用第三方 API 来构建你的网络应用。给你这么多选择，你怎么选？

关于 [Jamstack](https://www.netlify.com/jamstack/) 的美妙之处在于，除了提升性能和可伸缩性，它还允许你使用任意数量的第三方 API 来构建你的 web 应用。结果是，你可以为每一项工作插入一流的产品，并在每个专业领域利用持续创新；在某种程度上，这是一种分拆。

考虑实现 Algolia，而不是构建一个定制的全文搜索模块，或者实现 Contentful，而不是处理托管在您必须维护的服务器上的 CMS，或者使用 Netlify 的无缝开发工作流，而不是自己编译源代码并通过 FTP 上传到 web 服务器。此外，这种模式允许您在为堆栈的任何部分找到更好的解决方案时，轻松地切换出单个服务。

当然，随着选择而来的是责任:在有这么多选择的情况下，你应该如何选择要使用的解决方案？

在本帖中，我们将分享为项目选择 API 时需要考虑的 5 个标准。

以下是我们将涉及的要点:
[平衡技术质量和业务需求](#Balancing-technical-quality-and-business-needs)
[API 作为解决方案](#API-as-a-solution)
[数据复杂性](#Data-complexity)
[智能 UI 策略](#Smart-UI-strategies)
[策略和支持](#Policies-and-support)

## 平衡技术质量和业务需求

您购买的服务需要完全符合您的架构，但也要与非技术利益相关方的需求保持平衡，因为这是他们将管理的事情。因此，您需要两全其美:一个拥有同样出色的文档的出色的 API，以及一个可访问的功能完整的业务仪表板，同时为两个利益相关者群体保持灵活性和控制力的平衡。

现在，当构建一个软件产品时，所有的事情都是关于权衡的。对于不太成熟的产品，您可能会发现更侧重于开发人员或业务焦点。因此，第一个要求是寻找一个在这两个领域都有能力的相当成熟的提供商，并尽可能减少这种权衡。

## API 作为解决方案

就 API 本身而言，寻找 API 不被视为服务，而是解决方案的迹象:

*   API 客户端/开发人员工具的维护情况如何，它们使您的集成变得有多容易？寻求灵活性和易用性。
*   供应商提供的功能中有多少可以通过 API 访问？
*   文档有多好？它是简单的功能规范，还是帮助你实现目标的全套资源？当一个 API 是一个解决方案时，文档将是全面的和易于使用的，有许多常见用例的代码样本。一些好的文档示例有 [React](https://reactjs.org/docs/getting-started.html) ，[Gatsby](https://www.gatsbyjs.com/docs/)，[Vue](https://vuejs.org/v2/guide/)，以及[graph QL](https://graphql.org/learn/)。除了文档的直观布局和设计之外，这些 API 还使用搜索使开发人员更容易找到她需要的资源。
*   提供商有开发者体验团队吗？在供应商的业务中有专门致力于帮助工程师在实现他们的产品时更有效率的拥护者会有很大的帮助。这表明供应商非常重视这个涉众群体。

## 数据复杂性

在添加 API 提供者时，您会希望查看数据流和部署过程中增加的任何复杂性。例如，当使用 headless CMS 时，当内容更新时，您需要触发站点的重新部署。在这种情况下，你需要寻找一个关于如何设置 webhooks 的集成指南。在 Algolia 这样的搜索 API 的例子中，当内容被创建或更改时，您需要通过管道将内容发送到搜索 API，当内容被删除时，您需要将内容移除。此外，您的内容可以来自许多不同的来源，如文章、产品等等。

幸运的是，许多 Jamstack 的提供商让这个问题变得很容易解决。一定要检查他们是否有集成到您正在考虑的其他 Jamstack 技术的工具。如果工具之间有直接的集成，那就更好了。例如，如果您正在使用 Algolia with Netlify，您可以利用 [Algolia 的 Netlify 插件](https://crawler.algolia.com/admin/netlify) 来简化上述过程。

## 智能用户界面策略

当选择 API 优先的提供商时，你需要考虑你的 UI。API 是为了在前端给你自由而构建的，它们尽量不固执于它们将被嵌入的接口。传统上，这意味着您必须构建所有的 UI。  然而，随着服务的成熟，现在很多提供商都提供 UI 组件供开发者使用。在使用服务的 API 客户端时，这些组件通常在接口中实现了最佳实践 UI。

如果你使用一个带有 UI“组件”或“部件”的提供者，就需要考虑权衡。无头方法在设计和用户体验方面提供了自由度和灵活性。使用提供商的小部件为构建前端提供了更快的途径，尽管您通常会失去一些设计定制的自由。您应该如何验证这些工具？寻找智能默认值，以及覆盖 UI 本身的能力，而不丢失组件内置的逻辑。这样，您可以从缺省值开始，并快速发展，而不必在偏离提供商的标准模式太远时重新构建一切。以 Algolia 为例:开发者有能力 [扩展小部件](https://www.algolia.com/doc/guides/building-search-ui/widgets/customize-an-existing-widget/js/#customize-the-complete-ui-of-the-widgets) 来定制 UI 并保留小部件提供的功能，甚至 [通过直接在底层库之上构建来创建定制的小部件](https://www.algolia.com/doc/guides/building-search-ui/widgets/create-your-own-widgets/js/) 。

## 政策和支持

由于您可能在您的应用程序中管理多个提供者——可能每个用例一个提供者——从管理的角度来看，您可能希望让您的生活尽可能简单。在这里，您需要考虑每个服务的一些元素:

1.  [SLA](https://blog.algolia.com/for-slas-theres-no-such-thing-as-100-uptime-only-100-transparency/)——你需要担心的最后一件事就是你的某个提供商倒闭了，但这确实发生了。在这种情况下，您应该将 SLA 视为您业务的保险。您还可以内置辅助故障转移来切换提供者。
2.  支持——文档可以让事情变得自助，但是当行动迅速时，一个小小的澄清或问题的一天延迟会让一切变得不同。确保你有一个团队，当你需要他们的时候，特别是在实施阶段。
3.  发布政策——当使用许多 API 时，确保任何一个 API 发布更新都不会影响到你的站点是很重要的。即使是 API 客户端中一个不向后兼容的小变化也会对您的实现造成严重破坏。密切关注您的提供商如何发布更新，并确保他们的 API 实际上是兼容的。
4.  安全性和合规性——为工作项目选择 API 时，确保您符合公司的安全性和隐私要求。您可能需要一个拥有 SOC2 认证的供应商，并且知道如何以符合 GDPR 标准的方式处理数据。对于电子商务项目，您可能需要研究 PCI 合规性。金融或医疗保健等监管更严格的行业有更多的要求。大多数提供商在其网站上会有一个 [安全](https://www.netlify.com/security/) 或 [合规页面](https://www.algolia.com/distributed-secure/security-compliance/) 。



作为 Jamstack 的开发人员，这是一个激动人心的时刻。您可以自由选择最适合您正在解决的问题或您正在构建的产品的 API。在未来的几个月和几年里，我们可以期待推出更多的服务。我们希望这个指南能帮助你为你的下一个项目选择正确的 API。

*关于作者*

Matt 在 Algolia 从事解决方案工程工作，之前曾在通信 API Twilio 和电子商务 and Moltin 工作过。

Sarfaraz Rydhan 是 Netlify 合作伙伴生态系统总监。Sarfaraz 与技术和商业领袖合作，通过使用 JAMstack web 架构帮助公司更好地接触客户。作为一名经验丰富的前软件工程师，Sarfaraz 利用他的技术和运营专业知识来帮助这些公司服务于新的市场，并在考虑清晰的业务成果的情况下做出技术决策。