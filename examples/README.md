# Curriculum Examples

This directory contains real-world examples of curricula built using the Curriculum as Code methodology. These examples demonstrate best practices, show different course types in action, and provide inspiration for your own curriculum development.

## Roo Custom Mode Export Files

This directory includes individual YAML export files for specialized Roo custom modes designed for curriculum development. Each file can be imported individually into Roo using the [Import/Export modes functionality](https://docs.roocode.com/features/custom-modes#importexport-modes).

### Core Curriculum as Code Development Modes

- **[`instructional-designer-export.yaml`](instructional-designer-export.yaml)** - General instructional design with learning objectives, content structure, and accessibility compliance
- **[`content-reviewer-export.yaml`](content-reviewer-export.yaml)** - Quality assurance and improvement of existing curriculum materials
- **[`assessment-designer-export.yaml`](assessment-designer-export.yaml)** - Creating effective assessments that accurately measure learning outcomes
- **[`editor-export.yaml`](editor-export.yaml)** - Ensuring flawless English language usage, grammatical accuracy, and active voice

### Instructional Design Model Specialists

- **[`instructional-designer-addie-export.yaml`](instructional-designer-addie-export.yaml)** - ADDIE methodology: Analysis, Design, Development, Implementation, Evaluation
- **[`instructional-designer-sam-export.yaml`](instructional-designer-sam-export.yaml)** - SAM model: Agile, iterative development with rapid prototyping
- **[`instructional-designer-dick-carey-export.yaml`](instructional-designer-dick-carey-export.yaml)** - Dick and Carey systems approach: Detailed goal analysis and precise strategies
- **[`instructional-designer-merrill-export.yaml`](instructional-designer-merrill-export.yaml)** - Merrill's First Principles: Problem-centered, authentic learning experiences
- **[`instructional-designer-gagne-export.yaml`](instructional-designer-gagne-export.yaml)** - Gagné's Nine Events: Systematic lesson design for cognitive processing
- **[`instructional-designer-blooms-export.yaml`](instructional-designer-blooms-export.yaml)** - Bloom's Taxonomy: Cognitive skill development across complexity levels
- **[`instructional-designer-kemp-export.yaml`](instructional-designer-kemp-export.yaml)** - Kemp's model: Flexible, holistic approach with non-linear progression
- **[`instructional-designer-assure-export.yaml`](instructional-designer-assure-export.yaml)** - ASSURE model: Technology-enhanced instruction with media selection
- **[`instructional-designer-backward-design-export.yaml`](instructional-designer-backward-design-export.yaml)** - Understanding by Design: Starting with desired outcomes
- **[`instructional-designer-arcs-export.yaml`](instructional-designer-arcs-export.yaml)** - ARCS model: Motivational design for Attention, Relevance, Confidence, Satisfaction
- **[`instructional-designer-kirkpatrick-export.yaml`](instructional-designer-kirkpatrick-export.yaml)** - Kirkpatrick evaluation: Measuring Reaction, Learning, Behavior, Results

### Using Custom Modes

1. **Download** the specific mode file you need
2. **Import** into Roo using the custom modes import functionality
3. **Switch modes** in Roo: `@mode [mode-slug]` (e.g., `@mode instructional-designer-addie`)
4. **Get specialized assistance** tailored to your instructional design methodology

## Curriculum Examples

### Corporate Training
- **[Leadership Fundamentals](corporate-training/leadership-fundamentals/)** - 3-day management development program
- **[Cybersecurity Awareness](corporate-training/cybersecurity-awareness/)** - Online security training module

### Academic Courses
- **[Introduction to Programming](academic-course/intro-to-programming/)** - Semester-long computer science course
- **[Business Statistics](academic-course/business-statistics/)** - Data analysis course for business students

### Certification Preparation
- **[Project Management PMP](certification-prep/project-management-pmp/)** - Comprehensive exam preparation program

### Microlearning
- **[Time Management Series](microlearning/time-management-series/)** - 5-part skill-building modules
- **[Communication Skills Bites](microlearning/communication-skills-bites/)** - Quick professional development lessons

## How to Use Examples

### Learning from Examples
1. **Browse the structure** - See how real courses are organized
2. **Review content patterns** - Notice formatting and style conventions
3. **Study metadata usage** - Understand how course information is structured
4. **Examine assessments** - Learn assessment design and integration

### Adapting Examples
1. **Copy the structure** you want to emulate
2. **Modify metadata** for your context and audience
3. **Replace content** while maintaining the organizational pattern
4. **Customize assessments** for your learning objectives

### Contributing Examples
Help grow the library by contributing your successful curricula:
1. **Anonymize content** - Remove proprietary or sensitive information
2. **Document your approach** - Explain design decisions and rationale
3. **Include lessons learned** - Share what worked well and what didn't
4. **Test the example** - Ensure others can follow and adapt it

## Example Categories

### By Delivery Method
- **Self-Paced eLearning** - Online modules learners complete independently
- **Instructor-Led Training** - Classroom or virtual instructor-facilitated courses
- **Blended Learning** - Combination of self-paced and instructor-led components
- **Just-in-Time Learning** - Performance support and microlearning

### By Content Type
- **Skill Development** - Practical competency building
- **Knowledge Transfer** - Information and concept learning
- **Compliance Training** - Required training for regulations or policies
- **Leadership Development** - Management and leadership capability building

### By Industry
- **Technology** - Software, IT, and technical skills
- **Healthcare** - Medical training and patient care
- **Finance** - Financial services and regulatory compliance
- **Manufacturing** - Safety, processes, and quality training

## Quality Standards

All examples in this directory meet these criteria:
- **Complete Structure** - Include all necessary files and folders
- **Clear Documentation** - Comprehensive README files and inline comments
- **Best Practices** - Demonstrate proper instructional design principles
- **Accessibility** - Meet WCAG 2.1 AA accessibility standards
- **Reusability** - Easily adaptable for similar use cases

## Getting Started with Examples

### Quick Start
1. **Choose an example** similar to your curriculum needs
2. **Copy the entire folder** to your project workspace
3. **Review the README** for specific guidance and context
4. **Customize metadata** in the `metadata/` folder
5. **Replace content** with your material while keeping the structure

### Detailed Study
1. **Read the documentation** to understand design rationale
2. **Examine content progression** and learning flow
3. **Analyze assessment strategy** and alignment
4. **Study asset organization** and naming conventions
5. **Review accessibility features** and implementation

## Example File Structure

Each example follows this standard organization:

```
example-name/
├── content/                    # All curriculum content
│   ├── modules/               # Course modules or lessons
│   ├── assessments/           # Quizzes and evaluations
│   └── resources/             # Supporting materials
├── assets/                    # Media and documents
│   ├── images/               # Visual content
│   ├── videos/               # Video files and transcripts
│   └── documents/            # PDFs and downloads
├── metadata/                  # Course configuration
│   ├── course-info.yml       # Basic course information
│   ├── learning-objectives.yml # Learning outcomes
│   └── assessment-rubrics.yml # Evaluation criteria
└── README.md                 # Example-specific documentation
```

## Licensing and Usage

### Example Content Licensing
- Examples are provided under **CC BY 4.0** license
- You may adapt, remix, and share with attribution
- Commercial use is permitted
- Credit the original creators when adapting

### Attribution Requirements
When using examples as starting points:
1. **Acknowledge the source** in your documentation
2. **Note significant adaptations** you've made
3. **Maintain copyright notices** from original authors
4. **Consider contributing improvements** back to the community

## Support and Feedback

### Getting Help
- **Review documentation** in the `docs/` folder first
- **Check example README files** for specific guidance
- **Search existing issues** in the project repository
- **Create new issues** for questions or problems

### Providing Feedback
- **Rate examples** - Let us know which ones are most helpful
- **Suggest improvements** - Identify gaps or enhancement opportunities
- **Share success stories** - Tell us how examples helped your projects
- **Contribute new examples** - Expand the library with your successful curricula

## Future Examples

We're continuously adding new examples. Planned additions include:
- **Virtual Reality Training** - Immersive learning experiences
- **Mobile-First Learning** - Smartphone-optimized curriculum
- **AI-Enhanced Content** - Personalized and adaptive learning
- **Global Accessibility** - Multi-language and cultural adaptation

---

**Remember**: Examples are starting points, not final solutions. Always adapt content to your specific audience, context, and learning objectives.