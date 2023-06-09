[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/00vPqKTJ)
# 软件工程实训任务二：小组协同开发
1. **实验目的**
- ** 巩固强化软件编程规范
- 提高面向对象软件建模与抽象能力
- 培养小组协同开发能力
- 掌握基于Maven的软件项目管理机制
- 掌握基于Github的小组协同开发工具和平台
- 了解DevOps软件开发流程
1. **实验内容**
- ** 创建软件开发小组
- 针对样例代码工程进行小组讨论，确定功能扩充需求点
- 基于Github中的issue管理功能明确工作任务并为组员分配工作任务
- 基于小组商定的分支模型进行软件功能开发，并按开发流程进行代码测试、提交、归并和同步
- 代码提交到远程仓库后，应进行自动化代码格式规范检查和测试以确保功能符合需求设计
- 完成前述各项任务后，可尝试进行代码自动化打包，自动生成可供执行的jar文件

1. **实训要求**
1. **   创建软件开发小组
   1. 每个开发小组人数3-5人，推选一人作为组长，负责组织、协调和领导团队开发；
   1. 所有小组成员应按操作步骤在github开发平台上加入同一小组，共用同一代码仓库；
1. 开展小组讨论，确定功能扩充点
   1. 样例工程“Ludo”具备最基本的程序功能，该项目具有极大的扩展空间，开发小组内可进行沟通讨论，确定系统结构优化需求或功能扩充需求，结构优化或功能扩充项不能少于5项；
3. `   `基于Github中的issue管理功能明确工作任务并为组员分配工作任务
   1. 将工作任务拆分细化后，明确版本开发计划和里程碑时间节点；
   1. 在github平台创建任务issue并为所有组员分配任务；
   1. 每位组员可以分别承担不同的开发任务，也可以按照小组角色分别承担开发、测试、集成等工作任务；
   1. 工作任务的划分是最终衡量小组成员工作量的重要依据；
3. 基于小组商定的分支模型进行软件功能开发，并按开发流程进行代码测试、提交、归并和同步
   1. 小组成员按照小组商定的分支模型在各自的工作分支进行进行开发任务；
   1. 工作分支在合并前应同步到远程仓库供教师检查每人的开发工作完成情况；
   1. 提交代码时应按照小组约定的规范格式填写代码提交说明，代码提交说明也将作为评分的重要依据；
3. 代码提交到远程仓库后，应进行自动化代码格式规范检查和测试以确保功能符合需求设计；
   1. 可以利用github平台的actions功能在代码提交时自动触发代码格式检查，对于不符合规范的代码系统将给出提交失败提示；
   1. 可以利用github平台的actions功能在代码提交时自动触发测试用例检查，对于不能通过测试检查的代码系统将给出提交失败提示；
3. 可尝试进行代码自动化打包，自动生成可供执行的jar文件
   1. 结合github平台的actions功能和maven编译脚本，在代码通过规范性检查和测试用例后，进行自动化打包，生成可供直接执行的jar文件用于系统发布

1. **任务分析**

` `The main purpose of this task is to consolidate and strengthen our software programming specifications; Improve the modeling and abstraction ability of object-oriented software; Because the function of the sample engineering code is less and imperfect, we use GitHub as a team to develop tools and platforms, complete the code development, expand the game function, and cultivate our team collaborative development ability. We therefore decided to develop the game called Ludo


1. **开发版本计划与任务分派**
- **计划**

1\. Learn how to use Git tools and how to maintain personal code version based on git tools.

2\. fork sample project, clone code to local warehouse.

3\. Run the sample project in the local development environment to understand the code logic of the sample project.

4\. Read the code carefully and annotate each function.

5\. Clarify the code structure and describe the code structure and logic of the sample project with UML diagram.

6\. Expand code functions and optimize code logic.

7\. Install the Check Sytle-IDEA plug-in on the idea to standardize the code format.

8\. Write the experimental report in MarkDown format.

9\. push the task results to the remote code warehouse.

- **任务分派**

***DONOUVOSSI HILDANE FAFADJI :***

Code：Class player,subPlayer,ImageEngine,playerColor,Throw

Github: issue, feat branch

Doc：Experiment report

