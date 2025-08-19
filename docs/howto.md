# How to Set Up a Curriculum as Code Environment

This guide provides two complete paths for setting up your development environment to use the "Curriculum as Code" methodology with VSCode and AI assistants.

## Table of Contents

### Choose Your Path

**[Path A: Complete Cline Setup & Usage](#path-a-complete-cline-setup--usage)** - Perfect for instructional designers new to coding workflows, simpler projects

**[Path B: Complete Roo Setup & Usage](#path-b-complete-roo-setup--usage)** - Best for experienced users, complex projects, advanced workflows

### Shared Resources
- [Troubleshooting](#troubleshooting)
- [Next Steps](#next-steps)

---

## Path A: Complete Cline Setup & Usage

*Perfect for: Instructional designers new to coding workflows, simpler projects*

Cline is a user-friendly AI assistant with project-specific rules and memory bank integration, designed for straightforward curriculum development workflows.

### A1: Install VSCode

1. **Download VSCode**
   - Visit [https://code.visualstudio.com/](https://code.visualstudio.com/)
   - Download the version for your operating system (Windows, macOS, or Linux)
   - Install following the standard installation process

2. **Additional Prerequisites**
   - **Git** For version control
   - **Node.js** (optional) For any automation scripts you might add later

### A2: Get API Access to LLM Models

Both Cline and other AI assistants require API access to large language models to function. We recommend **OpenRouter.ai** because it provides access to multiple models from different companies through a single API key.

#### Why OpenRouter.ai?

- **Multiple Model Access**: Claude, GPT-4, Gemini, and other leading models in one place
- **Easy Model Switching**: Compare different models for different tasks
- **Simple Setup**: One API key for all models

#### Choosing the Right Model

Before selecting a model, research current performance and pricing using these LLM leaderboards:

- **[Artificial Analysis](https://artificialanalysis.ai/leaderboards/models)** - Comprehensive model performance and cost analysis
- **[LLM Stats](https://llm-stats.com/)** - Real-time model statistics and comparisons
- **[LMSys Chatbot Arena](https://lmarena.ai/leaderboard/)** - Community-driven model rankings based on human preferences

These resources help you choose models that best fit your specific curriculum development tasks and budget requirements.

#### Getting Started with OpenRouter

1. **Create an Account**
   - Visit [https://openrouter.ai/](https://openrouter.ai/)
   - Sign up for a free account
   - Verify your email address

2. **Add Credits**
   - Go to the Credits section in your dashboard
   - Add funds to your account (start with $10-20 for testing)
   - OpenRouter uses pay-per-use pricing

3. **Get Your API Key**
   - Navigate to the API Keys section
   - Create a new API key
   - Copy and securely store your API key (you'll need it for setup)

4. **Choose Your Models**
   - Browse available models in the Models section
   - Use the leaderboard resources above to select models that fit your needs and budget

#### Alternative Options

If you prefer direct access:
- **Anthropic Claude**: [https://console.anthropic.com/](https://console.anthropic.com/)
- **OpenAI GPT**: [https://platform.openai.com/](https://platform.openai.com/)
- **Google Gemini**: [https://ai.google.dev/](https://ai.google.dev/)

#### Security Best Practices

- **Never share your API keys** in code repositories or documentation
- **Use environment variables** to store API keys securely
- **Monitor usage** regularly to avoid unexpected charges
- **Set spending limits** in your account dashboard

### A3: Install and Configure Cline

#### Install Cline Extension

1. Open VSCode Extensions marketplace (`Ctrl+Shift+X` or `Cmd+Shift+X`)
2. Search for "Cline"
3. Install the official Cline extension
4. Follow the [official Cline installation guide](https://docs.cline.bot/)
5. Configure your API key from Step A2 in the Cline settings

#### Configure Cline Memory Bank

For complete Cline Memory Bank setup and usage instructions, follow the official documentation:

**[Cline Memory Bank Setup Guide](https://docs.cline.bot/prompting/cline-memory-bank)**

NOTE: For the Curriculum as Code example workspace, we will add the [Cline Memory Bank Custom Instructions content](https://docs.cline.bot/prompting/cline-memory-bank#getting-started-with-memory-bank) to a file named `.clinerules/01-memory-bank.md` file. 

Cline's Memory Bank automatically manages project context through simple commands. No manual file creation needed.

### A4: Create Your Project Workspace

Before starting any workflow, create a dedicated workspace for your curriculum project:

```bash
# Create a dedicated folder for your curriculum project
mkdir my-curriculum-project
cd my-curriculum-project

# Open as VSCode workspace
code .
```

*This keeps your project separate and organized, making it easy to manage and share.*

#### Get Reference Materials (One-time setup)

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

### A5: Cline Workflows

Choose your workflow based on project complexity and experience level.

#### Basic Start Workflow with Cline

**Perfect for**: New curriculum as code developers, simple projects, quick creation

##### 1. Copy Template and Setup

**Get the Basic Start Template:**
```bash
# Copy from your reference repository location
cp -r ~/Documents/curriculum-as-code/templates/example-project/* ./
```

##### 2. Configure Cline Collaboration

- Edit [`.clinerules/02-instructions.md`](.clinerules/02-instructions.md) to your specifications. If you decide to implement additional Agents you can specify instructions in this file as well.

- Initialize the Cline Memory Bank:
```
initialize memory bank
```

- Start your project:
```
I want to create a new curriculum project. Please use the .clinerules/instructions as a guide for this project
```

##### 3. Create Content with Cline

- Work with Cline to create content in the `content/` folder
- Store media files in `assets/` folder
- Use RAG materials in `rag_material/` for additional context

##### 4. Optional: Add Version Control

```bash
# Track changes with git (recommended for collaboration)
git init
git add .
git commit -m "Initial curriculum project setup"
```

#### Pro Mode Workflow with Cline

**Perfect for**: More complex projects while staying within Cline's capabilities

##### 1. Copy Pro Mode Template

**Get the Pro Mode Template:**
```bash
# Copy from your reference repository location
cp -r ~/Documents/curriculum-as-code/templates/pro-mode-project/* ./
```

##### 2. Configure Advanced Cline Setup

- Edit `.clinerules/02-instructions.md` to your specifications for the more complex project
- Initialize the Cline Memory Bank:
```
initialize memory bank
```

##### 3. Advanced Planning with Cline

```
I have a complex curriculum project. Please review the 02-instructions.md and rag-materials/ folder to understand the full context, then help me plan this curriculum architecture using the Curriculum as Code methodology.
```

##### 4. Enhanced Content Development

Cline will:
- **Review and utilize the Memory Bank** for context persistence
- **Plan curriculum architecture** based on your instructions
- **Utilize enhanced RAG materials** in `rag-materials/` for comprehensive context
- **Guide systematic content development** through the more sophisticated template structure

##### 5. Advanced Version Control

```bash
# Advanced project management with git
git init
git add .
git commit -m "Initial Pro Mode project setup"

# Set up branching strategy
git checkout -b develop
git checkout -b feature/module-1
```

#### Cline Collaboration Best Practices

**Team Setup:**
- Each team member follows the same Cline setup process
- Share Memory Bank configurations and `.clinerules/02-instructions.md` across team
- Establish consistent naming conventions

**Content Standards:**
- Use shared templates and style guides
- Regular team reviews of Memory Bank settings
- Document decisions in Memory Bank files for persistent context

**Version Control Best Practices:**
```bash
# Commit Structure
git add .
git commit -m "feat: add lesson 3 - advanced concepts"
git push origin main

# Branching Strategy
# main - stable, reviewed content
# develop - work in progress  
# feature/lesson-name - individual lessons
```

---

## Path B: Complete Roo Setup & Usage

*Best for: Experienced users, complex projects, advanced workflows*

Roo offers advanced features and multiple specialized modes for sophisticated AI assistance, including custom instructional design methodology modes.

### B1: Install VSCode

1. **Download VSCode**
   - Visit [https://code.visualstudio.com/](https://code.visualstudio.com/)
   - Download the version for your operating system (Windows, macOS, or Linux)
   - Install following the standard installation process

2. **Additional Prerequisites**
   - **Git** For version control
   - **Node.js** (optional) For any automation scripts you might add later

### B2: Get API Access to LLM Models

Roo requires API access to large language models to function. We recommend **OpenRouter.ai** because it provides access to multiple models from different companies through a single API key.

#### Why OpenRouter.ai?

- **Multiple Model Access**: Claude, GPT-4, Gemini, and other leading models in one place
- **Easy Model Switching**: Compare different models for different tasks
- **Simple Setup**: One API key for all models

#### Choosing the Right Model

Before selecting a model, research current performance and pricing using these LLM leaderboards:

- **[Artificial Analysis](https://artificialanalysis.ai/leaderboards/models)** - Comprehensive model performance and cost analysis
- **[LLM Stats](https://llm-stats.com/)** - Real-time model statistics and comparisons
- **[LMSys Chatbot Arena](https://lmarena.ai/leaderboard/)** - Community-driven model rankings based on human preferences

These resources help you choose models that best fit your specific curriculum development tasks and budget requirements.

#### Getting Started with OpenRouter

1. **Create an Account**
   - Visit [https://openrouter.ai/](https://openrouter.ai/)
   - Sign up for a free account
   - Verify your email address

2. **Add Credits**
   - Go to the Credits section in your dashboard
   - Add funds to your account (start with $10-20 for testing)
   - OpenRouter uses pay-per-use pricing

3. **Get Your API Key**
   - Navigate to the API Keys section
   - Create a new API key
   - Copy and securely store your API key (you'll need it for setup)

4. **Choose Your Models**
   - Browse available models in the Models section
   - Use the leaderboard resources above to select models that fit your needs and budget

#### Alternative Options

If you prefer direct access:
- **Anthropic Claude**: [https://console.anthropic.com/](https://console.anthropic.com/)
- **OpenAI GPT**: [https://platform.openai.com/](https://platform.openai.com/)
- **Google Gemini**: [https://ai.google.dev/](https://ai.google.dev/)

#### Security Best Practices

- **Never share your API keys** in code repositories or documentation
- **Use environment variables** to store API keys securely
- **Monitor usage** regularly to avoid unexpected charges
- **Set spending limits** in your account dashboard

### B3: Install and Configure Roo

#### Install Roo Extension

1. Open VSCode Extensions marketplace (`Ctrl+Shift+X` or `Cmd+Shift+X`)
2. Search for "Roo"
3. Install the official Roo extension
4. Follow the Roo setup guide to configure your API key from Step B2

#### Configure Memory Bank

For complete Roo Memory Bank setup instructions, follow the official documentation:

**[Roo Code Memory Bank Setup Guide](https://github.com/GreatScottyMac/roo-code-memory-bank)**

Setup note: The setup guide directs users to an older location for Modes in Roo. Modes can now be found in the "More Actions(Three Dots)" of the menu bar to the right of the Settings and Account sections.

This guide includes:
- Memory Bank package installation
- Configuration and initialization steps
- Usage examples and best practices

#### Understanding Roo Modes

Roo provides multiple specialized modes that you can switch between:

- **Architect Mode**: Plan and design curriculum structure
- **Code Mode**: Create and edit content files
- **Ask Mode**: Get answers and explanations
- **Debug Mode**: Troubleshoot issues and problems
- **Custom Modes**: Create specialized modes for specific tasks

#### Switch Between Modes

```
@mode architect   # Switch to architecture and planning mode
@mode code        # Switch to code mode 
@mode ask         # Switch to question and answer mode
@mode debug       # Switch to troubleshooting mode
```

#### Create Custom Curriculum Modes

For complete instructions on creating custom Roo modes, follow the official documentation:

**[Roo Custom Modes Guide](https://docs.roocode.com/features/custom-modes#importexport-modes)**

This guide covers:
- Creating custom mode files
- Mode configuration and syntax
- Best practices for mode design
- Testing and deployment
- Import/Export functionality for individual mode files

#### Example Custom Modes for Curriculum Development

We've created a comprehensive set of specialized custom modes for curriculum development. Each mode is available as an individual YAML file in our examples folder for easy import:

**[View Examples Folder](../examples/)**

Our collection includes 15 specialized modes organized into two categories:

##### Core Curriculum Development Modes

1. **Instructional Designer**: For creating structured, accessible curriculum content with proper learning objectives and organization
2. **Content Reviewer**: For quality assurance and improvement of existing curriculum materials
3. **Assessment Designer**: For creating effective assessments that accurately measure learning outcomes
4. **Editor**: For ensuring flawless English language usage, grammatical accuracy, and active voice in all curriculum content

##### Instructional Design Model Specialists

These modes are specialized for specific instructional design methodologies:

5. **ADDIE Model Instructional Designer**: Systematic curriculum development through Analysis, Design, Development, Implementation, and Evaluation phases
6. **SAM Model Instructional Designer**: Agile, iterative development with rapid prototyping and frequent feedback cycles
7. **Dick and Carey Model Instructional Designer**: Systems approach with detailed goal analysis and precise instructional strategies
8. **Merrill's First Principles Instructional Designer**: Problem-centered learning with authentic, real-world applications
9. **Gagné's Nine Events Instructional Designer**: Systematic lesson design optimizing cognitive processing and retention
10. **Bloom's Taxonomy Instructional Designer**: Cognitive skill development across remembering, understanding, applying, analyzing, evaluating, and creating
11. **Kemp's Instructional Design Model Designer**: Flexible, holistic approach allowing non-linear progression through design elements
12. **ASSURE Model Instructional Designer**: Technology-enhanced instruction with emphasis on media selection and active participation
13. **Backward Design Instructional Designer**: Understanding by Design methodology starting with desired outcomes
14. **ARCS Model Instructional Designer**: Motivational design focusing on Attention, Relevance, Confidence, and Satisfaction
15. **Kirkpatrick Model Instructional Designer**: Comprehensive evaluation measuring Reaction, Learning, Behavior, and Results

##### Using These Modes

To switch to any of these specialized modes in Roo:

```
@mode instructional-designer-addie    # For ADDIE methodology
@mode instructional-designer-sam      # For SAM methodology
@mode instructional-designer-merrill  # For Merrill's First Principles
@mode assessment-designer            # For assessment creation
@mode content-reviewer              # For quality assurance
```

To use these modes, download the individual YAML files from the [`examples/`](../examples/) folder and import them using Roo's custom mode import functionality. Each mode can be imported individually based on your specific needs.

Note: When adding a new mode it is suggested to append the [Code Memory bank module](https://github.com/GreatScottyMac/roo-code-memory-bank/blob/main/modules/memory_bank_strategy_code.yml) to each modes "Mode-specific Custom Instructions" section. This should keep the memory bank working for each custom ID mode added.

### B4: Create Your Project Workspace

Before starting any workflow, create a dedicated workspace for your curriculum project:

```bash
# Create a dedicated folder for your curriculum project
mkdir my-curriculum-project
cd my-curriculum-project

# Open as VSCode workspace
code .
```

*This keeps your project separate and organized, making it easy to manage and share.*

#### Get Reference Materials (One-time setup)

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

### B5: Roo Workflows

Choose your workflow based on project complexity. Roo excels at sophisticated, multi-phase curriculum development projects.

#### Basic Start Workflow with Roo

**Perfect for**: Experienced users starting with simpler projects but wanting advanced AI capabilities

##### 1. Copy Template and Setup

**Get the Basic Start Template:**
```bash
# Copy from your reference repository location
cp -r ~/Documents/curriculum-as-code/templates/example-project/* ./
```

##### 2. Initialize with Architect Mode

```
@mode architect
"I want to create a new curriculum project. Please review the .clinerules/instructions and help me plan this curriculum architecture using the Curriculum as Code methodology."
```

##### 3. Advanced Planning & Development

Roo will:
- **Review and create a Memory Bank** for context persistence
- **Plan curriculum architecture** based on your instructions
- **Utilize RAG materials** in `rag_material/` for comprehensive context
- **Recommend specialized modes** for different phases

##### 4. Switch to Specialized Modes

After planning, use specialized modes for implementation:

```
@mode instructional-designer    # For general curriculum design
@mode assessment-designer      # For assessment creation
@mode content-reviewer        # For quality assurance
```

##### 5. Optional: Add Version Control

```bash
# Track changes with git (recommended for collaboration)
git init
git add .
git commit -m "Initial Roo curriculum project setup"
```

#### Pro Mode Workflow with Roo

**Perfect for**: Complex projects, enterprise-level programs, multi-methodology approaches

##### 1. Copy Pro Mode Template

**Get the Pro Mode Template:**
```bash
# Copy from your reference repository location
cp -r ~/Documents/curriculum-as-code/templates/pro-mode-project/* ./
```

##### 2. Initialize with Architect Mode

```
@mode architect
"I have a new complex curriculum project. Please review the instructions.md and help me plan this curriculum architecture using the Curriculum as Code methodology."
```

##### 3. Advanced Planning & Development

Roo will:
- **Review and create a Memory Bank** for context persistence
- **Plan curriculum architecture** based on your instructions
- **Utilize enhanced RAG materials** in `rag-materials/` for comprehensive context
- **Recommend specialized modes** for different phases

##### 4. Switch to Specialized Methodology Modes

After planning, use methodology-specific modes for implementation:

```
@mode instructional-designer-addie    # For ADDIE methodology
@mode instructional-designer-sam      # For SAM methodology
@mode instructional-designer-merrill  # For Merrill's First Principles
@mode assessment-designer            # For assessment creation
@mode content-reviewer              # For quality assurance
```

##### 5. Advanced Version Control

```bash
# Advanced project management with git
git init
git add .
git commit -m "Initial Pro Mode project setup"

# Set up branching strategy
git checkout -b develop
git checkout -b feature/module-1
```

#### Multi-Phase Development with Roo

Roo excels at managing complex, multi-phase curriculum development:

##### Phase 1: Analysis & Planning
```
@mode architect
"Let's start with a comprehensive analysis phase. Review all RAG materials and help me create a detailed curriculum architecture."
```

##### Phase 2: Instructional Design
```
@mode instructional-designer-addie    # or your chosen methodology
"Now let's move into the design phase using the ADDIE model. Please review our architecture and begin detailed curriculum design."
```

##### Phase 3: Content Development
```
@mode code
"Time to create the actual content. Please help me implement our design with proper markdown structure and organization."
```

##### Phase 4: Assessment Creation
```
@mode assessment-designer
"Let's create comprehensive assessments that align with our learning objectives and chosen methodology."
```

##### Phase 5: Review & Quality Assurance
```
@mode content-reviewer
"Please conduct a thorough review of all curriculum content for quality, consistency, and alignment."
```

#### Roo Collaboration Best Practices

**Team Setup:**
- Each team member follows the same Roo setup process
- Share Memory Bank configurations and custom modes across team
- Establish consistent mode-switching protocols

**Content Standards:**
- Use shared templates and style guides
- Regular team reviews of Memory Bank settings
- Document mode usage and decisions in Memory Bank files for persistent context

**Advanced Version Control:**
```bash
# Commit Structure with mode context
git add .
git commit -m "feat: add lesson 3 using ADDIE mode - advanced concepts"
git push origin main

# Branching Strategy for complex projects
# main - stable, reviewed content
# develop - work in progress
# feature/methodology-name - methodology-specific branches
# feature/assessment - assessment development
# review/content-qa - quality assurance branch
```

**Human in the Loop Integration:**
- Add review gates at content creation, quality assurance, and approval stages
- Use git workflows for collaborative review and approval processes
- Leverage specialized AI modes for different team roles and expertise areas

---

## Troubleshooting

### Common Issues

1. **AI Assistant Not Recognizing Context**
   - **For Cline**: Verify Memory Bank files are properly configured, check file permissions in `.cline/` directories, restart VSCode and reinitialize Memory Bank
   - **For Roo**: Check memory bank files are properly configured, verify mode transitions are working, restart VSCode and reinitialize Roo

2. **Markdown Formatting Issues**
   - Install recommended VSCode extensions
   - Use markdownlint to identify formatting problems
   - Reference template files for proper structure

3. **Git Conflicts**
   - Use clear commit messages
   - Coordinate with team on file editing
   - Resolve conflicts in content files carefully

4. **Mode Switching Issues (Roo)**
   - Verify custom modes are properly imported
   - Check mode syntax: `@mode mode-name`
   - Restart Roo if modes are not responding

5. **Memory Bank Issues**
   - **For Cline**: Use `initialize memory bank` command to reset
   - **For Roo**: Check memory bank files exist and are readable
   - Verify API key configuration is correct

### Getting Help

- **Cline**: Reference [official documentation](https://docs.cline.bot/)
- **Roo**: Check [Roo documentation](https://docs.roocode.com/)
- **Curriculum as Code**: Create issues in the project repository
- **Community**: Join discussions in project forums

---

## Next Steps

After completing setup with either path:

1. **Read the Agents Guide** - See [`docs/agents.md`](./agents.md) for creating specialized AI assistants
2. **Explore Examples** - Check `examples/` folder for sample curricula and custom modes
3. **Start Creating** - Use templates to build your first course
4. **Join Community** - Contribute templates and improvements back to the project

### Path-Specific Next Steps

**If you chose Path A (Cline):**
- Focus on mastering Memory Bank commands
- Explore advanced `.clinerules/instructions.md` configurations
- Consider upgrading to Path B (Roo) for complex projects

**If you chose Path B (Roo):**
- Master mode switching and custom mode creation
- Explore methodology-specific modes for your instructional design approach
- Contribute new custom modes back to the community

Remember: The goal is to apply software development best practices to curriculum development while keeping the process simple and focused on educational outcomes.