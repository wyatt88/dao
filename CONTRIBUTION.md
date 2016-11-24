# 项目贡献指南

对于一名作风优良、品格顽强、追求完美的程序攻坚兵而言，Hack 代码项目绝对是一件无上荣光的事。DaoCloud 很荣幸能邀请您参与本项目的共同完善，您的贡献势必将带领该项目走向卓越。

不论是开源，还是闭源，一个优秀项目的发展永远都离不开优秀的**协作**。在这里，DaoCloud在大家的帮助下建立了《贡献者指导手册》，为所有的参与者阐述：如何高效的参与项目贡献。

## 话题

* [项目问题反馈](#项目问题反馈)
* [项目设计与提案](#项目设计与提案)
* [快速参与必读](#快速参与必读)
* [项目贡献指导](#项目贡献指导)

## 项目问题反馈

参与本项目的一种极佳方式，即当您遇到一个问题时，提交一份详细具体的问题报告。我们永远感激您书写良好、完整清晰的Bug反馈。

另外，项目的发展肯定会吸引更多工程师参与，在您提交一个问题反馈时，我们非常感谢您能够在问题列表中，查询是否已存在相同问题。您的此举，将会为所有参与此项目的工程师节省宝贵的时间，也在无形中提高了此项目的协作效率。

* 如果以及存在相同问题，您可以点击“订阅(subscribe)”按钮完成订阅，以便在问题更新时收到通知。
* 如果您有方法重现此问题，或者可以提供额外有可能有价值的信息，请留下您重要的评论。

交流是信息流动的过程，一个项目的完善离不开大家的参与，以及众多智慧的交流。我们鼓励所有贡献者在Github这个协作平台上完成尽可能多的交流。

## 项目设计与提案

对于项目当前的进展，我们非常鼓励您提交新的设计提案。您也可以为新的功能特性设计完整长远的蓝图。我们也非常鼓励您重构项目存在缺陷的地方，以及清理此项目的某些冗余部分。具体的此类贡献步骤与注意事项，请参阅[项目贡献指导](#项目贡献指导)。

## 快速参与必读

了解此项目势必是学习、使用、贡献此项目的第一步。为了帮助您快速参与此项目，本项目提供了以下内容帮助您迅速上手：

* 使用文档
* API说明文档
* 设计文档
* Roadmap文档

文档是优秀项目开发使用和维护过程中的必备资料。我们相信文档必定会帮助此项目提高软件开发的效率，也保证软件的质量。如您发现文档存在不完善的地方，请务必参阅[项目贡献指导](#项目贡献指导)，并完成您的贡献，我们非常感激您的参与及贡献。

随着参与程度的加深，您肯定会涉及到此项目的PR(pull request)、问题列表、milestone、标签列表。以下是这些内容的简单介绍，希望对您有帮助：

* PR(pull request):为了完善此项目，通过代码的形式提交给此项目，项目管理者会通过标签(label)的形式，对PR进行分类；
* 问题列表(issue list): 用户针对项目，总会存在各种各样的问题，用户可以通过issue list反馈，项目管理者会通过标签(label)的形式，对issue进行分类；
* milestone:项目发展过程中，往往会设定里程碑版本；
* 标签(label): 为帮助PR、issue更好的分类，项目管理者可以设定标签(label)。

## 项目贡献指导

贡献此项目的方式有很多种，此处我们主要介绍如何给项目提交PR(pull request)。

### fork 项目

Fork此项目到您的GitHub账户之下，并在您个人的代码仓库上更新内容。

Clone 在您Github账号下的本项目之后，需要完成设置remotes。为了完成最简单的贡献工作流，您可以按照以下步骤完成remotes的配置：

* origin: 您个人的fork，也就是您Github账号下的此项目；
* upstream: DaoCloud下的此项目

运行以下命令完成remote设置：

```
git remote remove origin
git remote add origin https://github.com/<您的GitHub ID>/项目.git
git remote add upstream https://github.com/daocloud/项目.git
git remote set-url --push upstream no-pushing
```

### 分支规范（branch）

为此项目提交代码贡献的前提之一，必须创建一个全新的分支，并根据您所需要完成的功能与类型来定义此分支，主要目标是帮助他人更好的理解分支的作用：

* 如果这是一个Bug修复分支，请按照下列规范命名提交分支：XXXX-something，在这里XXXX是issue的ID；
* 如果这是一个功能增强分支，请在issue list中提交一个功能增强issue来具体描述您的提案，并按照下列规范命名提交分支：XXXX-something，在这里XXXX是issue的ID；

### 提交信息规范（commit message）

提交信息是帮助代码审核者更高效知晓PR意图的信息，可以有效加快 Code Review 的流程。我们推荐贡献者使用**简明清晰**的提交信息, 我们反对**寓意不明，指代含糊**的提交信息。一般情况下，我们鼓励使用这种形式的提交信息：

* Add_xxxx：代表添加内容xxx
* Update_xxxx：更新内容xxxx
* Remove_xxxx：删除内容xxxx
* Refactor_xxxx：重构内容xxxx
* Fix_xxxx: 修复某个具体的内容xxxx

我们极度反对使用如下的提交信息，理由很简单:这样的提交信息非常不具有可读性。

* ~~fix bug~~
* ~~update~~

### PR规范

我们认为PR是一个阶段性的工作成果，PR作为代码合并的一个整体，同样需要您在可读性，可审核性方面按照相应的要求来完成。PR的主要要求如下：

* 单个PR一般只包含一个commit，特殊情况下，单个PR可以包含多个commit，但数量不能超过5个；
* PR的描述有助于代码审核者快速了解PR的性质与具体情况，我们极度不赞成内容为空的PR描述。

一个优秀完备的PR描述，拥有以下PR的形式：

```
PR 描述:
针对问题233， 此PR加入功能特性A， 为此项目实现B

我做了什么：
1. 修改A程序的程序逻辑，使得考虑特殊情况B；
2. 为以上的程序逻辑添加了一个测试案例；
3. 将特殊情况B，整理成案例，加入文档C。

我是如何做到的：
1. 在文件D中，判断E逻辑的时候，考虑特殊情况B；

如何验证这功能：
1. 在运行该项目的时候，输入内容F，可以得到正确结果G，即可验证

```

### Code Review 规范

Code Review(代码审核)是在项目开发过程中，对源代码进行系统性检查的过程，可以帮助项目找到更多的缺陷，提高项目质量的同时，也很大程度提高开发者的自身水平。Code Review不仅仅是项目维护者的义务，同时也是每一个项目参与者最值得从事的事情之一。

本项目的Code Review主要基于Github上PR提交中的代码。本项目的 Code Review 并不代表着参与者PR能力的高低，而是带着评审的目标提高项目质量，每一个Reviewer都应该带着学习和提高的态度来参加Code Review。

Code Review 中势必会发现贡献者PR中存在的缺陷，或者令人疑惑的代码部分，Reviewer有权利提出自己的建议，包含以下几方面：

* 代码存在缺陷的地方，提出Reviewer认为存在缺陷的理由。
* 比如`建议删除以上三行代码代码，原因：此功能已经废除，无效代码有可能提高维护难度`是可读性较强的Code Review 评论；
* 比如：`这段代码有问题`是一个有待改善的Code Review 评论，因为没有提供合适的理由，有损协作效率；
* 对于理解较难的部分，Reviewer有建议作者提出增加注释的权利，便于所有参与者理解项目。

### Merge 规范

项目维护者在代码审核（code review）时，在PR的评论栏中使用 LGTM(Look Good To Me)代表同意此PR的合并，使用NotLGTM(Not Look Good To Me)代表反对此PR的合并。

一个变更在合并进入此项目之前，必须得到一位以上维护者的LGTM。另外，只要有一位维护者使用 NotLGTM，则该维护者必须提供反对的理由。除非，维护者收回 NotLGTM，否则原则上PR将不被合并进入此项目。

### 代码格式

起码的代码格式是规范项目协作的必要手段。本项目针对特定语言，希望每位贡献者遵守相应规范，比如Go语言项目，我们建议使用gofmt完成代码格式化。

本项目非常欢迎您的 Hacking ！