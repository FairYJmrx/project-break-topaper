# 逐篇文献抽取字段

这是一套尽量统一的抽取字段。目标不是机械填表，而是方便后续比较、归纳和追踪研究脉络。

## 通用字段

- 标题
- 作者
- 年份
- 发表 venue / 期刊 / 会议
- 研究问题
- 研究对象或任务
- 数据集 / 语料 / 实验对象
- 方法
- 基线 / 对照
- 评价指标
- 主要结果
- 作者声称的贡献
- 局限性
- 与当前主题的相关性
- 时间位置 / 发展阶段

## 方法类论文追加字段

当论文核心是方法、模型、流程、系统或分析管线时，再补充以下字段：

- 原始数据类型
- 模型实际输入数据
- raw data 到模型输入的转换步骤
- 方法类型
- 任务定义
- 标签或真值来源
- 评价方式与关键指标
- 最终输出
- 可解释性
- 适用边界
- 相对前一代方法的改进点
- 相对前一代方法保留的限制
- 在时间演化中的位置

## 写法规范

- 优先记录论文明确写出的信息
- 任何不确定内容都标注“文中未明确报告”
- 不要猜测作者没有说的细节
- 不要把推断写成事实
- 如果用户只关心部分字段，也尽量保持字段顺序不变
- 多篇论文比较时，尽量让所有卡片使用同一套字段

## mNGS / taxonomic classification 额外字段

如果主题是宏基因组、物种鉴定、read classification、taxonomic classification 或相关深度学习任务，建议额外关注：

- 任务层级：species / genus / family / phylum / kingdom
- 输入表示：vectorized k-mer / sequence token / raw sequence
- k 值
- canonical k-mer 是否使用
- 模型结构：CNN / RNN / LSTM / BiLSTM / Attention / Transformer / BERT-like / MLP
- 数据类型：真实 reads / simulated reads / contigs / 16S / shotgun
- 是否 hierarchical classification
- 是否讨论 calibration / confidence / confidence threshold / ECE
- 主要 baseline
- 与 baseline 的差异
- 数据是否过于理想化
- 是否存在预处理泄漏或评估口径不公平

## 适合直接写进卡片里的简评

建议每篇卡片最后补一行简评：

- 对我们当前工作的启发
- 是否支持当前方法选择
- 是否提示我们需要换数据、换表示或换模型
- 是否值得重点精读
