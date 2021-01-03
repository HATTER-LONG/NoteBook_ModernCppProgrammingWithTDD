# 《C++程序设计实践与技巧：测试驱动开发》

## TDD 的践行步骤

1. 编译一个最基本单元功能的测试代码。
2. 测试失败。
3. 实现功能代码**最低限度**使得测试代码通过。
4. 测试成功。
5. goto ⬆ 第一步。
6. TDD 的各个周期都会使用重构来审阅设计，不仅仅是功能代码同样包含测试用例。

## TDD 的前进规则

- 在 TDD 周期中的每一步，你必须能回答以下问题：
  1. 确定测试目标：
      - 怎样才算可以增量开发的最小行为？
      - 系统中已经存在这样的行为了么？
      - 怎样让测试名称准确表达行为？
      - 测试中使用的接口是客户端代码使用这一行为最好的方式吗？
      - 以上问题可以参考[成功运用 TDD 的方法](03_测试驱动开发基础/README.md#成功运用-tdd-的方法)
  2. 确保新的测试是失败的：
      - 如果没有失败，为什么？
      - 这个行为已经在系统中存在了么？
      - 是否是忘记了编译差异代码？
      - 是不是在上一个测试中步伐太大了，包含了多个行为？
      - 断言是否有效？
  3. 写出你认为可以让测试通过的代码：
      - 代码是不是刚好满足测试说明的行为要求？
      - 你清楚刚才写的代码中哪些地方需要整理么？
      - 是否遵循了团队标准？
  4. 确保所有测试都能通过：
      - 如果没有，你的编码是否正确？
      - 你的规范正确么？
  5. 整理刚才的代码改动：
      - 怎么做才能使你的代码符合团队标准？
      - 新的代码和系统中其他要清除的代码有重复么？
      - 代码有没有坏味？
      - 遵循好的设计原则了吗？
      - 除了当下要做的设计和代码整理工作，你还知道其他什么？
      - 设计是朝好的方向发展吗？
      - 你的代码改动会导致需要修改其他地方的代码吗？
  6. 确保所有测试再次通过：
      - 确信你的单元测试覆盖率够高吗？
      - 是不是应该运行一些速度较慢的测试集合，以便有信息继续前行？
      - 下一个测试是什么？
