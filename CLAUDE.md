# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Agents4Career is a Sherlock Holmes-inspired multi-agent system for job application optimization. It consists of five specialized AI agents that work together to analyze job descriptions, develop resume strategies, generate tailored CVs, prepare for interviews, and maintain a knowledge base.

## Agent Architecture

The system uses five Claude-based agents, each with specific responsibilities:

### 1. Greg Lestrade (`greg-lestrade`)
- **Role**: JD Analysis Expert
- **Function**: Analyzes job descriptions from recruiter perspective to define ideal candidate profiles
- **Input**: Job description files from `JD/` directory
- **Output**: Requirement analysis reports in `reports/01_greg/`
- **Usage**: "Greg，从招聘方角度分析：JD/公司_岗位.md"

### 2. Sherlock Holmes (`sherlock-holmes`)
- **Role**: Resume Strategy Consultant
- **Function**: Develops targeted resume strategies based on Greg's analysis and candidate background
- **Input**: Greg's reports + `cv_kb.md` knowledge base
- **Output**: Strategy documents in `reports/02_sherlock/`
- **Usage**: "Sherlock，基于Greg的报告制定策略"

### 3. Dr. Watson (`dr-watson`)
- **Role**: CV Generation Specialist
- **Function**: Creates tailored resumes following Sherlock's strategic recommendations
- **Input**: Sherlock's strategies + `cv_kb.md` personal background
- **Output**: Generated CVs in `reports/03_watson/`
- **Usage**: "Watson，根据Sherlock的策略生成CV"

### 4. Irene Adler (`irene-adler`)
- **Role**: Interview Strategy Expert
- **Function**: Creates comprehensive interview preparation guides based on Greg's analysis, Sherlock's strategies, and interview experiences
- **Input**: Greg's reports + Sherlock's strategies + `Interview/` experience files + `cv_kb.md`
- **Output**: Interview preparation guides in `reports/04_irene/`
- **Usage**: "Irene，基于Greg和Sherlock的报告制定面试攻略"

### 5. Mrs. Hudson (`mrs-hudson`)
- **Role**: Knowledge Base Manager
- **Function**: Maintains and updates the resume knowledge base system
- **Input**: `cv_sup.md` with new information
- **Output**: Updated knowledge base files
- **Usage**: "Hudson，整合cv_sup.md的新信息到知识库"

## File Structure

```
Agents4Career/
├── README.md                    # Project documentation
├── cv_kb.md                     # Main resume knowledge base (create if needed)
├── cv_sup.md                    # Supplementary information for Hudson (create if needed)
├── cv_detail.md                 # Detailed resume version (create if needed)
├── cv_concise.md                # Concise resume version (create if needed)
├── JD/                          # Job descriptions (create as needed)
├── Interview/                   # Interview experiences (create as needed)
├── reports/                     # Generated reports (create as needed)
│   ├── 01_greg/                 # Greg's requirement analyses
│   ├── 02_sherlock/             # Sherlock's strategies
│   ├── 03_watson/               # Watson's generated CVs
│   └── 04_irene/                # Irene's interview guides
└── .claude/
    └── agents/                  # Agent configuration files
        ├── greg.md
        ├── sherlock.md
        ├── watson.md
        ├── irene.md
        └── hudson.md
```

## Workflow Process

1. **Analysis Phase**: Greg analyzes the job description from recruiter perspective
2. **Strategy Phase**: Sherlock creates targeted resume strategy based on analysis
3. **Generation Phase**: Watson generates the actual tailored CV
4. **Interview Phase**: Irene creates comprehensive interview preparation guides
5. **Maintenance Phase**: Hudson updates the knowledge base with new information/feedback

## Key Files to Create

Before using the system, create these essential files:

- `cv_kb.md` - Contains your complete professional background, skills, experience
- `cv_sup.md` - Temporary file for new information to be processed by Hudson
- `JD/` directory - Place job descriptions here for analysis
- `Interview/` directory - Store interview experiences and preparation materials

## Usage Examples

```bash
# 1. Analyze a job description
"Greg，分析这个JD：JD/字节跳动_数据分析师.md"

# 2. Develop resume strategy
"Sherlock，基于Greg的报告制定策略"

# 3. Generate tailored CV
"Watson，根据Sherlock的策略生成CV"

# 4. Create interview preparation guide
"Irene，基于Greg和Sherlock的报告制定面试攻略"

# 5. Update knowledge base
"Hudson，整合cv_sup.md的新信息到知识库"
```

## Development Notes

- This is a documentation-based system using Claude agents via slash commands
- No build process, dependencies, or code compilation required
- All outputs are markdown files for easy review and editing
- The system is designed for iterative improvement through feedback loops
- Agents work sequentially, with each building upon the previous agent's output

## File Naming Conventions

- Greg's reports: `{公司}_{岗位}_需求分析_{YYYYMMDD_HHMMSS}.md`
- Sherlock's strategies: `{公司}_{岗位}_简历策略_{YYYYMMDD_HHMMSS}.md`
- Watson's CVs: `{公司}_{岗位}_CV_{YYYYMMDD_HHMMSS}.md`
- Irene's interview guides: `{公司}_{岗位}_面试攻略_{YYYYMMDD_HHMMSS}.md`
- CV templates: `{公司}_CV格式_{YYYYMMDD_HHMMSS}.md`

## Agent Access

The agents are accessed through Claude Code's Task tool using their respective subagent types:
- `greg-lestrade` for JD analysis
- `sherlock-holmes` for strategy development
- `dr-watson` for CV generation
- `irene-adler` for interview preparation (Note: Currently requires general-purpose agent)
- `mrs-hudson` for knowledge base maintenance
