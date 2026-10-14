# 贡献指南 (Contributing Guide)

感谢您关注《产品经理全书：从零到一构建现代产品管理实战知识体系》开源项目！

本指南旨在规范内容贡献、案例分享、勘误提交与代码协作流程。

---

## 💡 贡献原则

1. **真实产业视界**：倡导源自真实产业实践、有实际业务上下文支撑的方法论与复盘，拒绝空洞的教条主义。
2. **结构化与模块化**：遵循全书既有的结构化规范，包含思维导图（Mermaid）、对比表格、告警提示块（GitHub Alerts）与章末自测清单（Checklist）。
3. **保护商业隐私**：在分享自身实战案例时，严禁泄露任何涉及特定企业的保密商业数据、密钥密码或未公开商业机密，必须进行脱敏或抽象化处理。

---

## 🛠️ 如何参与贡献

### 1. 提交 Issue（问题与建议）
- **勘误修复**：如发现错别字、失效链接或公式排版问题，请直接提交 Issue 并标注对应文件路径与行号。
- **内容扩充建议**：若您认为某个章节缺少关键业务场景（如出海合规、AI Native 产品体验设计等），欢迎在 Issue 中发起讨论。

### 2. 提交 Pull Request（PR）
1. **Fork** 本代码仓库至您的个人 GitHub 账户；
2. **Clone** 到本地环境并新建特性分支：
   ```bash
   git checkout -b feature/enrich-partX-topic
   ```
3. **编辑内容**：
   - 保持 UTF-8 编码；
   - 遵循 Markdown 规范与全角/半角标点符号排版规范；
   - 如需引入配图，请将图片放置于 `docs/assets/images/` 目录下，并使用语义化英文命名。
4. **提交 Commit**：
   - 建议遵循 Conventional Commits 规范，例如：
     - `docs: fix typo in chapter 15 prioritization`
     - `feat: add AI Native PRD template in part 5`
5. **发起 PR**：推送至您的远程分支，并在 GitHub 上向主分支提交 Pull Request，详述修改动机与内容摘要。

---

## 📜 许可证协议

通过向本项目提交贡献，您同意将您所贡献的内容基于 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 协议进行公开授权。
