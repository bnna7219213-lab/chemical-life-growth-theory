# 新的生命形态与成体生长理论：化学视角

**English title:** *Chemical Perspectives on New Life Forms and Adult Growth Theory*  
**Repository / distribution name:** `chemical-life-growth-theory`

> **阶段：研究计划 / 早期原型（v0.1 理论框架与骨架代码）。**
>
> 暂无可运行的模拟模型。当前仓库只有一个已形式化的理论规格（`docs/MODEL_SPEC.md`）和一组骨架 Python 模块（`src/chemobio_model/`），所有实现均标注为 `TODO`。本阶段的研究目的是把局部组织状态调控问题先形式化，再逐步做最小模拟，与已知实验数据对照——**不是**已经验证过的生物学预测工具，更不构造新生命体。

## 项目是什么

一个以**化学视角**研究生命形态与成体生长问题的理论和计算项目。远期问题涉及化学结构、反应网络、物质与能量交换如何支持可生长系统；当前从已知碳基组织入手，建立可对照数据的局部状态转移模型。

- **第一建模对象（v0.1）：小鼠肠上皮**——由于其细胞周转快、公开表观遗传与再生数据充分（H3K36 甲基化、YAP、Wnt 等），便于与已有实验对照。
- **化学视角是后续建模主线：**逐步把抽象信号和资源代理映射到可定义的分子、反应/结合过程、动力学参数、物质通量与能量约束；先标清证据与未知，不把化学分子当作可任意调节的旋钮。
- **参照（当前不建模）：** 硅基芯片作为信息处理但不代谢、不自我维护的工程对照；假设性硅基生化仅做约束层面讨论，不做具体模型。

“新的生命形态与成体生长理论”是项目的长期理论方向；当前工作仍限于已知组织建模与文献对照。模拟用于提出和检验假设，不等于构造生命体。

## 项目不是什么

- **不**构造完整的全细胞数字孪生；首轮只做无空间的细胞状态群体模型。
- **不**治疗、不预测临床效果。
- **不**产出生命体或"替代生化"。
- **不**包含可识别的人类健康数据。

## 目录结构

```
.
├── README.md              # 本文件
├── PLAN.md                # 开发推进计划
├── LICENSE                # MIT 许可证（代码）
├── CITATION.cff           # 机器可读引文
├── pyproject.toml
├── .gitignore
├── LICENSE-docs.txt       # CC-BY-4.0（文档）
├── docs/
│   ├── PROJECT_CHARTER.md # 工作名称、工作假设、比较对象、边界
│   ├── THEORY_MAP.md      # 理论知识图谱 & 证据 vs 假设
│   ├── MODEL_SPEC.md      # 数学规格 v0.1
│   ├── DATA_PLAN.md       # 数据来源、字典、重用条件
│   └── REFERENCES.md      # 起始参考文献（6 篇已验证）
├── src/
│   └── chemobio_model/    # Python 骨架模块（均标注 TODO）
├── data/
│   ├── raw/               # 公开数据的只读副本（当前为空）
│   └── processed/         # 清洗衍生数据
├── notebooks/             # 探索性分析
└── reports/               # 临时结果与图表
```

## 当前进度

- [x] 项目章程、理论图谱、数学规格 v0.1、数据计划、参考文献 6 篇（含 DOI 验证）
- [x] Python 骨架模块 `states / parameters / transitions / resources / simulator / metrics / io / visualize`
- [ ] 选定组织的状态变量表（已选定小鼠肠上皮，待形式化）
- [ ] 参数先验与数据来源标注
- [ ] 最小可运行原型（无空间随机事件调度）
- [ ] 与肠上皮 H3K36 甲基化再生数据的对照测试

## 许可证

- 代码：[MIT License](LICENSE)
- 文档：[CC-BY-4.0](LICENSE-docs.txt)

## 引用

若使用本仓库的理论规格或骨架代码，请按 [CITATION.cff](CITATION.cff) 引用。
