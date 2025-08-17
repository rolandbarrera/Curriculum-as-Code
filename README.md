# Curriculum as Code

AI is transforming the Learning & Development world. You can either adapt or get left behind. This methodology puts you ahead of the curve by rebuilding your content creation process from the ground up, with AI context engineering at its core.

Using software development tools and AI, you treat curriculum development like a software project. You manage your curriculum as code, turning the common Instructional Design models into a software development process for your content. Multiple focused AI agents collaborate on building content, streamlining the process and sparking creativity. Git style version control tracks every change like a codebase, keeping your projects structured and iterable. Automation handles repetitive tasks. And the game changer: you keep AI contextually aware across multiple long sessions, ensuring it stays on track from day to day.

This method transforms content creation and pushes the boundaries of what instructional design can accomplish with a software based mindset.

## Understanding Context: The Whiteboard Analogy

When using any AI tool, you are filling up a context window. Think of the context window like a whiteboard. The more information you write on the board, the more confused your AI tool becomes about the big picture. This is where AI hallucinations happen most often. Eventually, you have to erase the board by starting a new session and beginning fresh, but now you've lost all your context.

AI models process information in units called "tokens" - roughly equivalent to words or word fragments. Each model has a maximum token limit for its context window (typically 8K to 200K+ tokens). As you approach this limit, the AI's performance degrades. More critically, using your entire token budget leaves no room for the AI to generate thoughtful responses. It's like filling your whiteboard so completely that there's no space left to work out solutions. Best practice is to use only 60-80% of available tokens for input, reserving the remainder for high-quality AI output.

Context engineering solves this problem. It enables you to capture and compress the important context so it's easily accessible by the AI when needed at a later time. The tools manage that context window effectively, so you can focus on your tasks without having to shift gears back and forth between different activities. Instead of losing everything when you start over, your AI maintains awareness of what matters most for your project.

## Context Engineering: The Foundation

**What is Context Engineering?**

"Context engineering is the discipline of building dynamic systems that supply an LLM with everything it needs to accomplish a task. To understand this, it's essential to realize that an LLM's 'prompt' is not just a single string of text, but an entire context window of input the model sees before producing output. This context includes multiple components beyond the immediate user question."
— [The New Stack](https://thenewstack.io/context-engineering-going-beyond-prompt-engineering-and-rag/)

"Context engineering is building dynamic systems to provide the right information and tools in the right format such that the LLM can plausibly accomplish the task."
— [LangChain Blog](https://blog.langchain.com/the-rise-of-context-engineering/)

In curriculum development, context engineering transforms how AI assistants understand and contribute to your instructional design process. Instead of starting from scratch each session, your AI partners maintain deep awareness of your project goals, content standards, learner profiles, and design decisions across extended development cycles. This creates a persistent, intelligent workspace where AI becomes a true collaborator in building learning experiences.

## What is Curriculum as Code?

Curriculum as Code applies context engineering and software development best practices to instructional design, enabling:

- **Version Control**: Track every change to your curriculum like a codebase
- **Human in the Loop Collaboration**: Multiple instructional designers working together seamlessly with AI assistants, maintaining human oversight and review at critical decision points to ensure quality, accuracy, and pedagogical soundness
- **Modular Design**: Reusable content blocks and standardized templates
- **AI Assisted Development**: Leverage Cline or Roo AI assistants for enhanced productivity while preserving human expertise and judgment
- **Documentation Driven**: Clear, readable Markdown format for all content

## Human in the Loop: The Essential Partnership

Curriculum as Code doesn't remove humans from the development process—it empowers more meaningful human participation. Traditional curriculum development often forces one person to wear multiple hats, juggling content creation, review, quality assurance, and project management. This methodology opens up the entire development process, allowing teams to add Human in the Loop gates wherever they add value.

The methodology adopts proven software development practices for curriculum teams:

**Flexible Review Gates**: Add content review checkpoints at any stage—from initial concept to final delivery. Subject matter experts, instructional designers, accessibility specialists, or learners themselves can provide feedback when it matters most.

**Collaborative Workflows**: Multiple team members can contribute simultaneously. Fork projects to explore different approaches, submit changes for review, or collaborate on specific modules without stepping on each other's work.

**Release Management**: Designate release managers who approve curriculum changes before they go live. Establish quality gates, approval workflows, and version control that matches your organization's needs.

**Distributed Expertise**: Leverage specialized roles throughout development. Learning engineers handle technical implementation, SMEs focus on content accuracy, accessibility experts ensure compliance, and instructional designers drive pedagogical strategy.

These collaborative processes are optional but available when needed. Teams can adopt as much or as little structure as their projects require, scaling from individual creators to large distributed teams using the same foundational methodology.

The goal is AI-enhanced human collaboration, not AI replacement. Technology handles repetitive tasks while humans focus on creative direction, strategic decisions, and meaningful interactions that improve learning outcomes.

## Quick Start

1. **Clone this repository**
   ```bash
   git clone https://github.com/rolandbarrera/curriculum-as-code.git
   cd curriculum-as-code
   ```

2. **Follow the setup guide**
   - See [`docs/howto.md`](docs/howto.md) for detailed VSCode and AI assistant setup
   - Choose between Cline (basic) or Roo (advanced) workflows

3. **Choose a template**
   - Browse [`templates/`](templates/) for course structures
   - Copy and customize for your curriculum needs

4. **Start creating**
   - All content in Markdown format
   - Organized folder structures
   - AI assisted content development

## Repository Structure

```
curriculum-as-code/
├── docs/                     # Documentation and guides
├── templates/                # Course structure templates
├── examples/                 # Sample curricula
└── .vscode/                  # VSCode configuration
```

## Documentation

- **[Setup Guide](docs/howto.md)** - Complete VSCode and AI assistant setup
- **[Agent Creation](docs/agents.md)** - Custom AI assistants for ID workflows
- **[Methodology](docs/methodology.md)** - Core principles and best practices
- **[Best Practices](docs/best-practices.md)** - Guidelines for effective curriculum development

## Templates Available

- **eLearning Module** - Self paced online courses
- **Instructor Led Training** - Classroom based courses
- **Virtual ILT (VILT)** - Online instructor led sessions
- **Lab Exercises** - Hands on practical training
- **Microlearning** - Bite sized learning modules

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