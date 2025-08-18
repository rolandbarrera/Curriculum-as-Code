# Curriculum as Code
```python
# Rethinking old broken approaches to developing curriculum by implementing Curriculum as Code

old_approach = "Outdated Curriculum Development Process"

# Fix by changing to the new methodology
new_methodology = old_approach.replace("Outdated Curriculum Development Process", "Curriculum as Code")

# Output the fixed approach, with new Methodology
for word in new_methodology.split():
    print(word)
```
```
Curriculum 
As
Code
```
AI is transforming the Learning & Development world. You can either adapt or get left behind.

This methodology puts you ahead of the curve by rebuilding your content creation process from the ground up, with AI context engineering at its core.

## Table of Contents

- [The Transformation](#the-transformation)
- [Understanding Context: The Whiteboard Analogy](#understanding-context-the-whiteboard-analogy)
- [Context Engineering: The Foundation](#context-engineering-the-foundation)
- [What is Curriculum as Code?](#what-is-curriculum-as-code)
- [Human in the Loop: The Essential Partnership](#human-in-the-loop-the-essential-partnership)
- [Quick Start](#quick-start)
- [RAG Materials: Context for AI Collaboration](#rag-materials-context-for-ai-collaboration)
- [Repository Structure](#repository-structure)
- [Documentation](#documentation)
- [Project Templates](#project-templates)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## The Transformation

Using software development tools and AI, you treat curriculum development like a software project. You manage your curriculum as code, turning common Instructional Design models into a software development process for your content.

This methodology dramatically accelerates content production. You are now enabled to employ multiple focused AI agents to work together on building content, streamlining the ID process and sparking creativity. Git style version control tracks every change like a codebase, keeping your projects structured and iterable.

Automation handles repetitive tasks. And the game changer: you keep AI contextually aware across multiple long sessions, ensuring it stays on track from day to day.

This method transforms content creation and pushes the boundaries of what instructional design can accomplish with a software-based mindset.



## Understanding Context: The Whiteboard Analogy

When using any AI tool, you are filling up a context window. Think of the context window like a whiteboard. The more information you write on the board, the more confused your AI tool becomes about the big picture.

AI models process information in units called "tokens" - roughly equivalent to words or word fragments. Each model has a maximum token limit for its context window (typically 8K to 200K+ tokens).

As you approach this limit, the AI's performance degrades. More critically, using your entire token budget leaves no room for the AI to generate thoughtful responses. This is where AI hallucinations happen most often.

It's like filling your whiteboard so completely that there's no space left to work out solutions. Best practice is to use only 60-80% of available tokens for input, reserving the remainder for high-quality AI output.

Eventually, you have to erase the board by starting a new session and beginning fresh, but now you've lost all your context.


### The Solution

Context engineering solves this problem. It enables you to capture and compress the important context so it's easily accessible by the AI when needed at a later time.

The tools manage that context window effectively, so you can focus on your tasks without having to shift gears back and forth between different activities.

Instead of losing everything when you start over, your AI maintains awareness of what matters most for your project.



## Context Engineering: The Foundation

### What is Context Engineering?

> "Context engineering is the discipline of building dynamic systems that supply an LLM with everything it needs to accomplish a task. To understand this, it's essential to realize that an LLM's 'prompt' is not just a single string of text, but an entire context window of input the model sees before producing output. This context includes multiple components beyond the immediate user question."
>
> — [The New Stack](https://thenewstack.io/context-engineering-going-beyond-prompt-engineering-and-rag/)

> "Context engineering is building dynamic systems to provide the right information and tools in the right format such that the LLM can plausibly accomplish the task."
>
> — [LangChain Blog](https://blog.langchain.com/the-rise-of-context-engineering/)


### Context Engineering in Curriculum Development

In curriculum development, context engineering transforms how AI assistants understand and contribute to your instructional design process.

Instead of starting from scratch each session, your AI partners maintain deep awareness of your project goals, content standards, learner profiles, and design decisions across extended development cycles.

This creates a persistent, intelligent workspace where AI becomes a true collaborator in building learning experiences.


## What is Curriculum as Code?

Curriculum as Code applies context engineering and software development best practices to instructional design.


### Core Capabilities

- **Version Control**: Track every change to your curriculum like a codebase

- **Human in the Loop Collaboration**: Enables multiple instructional designers working together seamlessly with AI assistants, maintaining human oversight and review at critical decision points to ensure quality, accuracy, and pedagogical soundness

— [How To Use Git to Collaborate with Others [Git Tutorial]](https://www.youtube.com/watch?v=ygqx50-JHEE)

- **Modular Design**: Reusable content blocks and standardized templates

- **AI Assisted Development**: Leverage Cline or Roo AI assistants for enhanced productivity while preserving human expertise and judgment

- **Documentation Driven**: Clear, readable Markdown format for all content



## Human in the Loop: The Essential Partnership

Curriculum as Code doesn't remove humans from the development process—it empowers more meaningful human participation.

Traditional curriculum development often forces one person to wear multiple hats, juggling content creation, review, quality assurance, and project management. This methodology opens up the entire development process, allowing teams to add Human in the Loop gates wherever they add value.


### Proven Development Practices

The methodology adopts proven software development practices for curriculum teams:

**Flexible Review Gates**

Add content review checkpoints at any stage—from initial concept to final delivery. Subject matter experts, instructional designers, accessibility specialists, or learners themselves can provide feedback when it matters most.

**Collaborative Workflows**

Multiple team members can contribute simultaneously. Fork projects to explore different approaches, submit changes for review, or collaborate on specific modules without stepping on each other's work.

**Release Management**

Designate release managers who approve curriculum changes before they go live. Establish quality gates, approval workflows, and version control that matches your organization's needs.

**Distributed Expertise**

Leverage specialized roles throughout development. Learning engineers handle technical implementation, SMEs focus on content accuracy, accessibility experts ensure compliance, and instructional designers drive pedagogical strategy.


### Scalable Collaboration

These collaborative processes are optional but available when needed. Teams can adopt as much or as little structure as their projects require, scaling from individual creators to large distributed teams using the same foundational methodology.

The goal is AI-enhanced human collaboration, not AI replacement. Technology handles repetitive tasks while humans focus on creative direction, strategic decisions, and meaningful interactions that improve learning outcomes.


## Quick Start

Transform your curriculum development process in minutes. Choose your path based on your experience level and project needs.

### Step 1: Create Your Project Workspace

**Start by creating a dedicated folder for your curriculum project:**

```bash
# Create a dedicated folder for your curriculum project
mkdir my-curriculum-project
cd my-curriculum-project

# Open as VSCode workspace
code .
```

*This keeps your project separate and organized, making it easy to manage and share.*

#### Before You Start

**Required:**
- ✅ VSCode installed
- ✅ API key ready (OpenRouter, Anthropic, or OpenAI)

**Optional:**
- Git (for version control)
- Node.js (for automation scripts)

### Step 2: Get Reference Materials (One-time setup)

**Get the Curriculum as Code templates and documentation:**

**Option A: Download (No Git Required)**
- Visit [repository releases](https://github.com/rolandbarrera/curriculum-as-code/releases)
- Download latest zip file
- Extract to your preferred location (e.g., `~/Documents/curriculum-as-code/`)

**Option B: Clone with Git**
```bash
# Clone to a separate location (NOT inside your project)
cd ~/Documents        # macOS/Linux
cd C:\Users\YourName   # Windows
git clone https://github.com/rolandbarrera/curriculum-as-code.git
```

*Keep this separate from your project workspace. This is your reference library.*

### Step 3: Choose Your Path

**Which approach fits your needs?**

**🚀 Basic Start** - Perfect for:
- New curriculum as code developers
- Quick project creation
- Simple workflows

**⚡ Pro Mode** - Ideal for:
- Experienced curriculum as code developers
- Custom project requirements
- Team collaboration
- Advanced AI features
- Large multi-faceted projects

---

### 🚀 Basic Start: Simple Projects

**Perfect for getting started quickly with proven course structures.**

#### 1. Install Cline AI Assistant

- Install Cline extension in VSCode
- Configure with your API key ([setup guide](docs/howto.md#step-3a-setting-up-cline-with-memory-bank))

#### 2. Set up your curriculum project for AI Collaboration

- Copy contents of templates/example-project to my-curriculum-project
- Edit instructions.md to your project specifications

#### 3. Start Your Project

- Initialize the Cline Memory bank by running this command within cline 
```
initialize memory bank
```
- Tell Cline you have instructions for your project.
```
I want to create a new curriculum project. Please use the instructions.md as a guide for this project
```
Your AI assistant will:
- Create all files needed for the Cline Memory bank
- Follow your instructions.md

#### 4. Create content
- Start working with Cline to create your content, ask questions in plan mode, switch to act mode to create.

#### 5. Optional: Add Version Control

```bash
# Optional: Track changes with git (recommended for collaboration)
git init
git add .
git commit -m "first commit"
```

---

### ⚡ Pro Mode: Large detailed programs and projects

**For experienced users who want full control and advanced AI collaboration.**

#### 1. Install and Configure Roo

- Install Roo extension in VSCode
- Configure with your API key ([detailed setup](docs/howto.md#step-3b-setting-up-roo-with-memory-bank))
- Import specialized Instructional Designer modes from [`examples/`](examples/)

#### 2. Set up your advanced curriculum project

- Copy contents of [`templates/pro-mode-project`](templates/pro-mode-project) to your project directory
- Review and customize the pre-configured Memory Bank files
- Edit [`instructions.md`](templates/pro-mode-project/instructions.md) for your complex project requirements

#### 3. Initialize Project with Architect Mode

**Start with Roo's Architect mode for planning:**

```
@mode architect
"I have a new complex curriculum project and advanced RAG materials. Please review the instructions.md and help me plan this curriculum architecture using the Curriculum as Code methodology."
```

#### 4. Advanced Planning & Development

Roo will:
- **Review create a Memory Bank** for context persistence
- **Plan curriculum architecture** based on your instructions
- **Utilize enhanced RAG materials** for comprehensive context
- **Recommend specialized modes** for different phases

#### 5. Switch to Specialized Modes

After planning, switch to specialized modes for implementation:

```
@mode instructional-designer-addie    # For ADDIE methodology
@mode assessment-designer            # For assessment creation
@mode content-reviewer              # For quality assurance
```

#### 6. Optional: Add Version Control

```bash
# Optional: Advanced project management with git
git init
git add .
git commit -m "Initial Pro Mode project setup"
```

---

## RAG Materials: Context for AI Collaboration

### What is RAG

The RAG (Retrieval Augmented Generation) solves the problem of AI losing context between sessions by creating a persistent knowledge base for your project. Without organized context materials, AI tools cannot access information beyond their training data.

We recommend each new curriculum project includes a `rag-materials/` folder for organizing project context materials that help AI assistants understand your specific requirements and maintain awareness across development sessions. 

### How It Works
When interacting with your AI tool (Cline or ROO) you can ask it to either reference the entire rag-material/ folder or specific files within the folder to help the AI gain context on your topic. The `rag-materials/` folder and its contents become a Knowlege Base repository for your project. We understand that this approach to RAG is simple, yet it is effective. We will implememnt more advanced RAG systems in future iterations. 

**AI Integration:** Reference materials in your prompts:
```
"Based on the requirements in rag-materials/, please create..."
```

```
please ingest templates/pro-mode-project/rag-materials/git.md to assist with the creation of a introductory course outline
```

**Basic Start Projects** Simple RAG structure:
```
my-curriculum-project/
├── rag-materials/
│   └── README.md                  # Simple organization guidance
├── content/                       # Your curriculum content
└── assets/                        # Your media files
```

**Pro Mode Projects** Enhanced RAG structure:
```
my-advanced-curriculum/
├── rag-materials/
│   ├── README.md                  # Advanced organization guide
│   ├── analysis-research/         # JTA, learner analysis, performance gaps
│   ├── requirements-constraints/  # Project specs, budgets, compliance
│   ├── reference-materials/       # Standards, templates, style guides
│   ├── stakeholder-context/       # Personas, SME notes, org info
│   └── technical-specs/           # LMS requirements, accessibility
├── content/                       # Your curriculum content
└── assets/                        # Your media files
```

### Using RAG Materials

Add documents that provide background and context:
- Project requirements and constraints
- Research and analysis documents
- Reference materials and style guides
- Stakeholder information and personas
- Technical specifications and standards

**Organization:** Structure however makes sense for your project. The README.md provides suggestions, but you decide what works best.

**Best Practices:** Keep materials in text-based formats (Markdown, TXT, PDF, CSV, JSON, YAML) for optimal AI consumption. Hint: Save PPT files to PDF and Publish existing Rise courses to PDF for easy ingestion to RAG system.

### ✅ Verify Your Setup

After each step, check:
- [ ] Project folder created and opened in VSCode
- [ ] Reference materials accessible at your chosen location
- [ ] AI assistant responds to test message
- [ ] Template copying works correctly (Basic Start) or Memory Bank initializes (Pro Mode)

### Common Issues

**"Template not found"**
- Verify reference repository location
- Check folder permissions
- Update template path in AI prompt with your actual location

**"AI assistant not responding"**
- Verify API key configuration
- Check internet connection
- Restart VSCode

### Next Steps

After setup, explore:

- **[Setup Guide](docs/howto.md)** - Detailed configuration instructions
- **[Examples](examples/)** - Specialized Roo AI modes

**Ready to transform your curriculum development process!**



## Repository Structure

The Curriculum as Code methodology uses two distinct folder structures:

### Reference Repository Structure
*This is what you get when you download/clone the main repository for reference:*

```
curriculum-as-code/                # Reference repository (~/Documents/)
├── docs/                         # Documentation and guides
├── templates/                    # Project starter templates
│   ├── example-project/          # Basic Start template
│   └── pro-mode-project/         # Pro Mode template
├── examples/                     # ID AI modes
└── README.md                     # This guide
```

### Your Project Workspace Structure
*This is what you create for your actual curriculum project:*

**Basic Start Projects:**
```
my-curriculum-project/            # Your project workspace
├── content/                      # Your curriculum content
├── assets/                       # Your media files
├── rag-materials/                # Project context materials
│   └── README.md                 # Organization guidance
├── instructions.md               # Project setup guide
└── (optional) .git/              # Your version control
```

**Pro Mode Projects:**
```
my-advanced-curriculum/           # Your project workspace
├── content/                      # Your curriculum content
├── assets/                       # Your media files
├── rag-materials/                # Enhanced project context
│   ├── analysis-research/        # JTA, learner analysis
│   ├── requirements-constraints/ # Project specs, compliance
│   ├── reference-materials/      # Standards, style guides
│   ├── stakeholder-context/      # Personas, SME notes
│   ├── technical-specs/          # LMS, accessibility specs
│   └── README.md                 # Advanced organization guide
└── (optional) .git/              # Your version control
```

### Key Separation Benefits

- **Clean Independence**: Your project files stay separate from framework files
- **Easy Updates**: Pull latest templates and docs from the reference repository
- **Version Control**: Each project gets its own git history
- **Collaboration**: Share projects without framework overhead
- **Customization**: Modify structures without affecting the reference



## Documentation

- **[Setup Guide](docs/howto.md)** - Complete VSCode and AI assistant setup

- **[Agent Creation](docs/agents.md)** - Custom AI assistants for ID workflows

- **[Methodology](docs/methodology.md)** - Core principles and best practices

- **[Best Practices](docs/best-practices.md)** - Guidelines for effective curriculum development



## Project Templates

- **Curriculum Starter** - Simple project structure with basic folders and guidance

## Contributing

We welcome contributions! See our [contribution guidelines](.github/CONTRIBUTING.md) for details.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

Templates and examples are available under CC BY 4.0 for educational sharing.


## Support

- **Issues**: Report bugs or request features via GitHub Issues

- **Discussions**: Join community discussions in GitHub Discussions

- **Documentation**: Check the [`docs/`](docs/) folder for comprehensive guides


---

**Transform your instructional design process with the power of software development methodologies!**