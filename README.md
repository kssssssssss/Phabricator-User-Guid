#Phabricator基本概述
>Phabricator是一套基于Web的软件开发协作工具，包括代码审查工具Differential，资源库浏览器Diffusion，变更监测工具Herald，Bug跟踪工具Maniphest和维基工具Phriction。Phabricator可与Git、Mercurial、Subversion集成使用。
Phabricator是开源软件，可在Apache许可证第2版下作为自由软件分发。
Phabricator最初是Facebook的一个内部工具，主要开发者为Evan Priestley。Evan Priestley离开Facebook后，在名为Phacility的新公司继续Phabricator的开发。

#CodeReview基本概述
#### 为什么需要执行代码评审
- 代码评审的最大好处是纯社会性的，当你知道你的每一行代码都有另外一个人看，自然而然会更加卖力的表现，拿出最好的状态编码，因为每个人都有虚荣心嘛；
- 代码评审可以及时发现一些容易发现的BUG，而不必将发现BUG的时间点推迟到测试阶段；
- 代码评审可以保证至少有两个人都理解任何一份代码。当出现员工休假，离职等情况的时候，至少保证团队的代码不会陷入无人理解或者无人处理的状况。

####代码评审流程
代码评审的流程有如下两种方式:
-  **提交前评审**(_pre-push code review_)(**Review**)
-  **提交后评审**(_post-push code review_)(**Audit**)
详细







