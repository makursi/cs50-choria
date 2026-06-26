# 011 — Week 9: Flask — Finance

## Parent

[PRD: CS50x 2026 个人学习日志仓库](../prd.md)

## What to build

完成 Week 9（Flask）后半部分的核心问题集：C$50 Finance 股票交易模拟应用。这是一个完整的 Flask Web 应用，功能包括：

- 用户注册与登录（session 管理）
- 实时股票行情查询（调用 IEX Cloud API 或替代 API）
- 模拟买入/卖出股票
- 交易历史记录
- 资产组合概览与现金余额管理

在 `week-9-flask/finance/` 下创建完整的 Flask 应用。

该周笔记补充：Session 管理、API 调用、密码哈希、事务处理。

## Acceptance criteria

- [ ] `week-9-flask/finance/` 包含完整 Flask 应用，含 `app.py`、模板、静态文件、`helpers.py`
- [ ] 用户可注册、登录、登出
- [ ] 可按股票代码查询实时价格
- [ ] 可买入/卖出股票，余额正确扣减/增加
- [ ] 显示交易历史和持仓概览
- [ ] `notes.md` 补充 Finance 相关知识点（session、API、密码哈希）
- [ ] 每道子功能独立 commit，commit message 英文
- [ ] 代码注释使用英文

## Blocked by

- [#000 — Repo 脚手架](./000-repo-scaffold.md)
- [#010 — Week 9 Flask: Birthdays](./010-week-9-flask-birthdays.md)（建议先做完 Birthdays 再攻 Finance）
