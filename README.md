# 毛泽东·先调查再下结论

先调查再下结论：有资料依据、有使用边界、可复核的中文 Agent Skill。

**把熟悉的思想，变成下一次任务可用的方法。**

适合：民用项目出现争议、报告只有结论而缺少一手事实。

交付：限定民用问题与调查权限 → 列实际参与者、现场过程和可核记录 → 安排自愿访谈与合法观察 → 比较多方记录 → 用调查结果提出可反驳解释 → 输出事实台账、条件结论与补证任务。

**一分钟看懂**：出货延误，主管认定都是员工不努力。

本 Skill 会这样处理：对照订单、材料到货和排班，访谈实际参与者；原因未核前不把态度写成事实。

[用途与同类差异](references/positioning.md)。人物知名度提供发现入口，实际价值来自工作流与可复核产物；不保证星标增长。

## 安装与使用
公开仓库直接提供 Skill，不依赖 GitHub Release。
```sh
npx skills add constantin2088/mao-zedong-investigation-skill
```
也可将仓库内容复制到支持该格式的客户端 Skill 目录，保留以 `mao-zedong-investigation-skill` 命名的文件夹和根目录 SKILL.md。客户端支持范围以其文档为准。安装后提出具体任务，由客户端按描述加载。

**试用任务**：出货延误，主管认定都是员工不努力。

## 内容
- [执行说明](SKILL.md)
- [资料卡](references/sources.md)、[工作表](references/frameworks.md)、[边界](references/boundaries.md)
- [三个示例](examples/demo.md)、[十个行为评测场景](evals/test-cases.md)

## 验证与贡献
```sh
python scripts/check_skill.py . --release
python -m unittest discover -s tests -v
python scripts/check_links.py
```
`--release` 是完整性检查参数，不创建 GitHub Release。CI 在每次提交运行上述检查。独立客户端模型行为评测尚未执行；用例、结构检查与实际模型能力分开报告。
修改时提供来源和定位，区分原文与转译；运行检查后直接提交到仓库。不要创建发布附件作为必需安装步骤。系列标识、链接和推荐由总仓库 catalog/skills.json 同步，避免手工修改受管理区块。

## 许可
项目原创内容使用 [MIT](LICENSE)。链接所指第三方作品保留原权利，本仓库不重新许可它们。
