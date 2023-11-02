# r15 - 体育博彩赔率教学程序

## 项目简介

"r15" 是一个用于教育用户体育博彩盘口赔率的运作过程的教学程序。

这个基于Python的项目旨在帮助用户更好地理解博彩赔率、计算和相关术语。

程序取名 "15 rounds" ，是关于 A队伍 与 B队伍 进行 15回合 比赛的游戏。

## 游戏规则

每个回合会随机生成一个平均分布在 0 到 1 之间的6位小数 "r" ，用来决定这个回合的输赢情况。

每一回合结果都有可能影响到 "state" 的值，从而决定下一回合的输赢概率。

"state" 在第一回合时是 "None" ，而在后续所有 14 个回合中都有 "A" 或者 "B" 的赋值。

"赢下回合"、"赢得回合"、"赢下分数"与"赢得分数"是相同的意思。

"A"与"A队伍"是相同的意思，同样，"B"与"B队伍"是相同的意思。

没有回合会以平局或者双赢告终。

## 游戏概率

对于第一回合而言:

A队伍拥有 51% 的胜率。

对于其他回合而言:

A队伍 赢得上一分后，拥有 81% 的胜率赢下这一分。

B队伍 赢得上一分后，拥有 67% 的胜率赢下这一分。

## 程序运算

当 "state" 为 None 并且 "r" 小于 0.510 000 时，A 赢得第一回合， "state" 变量赋值为 "A"。

当 "state" 为 None 并且 "r" 不小于 0.510 000 时，B 赢得第一回合， "state" 变量赋值为 "B"。

当 "state" 为 A 并且 "r" 小于 0.810 000时，A 赢得该回合 ，"state" 变量仍然为 "A"。

当 "state" 为 A 并且 "r" 不小于 0.810 000时，B 赢得该回合 ，"state" 变量赋值为 "B"。

当 "state" 为 B 并且 "r" 小于 0.670 000时，B 赢得该回合 ，"state" 变量仍然为 "B"。

当 "state" 为 B 并且 "r" 不小于 0.670 000时，A 赢得该回合 ，"state" 变量赋值为 "A"。

## 术语解释

- **ftn:** "ftn" 即 "first to n" ，指的是在比赛中率先达到某个特定分数。例如，"ft3" 指的是在比赛中率先达到3分。
- **rn:** "rn" 即 "round n" ，指的是在比赛中赢得特定的第若干回合。例如，"r3" 指的是在比赛中赢得第3分。

## 使用方法

1. **安装 Python:** 确保你已经安装了Python。如果没有，你可以从 [Python 官方网站](https://www.python.org/) 下载和安装。

2. **克隆项目:** 使用以下命令克隆项目到本地计算机：

   ```bash
   git clone https://github.com/33333bb/r15.git