PPT,Class Diagram

***YASMIN FAUZIA :***

Code：Class User,GameDashboard,LoginForm,RegistrationForm,Opening

Github：Branch management

Doc:PPT,reportmd

***ALI MD SOBUJ :***

Code：Class GameScreen,GameWindows,Logic,Start

Github：publish branch,issue

Doc：Experiment report,Use Case Diagram

1. **程序设计与开发**
**
` `Ludo is simplification of the Indian game Pachisi. Invented at the end of the nineteenth century, Ludo has been a popular game from then till now. Though the player has some choice in what to do, luck dominates in deciding who wins and who loses, making it an excellent game to play against children.

Up to four players each have four pieces, which they race around the outside of a cross-shaped board according to the throws of a single six-sided die. Once a piece has completed a circuit, it turns towards the centre of the board where it finishes its journey. The first player to get all four pieces to the centre wins the game.

Use Case diagram

Available on the directory



Class diagram

Available on the directory

1. **开发分支模型与代码合并**

04 branches were created for this project: master , publish, develop and feat.

- Master: No other modifications are accepted except the merge from the publish branch.
- Develop branch: This branch is mainly used as an integration test branch, and all test environments deploy this branch for testing. 
- Feat branch: Used for function development. This branch is pulled and created from the develop branch every time, and then it is upgraded and merged into the develop branch after development.
- Publish branch: Used in pre-production environment and production environment release. For the final version, you can publish the Tag, automatically publish it through Actions configuration, package it and put it in the publish branch.

First, the team leader divides the develop and publish branches on the basis of the master branch. Then select the first function to branch out the feature branch on the basis of the develop branch.

The team develops locally, and after the self-test has no problem, it initiates a request to merge to the feature branch, and gives a commit, labeled feat(feature).

When a function is fully developed, a request is made to merge the contents of the feature branch into the develop branch.

Every time you push to the feature branch, you can check the format of the code and run the test through actions.

After all this the code is merged and pushed to the master branch

Some issues were also raised on GitHub 





1. **任务成果**

The user need to login first

Then he can access the game dashboard and choose the game he wants to play

Now he can start to play



1. **过程问题记录与分析**
1. There is not much problem in the process of annotating and labeling the code logic function, many functions like throw for rolling the dice were added correctly, which is not particularly difficult.
1. In the process of code structure analysis, how to draw UML diagrams we encountered problems, because some knowledge about UML class diagrams has not been firmly remembered, and the definitions of various relationships such as combination and aggregation are not clearly remembered. So we first reviewed the contents of the basic course of software engineering and looked back at PPT to arouse my memory. Then the code structure was carefully analyzed. We figured that we needed to first sit and choose what kind of model we want to use before starting to write any code.
1. We have used the Typora tool before, and we are familiar with the grammar of markdown mode, so the report is quite handy to write.
1. At the beginning of the task, our group discussed the division of labor first, and determined which functions to expand and how to hand over communication. After negotiating the code standards, they put themselves into their respective functional development. During the whole process, everyone helped each other and learned from each other's strengths, which was a great team development experience.

On the basis of the last task, we got a certain understanding of git, GitHub, their usage and principle, though we need to learn a bit more how to use GitHub to avoid some problems we had encountered this time but creating branches and merging branches wasn’t really difficult.












1. **实践总结**

In this practical course, we got in touch with a lot of software programming tools like git,github,xamp.. Learned how to use them to maintain personal code version, and understood its working principle and basic usage. Those are indispensable tools for us to develop large-scale software engineering projects in the future and plays a very important role in team collaborative development.

We also know the code annotation rules based on Javadoc standard, and have a certain understanding of it.

In the first task, we reviewed the knowledge of basic courses of software engineering, reviewed the drawing methods and standards of UML diagrams, and analyzed the code structure of sample projects, realizing the importance of code structure analysis in project development and deepening on our understanding of code structure.

Master the software project management mechanism based on GitHub.

In this task, we used the Java swing GUI designer to realize simple visual function management and consolidate our knowledge.

The most important thing is the collaborative development of the group. We have completed a small software project development based on GitHub platform, which shows the importance of communication, cooperation and complementarity.









