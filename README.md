# 华南理工大学硕/博士学位论文LaTeX模板

本模板由 

https://github.com/alwintsui/scutthesis 

以及 

https://github.com/yecfly/scut-thesis 

的模板修改而来，可用于撰写华南理工大学硕/博士学位论文。本项目是本人在撰写毕业论文时开启的，始于2020年的非官方模板，实测可以通过所有格式审核。

“祖传代码”是前辈们的心血，在此向他们致以崇高的敬意！本模板在修改“祖传代码”过程中仅对修改部分进行更新，其余部分仍保留源代码。类似地，编译时如果提示缺乏字体，请按照attachment里面的字体（右键安装即可）

另外参考文献管理软件推荐使用开源的zotero，这是生成本模板的bib文件的软件（最新实测其他文献管理软件如endnote也可以使用本模板，重点是导出bib文件）。当然，也可以手动新建一个后缀名为.bib的文件，然后直接在文献页面（或谷歌、百度学术页面）复制BibTeX数据到该.bib文件，最后在scutthesis.tex文件里使用就行。zotero不仅有强大的PC端（支持mac、win、linux），可以使用chrome等浏览器搜索到论文后利用插件一键捕获文献信息到zotero。然后对zotero收集好的文献，选中想要引用的论文然后按快捷键复制（需要适当自定义设置），再到撰写论文的tex文件粘贴即可（word也可以使用zotero，也很方便，本项目我们仅仅讨论latex模板）。zotero还有移动端（安卓、ios），所有文献信息都是同步的，文献的pdf文件可以使用第三方存储工具同步。总之多端同步，开源免费，方便随时随地看论文，省去管理文献的麻烦，相见恨晚！在写毕业论文的各位可以推荐给研一的师弟师妹，早用早享受，方便后期写论文。

在这里多提一下，国外的文献管理软件对知网等平台搜出来的中文论文的支持都不是很稳定，有时候很好，有时候某些版本又抽风，有时候因为知网等平台的更新也会有影响，所以建议大家论文的引用最好找sci高水平论文去引，尽量引用近几年的本领域top期刊、会议文章。这样整篇文章绝大部分都是引用英文文章（国产top期刊、会议也大都是英文，现在国产期刊也很强，像我熟悉的航空学报英文版现在也是top期刊），巧妙避开这个问题。同时这会在盲审时增加得分。我见过一个同学大面积引用“XX学院学报”，“XX职业技术大学\学院毕业论文”的文章，盲审没过，按照我的上诉建议修改后就顺利通过了。大家仔细想想，你引用的文章是这么一个水平，那说明你的工作就是基于这么一个水平，你说你的文章能是什么水平？盲审肯定吃亏。文献引用本身就是想表达这样一件事：我论文里说的这个事，某某文章提到过\做过。高水平期刊的文章原创性肯定比低水平期刊的文章要强，所以同样的事可以通过找到高水平期刊的论文来表达。如果想引用某某top大学的学位论文，那同样的事可以通过找到该作者发表的期刊、会议文章来完成，一般毕业论文是作者本人发表的所有文章的集合，高水平的学位论文其作者发表的小论文也一定是高水平的期刊、会议论文，所以一定能找到。文献调研很重要！所以建议即使没有做出惊天地泣鬼神的工作，引用的时候也是尽量引用像nature、science这样的顶级期刊的近几年的文章，起码给人感觉你的工作是站着巨人的肩膀上的，应该不会是很差的工作，听懂掌声！（手动狗头）

本模板最主要的改动是参考文献使用biblatex（biber），而不是原来的BibTeX，因此不再需要.bst文件。在这项改动之后，参考文献部分的格式符合国标，当然要注意进行适当的设置，因为学校的论文撰写规范里有的信息不需要显示。

本模板不再利用Lyx，直接使用TeXstudio进行编辑，这类似IDE。

使用之前可有选择性地阅读《一份（不太）简短的LATEX 2ε 介绍》，地址：https://github.com/CTeX-org/lshort-zh-cn.git ，以及阅读本模板的使用说明scutthesis.pdf文件。使用案例为本人的勘误后的学位论文（原文有部分笔误）：https://github.com/mengchaoheng/SCUTthesis-mengchaoheng.git

快速使用：

有两种方法：

1.使用编译脚本all.bat，记得关掉生成的pdf文档再双击all.bat。（双击clean.bat删除临时文件）

2.使用TeXstudio，首次编译建议从主文件scutthesis.tex开始编译，首先在TeXstudio的Options->Configure TeXstudio->build中，编译器(Dufault Compiler)选择XeLaTeX，默认文献工具(Default Bibliography Tool)选Biber，构建并查看（build & view） 按照scutthesis.pdf中的图2-1进行设置（点击右侧扳手符号进行设置，分别选择recompile-bibliography、Defualt compiler、Defualt Viewer并点add到右侧栏中），也可以使用默认的Compile & View（只不过此时不会自动更新参考文献著录）。本文模板编译后生成的scutthesis.pdf即为模板使用说明，首次使用最好直接阅读该说明并结合《一份（不太）简短的LATEX 2ε 介绍》学习。

错误排除：

目前遇到的导致错误的原因大都是以下三种：

1.语法错误，这种自己很容易解决，特别是工科生，按照latex的规范去写就好。

2.和参考文献有关的错误，记住一定检查好bib文件，而bib文件来源于参考文献管理软件如本文推荐的zotero，又或者来源于自己手动建立的文件。一定要设置好导出选项以及格式，同时TeXstudio要设置好编译选项。

3.编译器问题，和第二条一样，一定要在TeXstudio的Options->Configure TeXstudio->build中设置好。

确保以上三方面没问题的话，基本就可以愉快的写论文了。

另外使用zotero，科学上网很重要，通常我们使用谷歌学术搜索文献并利用chrome的zotero插件直接捕获文献著录信息。但我使用各种方法均遇到过被谷歌学术封锁的情况，后来只能换科学上网方法，这方面可以百度v2ray自行学习，找个不能随意换ip的服务器商（这种ip比较纯净，没被谷歌封过。随意换ip的商家，通常ip已经被玩烂了）。强烈建议不要在谷歌学术搜索界面用zotero插件一键捕获大量文章，一次只捕获一两篇最佳。进入文章页面（如IEEE页）一篇一篇地捕获也可以。利用谷歌学术从搜索结果大量捕获文献信息容易被谷歌封ip，一旦被封只能换ip，相当麻烦！
