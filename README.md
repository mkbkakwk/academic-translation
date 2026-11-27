# 安装与测试

本包为 DSH Skill，不是渲染插件。保留 v4 原始模板和术语，核心规则压缩，细则按需查阅。每块仍由模型复制 HTML/CSS 给工具；真正消除重复生成需要专用渲染器，尚未实现。

1. PowerShell 执行 `dsh plugin --profile web add dsh-html-live-preview`（已安装可跳过）。
2. 将整个 academic-translation 文件夹放在 `$env:USERPROFILE\.dsh\skills\`，若设置了 DSH_HOME 则放在 `$env:DSH_HOME\skills\`。不要多套一层目录。
3. 启动/重启 DSH Web，开启新会话。在技能选择器中选 academic-translation，或输入 `/academic-translation`（若客户端支持斜杠技能）。也可明确要求加载 academic-translation Skill。
4. 测试题名：`Uncertainty-Aware Retinal Vessel Segmentation via Ensemble Distillation`。应出现中文译文、两个意群、两级框与双语重点高亮。
5. 测试公式：`The attention weights are computed as $A=\operatorname{softmax}(QK^T/\sqrt{d_k})$, where $Q,K\in\mathbb{R}^{n\times d_k}$.` 应出现真实公式；另试 `\boldsymbol{x}`。若失败，检查插件错误条、CDN、CSP 和 MathJax 扩展加载。

渲染插件 README：https://github.com/Weihong-Liu/dsh-html-live-preview
DSH Skills 官方文档：https://deepseek-harness.github.io/deepseek-harness/reference/subsystems/skills

未在你的本地 DSH 运行；主题变量采用兼容兜底，可能需要针对宿主主题修改。工具结果会随会话保存，不代表没有持久化。插件预览默认有高度上限，可手动展开。不要同时保留 v4 全局提示词与本 Skill，以免规则重复。
