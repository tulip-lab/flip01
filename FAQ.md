# FLIP(00) FAQ

Hi everyone, this is a FAQ document about FLIP (01).
This is also a document that encourages everyone to update questions and provide good answers.


FLIP(01)的考核重点是NLP自然语言处理等常用方法的熟练掌握和运用，同时也会在00组的基础上强化考察 *LaTex* 和 *Git* 的使用。以下总结了一些组内成员在学习01组的过程中比较常见的问题，希望为大家的学习提供参考，同时我们也鼓励大家在 *FAQs* 上及时更新自己所遇到的问题或者为他人提出的问题提供解决方案，争取做到互帮互助，共同进步~当然，大家的更新操作需要采用提交 *issues* 或 *pull request* 的形式，这也是所有flip组的基本考核内容。



**1.** *GitFlow*  和 *LaTexDiff* 的操作流程

01组要求对这些操作流程完全熟练掌握，做到运用自如。

提供参考[blog 1](https://blog.tulip.org.au/2018/07/31/Tools-LaTeX/ )和[2](https://coco.tulip.org.au/post/git-latexdiff/)。

**2.** 为什么直接用 *TexStudio* 编译，*GitInfo* 是有效的。但使用 *Git LatexDiff* 生成的差异文档，*GitInfo* 不生效？

这是flip00组遗留下来的问题，希望在01组里每位同学都要重点注意这个问题。

解决方法 by [blog of Jiahui Zhou](http://blog.sanhuax2.xyz/ )。（本次考核会重点检查大家的 *LaTeXdiff* 操作）

**3**. 做NLP时，有些nltk语料库比较难找，比较耗时影响进度。

大家做的nlp题目都不同，可能会使用到各种不同的语料库，建议大家互相分享一下，以下是江文彬同学分享的她自己学习过程中找到的一些[语料库](https://pan.baidu.com/s/1-WiGMIM6mLWcikNOhpR0Qg  )，提取码为 *tvo3*

欢迎大家后续继续分享自己找到的语料库。

**4.** 为什么 *gensim* 这个库一直加不上，用国内源也不行？

需要注意版本问题，同时尽量用 *tar.gz* 安装，提供以下参考：[参考1](https://blog.csdn.net/weixin_40988315/article/details/79610094)和[参考2](https://blog.csdn.net/sinat_29957455/article/details/76735301?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task )

**5.** 使用word2vec进行词向量转化，放到机器学习模型里边跑，准确率依然不好，是处理的时候存在什么问题吗？

nlp想提升准确率，主要在于文本清洗和模型的选用，可以做进一步更完整的清洗工作，或者尝试word2vec+lstm等较新兴的模型组合。（answered by 徐荣欣）

尝试更换nbc。(answered by 周佳绘)