# 注意：项目进行中，暂不可用
### 前言
业务场景中存在一类任务，既需要提前规划，但是又存在任务目标与数量本身有不确定性，而且完成任务的过程也不能精确操制的情况。 比如：
- 爬虫任务的调度器，爬取目标会根据爬取对象内容变化而动态变化的，爬取过程也会受到网络、代理、内容大小等因素影响，无法精确控制进度，但是又需要根据更新优先级、限流策略和Worker数量尽量完成所有任务。
- 广告投放的调度器，广告投放目标有一定的计划性，但是也存在及时的任务增减，而且流量的变化也只能根据一些数据来预估，同样要考虑投放的频次及流量的分布。
这些场景都需要一个任务动态规划调度器，既能接收一些预设参数，也能接收实时的变化参数，进而动态的规划最佳的调度策略。
