#Phabricator基本概述
>Phabricator是一套基于Web的软件开发协作工具，包括代码审查工具Differential，资源库浏览器Diffusion，变更监测工具Herald，Bug跟踪工具Maniphest和维基工具Phriction。Phabricator可与Git、Mercurial、Subversion集成使用。
Phabricator是开源软件，可在Apache许可证第2版下作为自由软件分发。
Phabricator最初是Facebook的一个内部工具，,其被认为facebook成功的11个重要因素或者工具之一，facebook的工程师对这个工具赞誉有加。其主要开发者为Evan Priestley，Evan Priestley离开Facebook后，在名为Phacility的新公司继续Phabricator的开发。

#CodeReview基本概述
#### 为什么需要执行代码评审
- 代码评审的最大好处是纯社会性的，当你知道你的每一行代码都有另外一个人看，自然而然会更加卖力的表现，拿出最好的状态编码，因为每个人都有虚荣心嘛；
- 代码评审可以及时发现一些容易发现的BUG，而不必将发现BUG的时间点推迟到测试阶段；
- 代码评审可以保证至少有两个人都理解任何一份代码。当出现员工休假，离职等情况的时候，至少保证团队的代码不会陷入无人理解或者无人处理的状况。

####代码评审流程
代码评审的流程有如下两种方式:
-  **提交前评审**(_pre-push code review_)(**Review**)
-  **提交后评审**(_post-push code review_)(**Audit**)

详细流程如下：
Review流程：

1. 程序员在试图提交代码变更到代码库之前，先提交变更申请，变更申请包含了这次变更的内容，评审人；
2. 评审人查看变更内容，评估变更，与变更申请人沟通，评估是否通过变更；
3. 如果评审人通过变更，则变更申请人才可以提交代码到代码库；
4. 如果评审人不通过变更，则变更申请人需要根据讨论结果或评审建议做出修改，直到与评审人达成一致，通过评审，才可以提交代码到代码库；
![Pre-push流程](/assets/Pre-Push.png)

Audit流程
Audit流程对以前的开发流程无任何影响，提交者可以在提交时@Auditors 进行代码检查，系统会通知Auditors对代码评价。


#### pre-push code review vs post-push codereview

1. 普遍认为相比pre-push code review，post-push code review几乎没有任何好处！
2. 但是post-push code review 更加容易实施，过程对现有的组织架构和流程没有完全的颠覆，对团队成员的要求没有那么高；
3. 相比pre-push code review，post-push code review不需要对修改代码&提交变更这个过程中断，不需要等待评审的时间；
4. post-push codereview可以作为组织向pre-push code review过程实施的过渡训练；

#### 代码审核实践

Google工程师的重要建议：
（此处参考：http://www.aqee.net/things-everyone-should-do-code-review/）
最重要的一个原则：代码审查用意是在代码提交前找到其中的问题——你要发现是它的正确。在代码审查中最常犯的错误——几乎每个新手都会犯的错误——是，审查者根据自己的编程习惯来评判别人的代码。
 
对于一个问题，通常我们能找出十几种方法去解决。对于一种解决方案，我们能有百万种编码方案来实现它。作为一个审查者，你的任务不是来确保被审查的代码都采用的是你的编码风格——因为它不可能跟你写的一样。作为一段代码的审查者的任务是确保由作者自己写出的代码是正确的。一旦这个原则被打破，你最终将会倍感折磨，深受挫折——这可不是我们想要的结果。

另外在IBM developerworks 上有一篇介绍代码评审的最佳实践的文章写得相当好，参考：http://www.ibm.com/developerworks/rational/library/11-proven-practices-for-peer-review/




