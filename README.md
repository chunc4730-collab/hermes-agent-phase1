# hermes-agent Phase 1 补丁集

> 简体中文 | English below

为 Hermes Agent 提供 5 个核心可靠性模块。

## 是什么

coding-agent 插件配上这些补丁后，长任务更稳。

## 安装

```bash
git clone https://github.com/chunc4730-collab/hermes-agent-phase1.git
cd ~/hermes-agent
git am path/to/hermes-agent-phase1/patches/*.patch
```

## 4 层补丁

| 补丁 | 改动 | 模块 |
|---|---|---|
| L1 | agent/conversation_loop.py + new files | Token Budget, State Machine |
| L2 | agent/conversation_loop.py (重大) | Plan Continue, Auto Resume, Fork Isolation |
| L3 | agent/context_compressor.py +4 files | Microcompact, Fallback |
| L4 | agent/run_agent.py | 集成接线 |

## 适用版本

已验证可干净 apply 到最新 Hermes 主线 (2026-06)。

不需要完整 Hermes 源码 — 只是 4 个 git patch + README。

## 效果

配合 coding-agent 插件使用：长调试链 95% 跑完 vs 80-85% 裸跑。

## 作者

chunc4730-collab | Hermes coding-agent 插件作者

## English

4 clean git patches for Hermes Agent core. Apply with `git am patches/*.patch`.
Verified on latest upstream. Enables Token Budget, Microcompact, Fallback,
State Machine, Fork Isolation — 5 reliability modules for long coding sessions.
