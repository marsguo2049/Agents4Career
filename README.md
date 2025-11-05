# 🔍 Agents4Career

受福尔摩斯启发的多智能体求职优化系统  
A Sherlock Holmes-inspired Multi-Agent System for Job Application Optimization

---

## 💡 灵感来源 | Inspiration

受福尔摩斯演绎推理方法的启发，我构建了一个多智能体系统，每个智能体在求职流程中扮演特定角色——就像贝克街221B的角色们协作破案一样。

Inspired by Sherlock Holmes' deductive reasoning method, I built a multi-agent system where each agent plays a specific role in the job application process - just like the characters at 221B Baker Street working together to solve cases.

---

## 🎯 问题与方案 | Problem & Solution

**痛点 Pain Point**

每个岗位都需要针对性定制简历，手动调整耗时且难以保持一致性。

Every job application requires a tailored resume that matches specific job requirements. Manually customizing resumes for each position is time-consuming and inconsistent.

**方案 Solution**

用多智能体系统自动化流程——分析JD、识别关键需求、生成定制简历。

Automate the process with a team of AI agents that analyze job descriptions, identify key requirements, and generate targeted resumes.

---

## 🕵️ Agent团队 | Agent Team

- **Greg Lestrade（雷斯垂德警官）** - JD分析师：从招聘方角度分析职位需求  
  **JD Analyst**: Analyzes job descriptions from the recruiter's perspective

- **Sherlock Holmes（夏洛克·福尔摩斯）** - 策略顾问：基于Greg报告和cv_kb.md制定简历策略  
  **Strategy Consultant**: Develops resume strategies based on Greg's report and cv_kb.md

- **Dr. Watson（华生医生）** - CV生成专员：按策略生成定制简历  
  **CV Generator**: Creates tailored resumes following strategic recommendations

- **Mrs. Hudson（赫德森太太）** - 知识库管家：维护和更新简历知识库  
  **Knowledge Keeper**: Maintains and updates the resume knowledge base

---

## 🔄 工作流程 | Workflow
```
JD → Greg（需求分析 Analysis）→ Sherlock（策略制定 Strategy）→ Watson（CV生成 Generation）→ 定制简历 Tailored Resume
                                                                                      ↓
                                                                         反馈 Feedback → Hudson（维护 Maintenance）
```

---

## 📁 文件结构 | Structure
```
Career/
├── cv_kb.md              # 简历知识库 Resume knowledge base
├── JD/                   # 职位描述 Job descriptions
└── reports/
    ├── 01_greg/          # 需求分析报告 Requirement analysis
    ├── 02_sherlock/      # 简历策略 Resume strategies
    └── 03_watson/        # 生成的CV Generated CVs
```

---

## 🚀 快速开始 | Quick Start
```bash
# 1. 分析JD需求 Analyze JD requirements
"Greg，分析这个JD：JD/公司_岗位.md"
"Greg, analyze this JD: JD/company_position.md"

# 2. 制定简历策略 Develop resume strategy
"Sherlock，基于Greg的报告制定策略"
"Sherlock, create a strategy based on Greg's report"

# 3. 生成定制CV Generate tailored CV
"Watson，根据Sherlock的策略生成CV"
"Watson, generate CV based on Sherlock's strategy"
```

---

## 📋 功能特点 | Features

- ✅ 自动化JD需求分析 Automated JD requirement analysis
- ✅ 策略化简历定制 Strategic resume customization
- ✅ 标准化输出格式 Consistent output format
- ✅ 知识库持续积累 Knowledge base accumulation
- ✅ 反馈循环优化迭代 Feedback loop for continuous improvement

---

## 🛠️ 技术栈 | Tech Stack

- AI智能体（基于Claude） AI Agents (Claude-based)
- Markdown文档管理 Markdown for documentation
- 结构化工作流自动化 Structured workflow automation

---

## 📄 许可证 | License

Apache-2.0 license

## 🤝 贡献 | Contributing

欢迎提交Issue和PR！  
Issues and PRs are welcome!

## 📬 联系方式 | Contact

如有问题或建议，欢迎提Issue。  
For questions or suggestions, feel free to open an issue.

---

*"当你排除了所有不可能的情况，剩下的无论多么难以置信，一定就是真相。"*  
*"When you have eliminated the impossible, whatever remains, however improbable, must be the truth."*  
— 夏洛克·福尔摩斯 Sherlock Holmes
