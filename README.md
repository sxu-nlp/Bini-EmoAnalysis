### CCAC 2025技术评测赛道五：细粒度比拟句情绪分析

#### 任务背景：

比拟是中文常见的修辞手法，可分为比喻、拟人和拟物三种类型。比拟通过将本体（描述对象）与喻体（比拟对象）建立相似性联系（喻底），以生动形象的方式传递情感和语义。为了增强文本情绪表达效果，比拟句常出现在文学文本、社交媒体等场景中，对机器深层挖掘文本语义及情绪信息提出了挑战。因此，本任务细粒度分析比拟句涉及本体、喻体、喻底（本体和喻体间的相似依据）的多层关联，准确建模情绪，旨在深化比拟修辞格与情绪表达关联的认知，推动计算语言学与认知科学的交叉研究，从而为文学分析、舆情分析及人机交互提供支撑。

#### 任务介绍:

本届中文比拟情绪分析评测包含2个阶段，共计3个任务。第一阶段要求（1）从对比拟句所蕴含的情绪类别进行判断，（2）从中抽取细粒度本体及喻体要素。第二阶段根据给定的本体和喻体，结合比拟句子信息判断喻底。3个任务采用统一的数据集，由于1条比拟句可能出现多个“本体-喻体-喻底”对，则每1条数据会提供若干个<本体、喻体、喻底、情绪>四元组标签。以下为各任务的具体介绍：

**第一阶段**

- 任务1：比拟句情绪分析

   - 目标：给定一个比拟句，判别该句子的情绪类别。

   - 输出：8类情绪标签，0-7分别代表无情绪、乐、好、怒、哀、惧、恶、惊。

   - 评价指标：Macro-F1


- 任务2：细粒度本体、喻体特征抽取

   - 目标：抽取句子中所有本体（描述对象）及喻体（比拟对象）片段对。

    - 输出：假设一句比拟句中包含n组<本体-喻体>对，输出<本体1，喻体1>，......<本体n，喻体n>。

   - 评价指标：F1
   
   - 实体抽取采用模糊匹配：对于模型抽取的实体e，人工标注的答案实体a，覆盖度定义为：$s(e,a)=\frac{|e\cap a|}{|e\cup a|}$，若$s(e,a)\ge0.6$，则视为实体抽取正确。对于一组<本体-喻体>对，需本体、喻体实体同时满足正确条件时，视为<本体-喻体>对抽取正确。

**第二阶段**

- 任务3：<本体-喻体>对喻底判别

   - 目标：给定比拟句信息和一组<本体-喻体>对，以单选题形式进行比拟喻底的判别。

   - 问题：片段对〈本体ₖ, 喻体ₖ〉喻底是什么？

   - 选项：A 选项1 B 选项2 C选项3 D 选项4

   - 输出：正确选项标签。

   - 评价指标：ACC。

**最终排名依据**：三个任务的指标均值。

#### 数据集介绍:

待更新

#### 评测时间安排：
|                            |                    |
| -------------------------- | ------------------ |
| 事项                       | 时间               |
| 任务发布与报名启动         | 2025年4月1日       |
| 第一阶段训练集语料发布     | 2025年5月1日       |
| 第一阶段测试集语料发布     | 2025年5月20日      |
| 第一阶段提交截止           | 2025年5月30日      |
| 第二阶段训练集语料发布     | 2025年6月1日      |
| 第二阶段测试集语料发布 | 2025年6月15日 |
| 第二阶段提交截止         | 2025年6月20日     |
| 比赛结果公布               | 2025年6月下旬      |
|CCAC2025大会召开及颁奖典礼 | 2025年7月18日-20日|

#### 组织者和联系人

评测主席：廖健，陈鑫

评测组织：山西大学，太原科技大学

评测委员会成员：李鹏帅，张佳雯

如有疑问，请致信评测会务组：廖健（[liaoj@sxu.edu.cn](https://docs.qq.com/doc/liang@dlut.edu.cn)）, 陈鑫（[chenxin@tyust.edu.cn](https://docs.qq.com/doc/chenxin@tyust.edu.cn)）, 李鹏帅([3023109202@qq.com](https://docs.qq.com/doc/3023109202@qq.com))

#### 评测报名方式

![]([https://oss-liuchengtu.hudunsoft.com/userimg/b3/b38c98c74a8337ac35feb8291b6e0d0d.png](https://github.com/sxu-nlp/Bini-EmoAnalysis/blob/main/CCAC2025%20%E7%BB%86%E7%B2%92%E5%BA%A6%E6%AF%94%E6%8B%9F%E5%8F%A5%E6%83%85%E7%BB%AA%E5%88%86%E6%9E%90%E6%8A%A5%E5%90%8D%E8%A1%A8%E4%BA%8C%E7%BB%B4%E7%A0%81.png))

【腾讯文档】CCAC2025 细粒度比拟句情绪分析报名表

https://docs.qq.com/form/page/DWXd2TFZMVkV2RHJD
