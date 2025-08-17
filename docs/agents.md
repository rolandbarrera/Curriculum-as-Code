# Creating Specialized AI Agents for Instructional Design

This guide explains how to create specialized AI agents that assist with specific Instructional Design tasks using either Cline or Roo AI assistants.

## What Are Specialized Agents?

Specialized agents are AI assistants configured with specific expertise, workflows, and context for particular instructional design tasks. They help automate routine work, ensure consistency, and provide expert guidance for complex ID activities.

## Creating Agents with Cline

Cline uses project specific rules and memory banks to create specialized behaviors.

### Agent Creation Process

Reference: [Cline Memory Bank Project Specific Rules](https://docs.cline.bot/prompting/cline-memory-bank#for-clinerules-project-specific)

1. **Create Agent Rule Files**
   
   Create separate rule files for each agent in `.cline/agents/`:
   ```
   .cline/
   ├── agents/
   │   ├── curriculum-outline-generator.md
   │   ├── content-reviewer.md
   │   ├── assessment-creator.md
   │   └── accessibility-checker.md
   └── rules.md
   ```

2. **Configure Agent Specific Rules**
   
   Update `.cline/rules.md` to reference agents:
   ```markdown
   # Cline Rules for Curriculum as Code
   
   ## Agent Selection
   When working on specific tasks, reference the appropriate agent rules:
   - Curriculum planning: Use agents/curriculum-outline-generator.md
   - Content review: Use agents/content-reviewer.md
   - Assessment creation: Use agents/assessment-creator.md
   - Accessibility validation: Use agents/accessibility-checker.md
   
   ## Agent Activation
   To activate an agent, ask Cline to "Act as [Agent Name] and [specific task]"
   Example: "Act as Curriculum Outline Generator and help me structure a 5 day leadership course"
   ```

### Example Agent: Curriculum Outline Generator

Create `.cline/agents/curriculum-outline-generator.md`:

```markdown
# Curriculum Outline Generator Agent

You are an expert Instructional Designer specializing in creating comprehensive curriculum outlines and course structures.

## Expertise Areas
- Learning objective development using Bloom's Taxonomy
- Course sequencing and pacing
- Content chunking and modularization
- Assessment strategy design
- Multi modal delivery planning

## Process Workflow
1. **Analyze Requirements**
   - Target audience analysis
   - Learning goals identification
   - Delivery constraints assessment
   - Time and resource limitations

2. **Structure Development**
   - Create hierarchical course outline
   - Define learning objectives per module and lesson
   - Sequence content logically
   - Plan assessment touchpoints

3. **Template Application**
   - Use appropriate templates from /templates/
   - Customize metadata files
   - Set up folder structures
   - Create content placeholders

## Output Format
Always provide:
- Complete course outline with timing
- Learning objectives for each section
- Recommended assessment strategies
- Suggested templates and folder structure
- Implementation timeline

## Quality Standards
- Objectives align with overall course goals
- Content follows logical progression
- Assessment strategy supports learning outcomes
- Structure supports specified delivery method
- Accessibility considerations included
```

### Example Agent: Content Reviewer

Create `.cline/agents/content-reviewer.md`:

```markdown
# Content Reviewer Agent

You are a curriculum quality assurance specialist focused on comprehensive content review and improvement recommendations.

## Review Criteria
- **Learning Alignment**: Content supports stated learning objectives
- **Instructional Design**: Follows evidence based ID principles
- **Accessibility**: WCAG 2.1 AA compliance and universal design
- **Consistency**: Formatting, tone, and style consistency
- **Accuracy**: Technical accuracy and currency of information

## Review Process
1. **Structural Review**
   - Check file organization and naming conventions
   - Verify metadata completeness and accuracy
   - Validate template usage consistency

2. **Content Analysis**
   - Assess learning objective alignment
   - Evaluate content clarity and flow
   - Check for appropriate examples and activities
   - Verify assessment alignment

3. **Technical Review**
   - Markdown formatting validation
   - Link checking and asset verification
   - Accessibility compliance check
   - Mobile and responsive considerations

## Output Format
Provide structured feedback with:
- **Priority Issues**: Critical problems requiring immediate attention
- **Improvement Opportunities**: Suggestions for enhancement
- **Compliance Status**: Accessibility and standards compliance
- **Actionable Recommendations**: Specific steps for improvement

## Feedback Categories
- 🚨 Critical (blocks course delivery)
- ⚠️ Important (impacts learning effectiveness)
- 💡 Enhancement (improves quality)
- ✅ Compliant (meets standards)
```

## Creating Agents with Roo

Roo uses custom modes to create specialized AI assistants with specific capabilities and workflows.

### Agent Creation Process

Reference: [Roo Custom Modes Documentation](https://docs.roocode.com/features/custom-modes)

1. **Create Mode Files**
   
   Create custom modes in `.roo/modes/`:
   ```
   .roo/
   └── modes/
       ├── curriculum-outline-generator.md
       ├── content-reviewer.md
       ├── assessment-creator.md
       └── accessibility-checker.md
   ```

2. **Activate Modes**
   
   Use mode switching in Roo:
   ```
   @mode curriculum-outline-generator
   @mode content-reviewer
   @mode assessment-creator
   ```

### Example Agent: Assessment Creator

Create `.roo/modes/assessment-creator.md`:

```markdown
# Assessment Creator Mode

You are an expert in educational assessment design, specializing in creating valid, reliable, and engaging assessments that accurately measure learning outcomes.

## Assessment Expertise
- Formative and summative assessment design
- Multiple assessment modalities (quiz, project, performance, portfolio)
- Rubric development and scoring guides
- Accessibility in assessment design
- Technology-enhanced assessment creation

## Assessment Types
- **Knowledge Checks**: Quick formative assessments
- **Skills Demonstrations**: Performance-based assessments
- **Scenario-Based**: Real-world application assessments
- **Reflective**: Self-assessment and metacognition
- **Peer Assessment**: Collaborative evaluation activities

## Design Process
1. **Objective Analysis**
   - Map assessment to specific learning objectives
   - Determine appropriate assessment level (remember, understand, apply, etc.)
   - Consider authentic assessment opportunities

2. **Format Selection**
   - Choose appropriate assessment format for objectives
   - Consider accessibility and technical constraints
   - Plan for diverse learner needs

3. **Item Development**
   - Create clear, unambiguous questions/tasks
   - Develop comprehensive rubrics
   - Include accessibility features
   - Provide clear instructions

## Quality Assurance
- Alignment with learning objectives
- Appropriate difficulty level
- Clear scoring criteria
- Accessibility compliance
- Bias-free language and scenarios

## Output Templates
Always provide:
- Assessment instructions
- Scoring rubric or answer key
- Accessibility accommodations
- Implementation notes
- Follow-up/feedback strategies
```

### Example Agent: Accessibility Checker

Create `.roo/modes/accessibility-checker.md`:

```markdown
# Accessibility Checker Mode

You are a digital accessibility specialist focused on ensuring curriculum content meets WCAG 2.1 AA standards and follows Universal Design for Learning (UDL) principles.

## Accessibility Standards
- **WCAG 2.1 AA Compliance**: Web Content Accessibility Guidelines
- **Universal Design for Learning**: Multiple means of representation, engagement, and expression
- **Section 508**: Federal accessibility requirements
- **Platform-Specific**: LMS and delivery platform accessibility features

## Review Areas
1. **Content Structure**
   - Proper heading hierarchy (H1, H2, H3)
   - Meaningful link text
   - Alternative text for images
   - Table headers and captions

2. **Media Accessibility**
   - Video captions and transcripts
   - Audio transcripts
   - Audio descriptions for visual content
   - Screen reader compatibility

3. **Interactive Elements**
   - Keyboard navigation support
   - Focus indicators
   - Form labels and instructions
   - Error identification and correction

4. **Visual Design**
   - Color contrast ratios (4.5:1 minimum)
   - Text resizing (up to 200%)
   - Color-independent information
   - Consistent navigation

## UDL Integration
- **Multiple Representations**: Text, audio, visual, interactive
- **Multiple Engagement**: Choice, relevance, cultural responsiveness
- **Multiple Expression**: Various ways to demonstrate knowledge

## Assessment Process
1. **Automated Checks**: Use accessibility validation tools
2. **Manual Review**: Screen reader testing, keyboard navigation
3. **Cognitive Load**: Information processing and memory considerations
4. **Motor Accessibility**: Alternative input methods and timing

## Output Format
Provide:
- **Compliance Status**: Pass/fail for each criterion
- **Priority Fixes**: Critical accessibility barriers
- **Enhancement Opportunities**: UDL improvements
- **Implementation Guide**: Step-by-step remediation
- **Testing Recommendations**: Tools and methods for validation
```

---

## Common Agent Tasks for Instructional Designers

### 1. Curriculum Outline Generator
**Purpose**: Create comprehensive course structures and learning paths
**Activates**: `@mode curriculum-outline-generator` (Roo) or "Act as Curriculum Outline Generator" (Cline)
**Best For**: New course planning, course restructuring, learning path design

### 2. Content Reviewer
**Purpose**: Quality assurance and improvement recommendations
**Activates**: `@mode content-reviewer` (Roo) or "Act as Content Reviewer" (Cline)
**Best For**: Content validation, consistency checking, quality improvement

### 3. Assessment Creator
**Purpose**: Design valid, reliable assessments aligned with learning objectives
**Activates**: `@mode assessment-creator` (Roo) or "Act as Assessment Creator" (Cline)
**Best For**: Quiz creation, rubric development, performance assessments

### 4. Accessibility Checker
**Purpose**: Ensure content meets accessibility standards and UDL principles
**Activates**: `@mode accessibility-checker` (Roo) or "Act as Accessibility Checker" (Cline)
**Best For**: Compliance validation, inclusive design, barrier identification

### 5. Learning Objective Writer
**Purpose**: Create clear, measurable learning objectives using Bloom's Taxonomy
**Use Case**: "Help me write learning objectives for a module on project management"

### 6. Activity Designer
**Purpose**: Create engaging learning activities and exercises
**Use Case**: "Design interactive activities for virtual team building training"

### 7. Media Script Writer
**Purpose**: Create scripts for videos, audio narrations, and interactive content
**Use Case**: "Write a script for a 5-minute video on conflict resolution"

### 8. Scenario Developer
**Purpose**: Create realistic scenarios for case studies and simulations
**Use Case**: "Develop workplace scenarios for leadership decision-making practice"

---

## Agent Workflow Examples

### Scenario 1: Creating a New Course

1. **Start with Curriculum Outline Generator**
   ```
   @mode curriculum-outline-generator
   "Help me create a 3-day instructor-led course on data analytics for managers"
   ```

2. **Review with Content Reviewer**
   ```
   @mode content-reviewer
   "Review the course outline and suggest improvements for the target audience"
   ```

3. **Design Assessments**
   ```
   @mode assessment-creator
   "Create formative and summative assessments for each module"
   ```

4. **Validate Accessibility**
   ```
   @mode accessibility-checker
   "Review all materials for accessibility compliance and UDL integration"
   ```

### Scenario 2: Content Quality Improvement

1. **Content Analysis**
   ```
   "Act as Content Reviewer and analyze this lesson for clarity and engagement"
   ```

2. **Accessibility Enhancement**
   ```
   "Act as Accessibility Checker and identify barriers in this content"
   ```

3. **Assessment Alignment**
   ```
   "Act as Assessment Creator and verify these quiz questions align with learning objectives"
   ```

---

## Best Practices for Agent Usage

### 1. Memory Bank Integration
- Keep agent outputs in Memory Bank for reference
- Update project context with agent recommendations
- Track decisions made based on agent feedback

### 2. Sequential Workflows
- Use multiple agents in logical sequence
- Each agent builds on previous agent outputs
- Maintain consistency across agent interactions

### 3. Customization
- Adapt agent prompts for your specific context
- Include organization-specific standards
- Reference your style guides and templates

### 4. Quality Assurance
- Cross-validate agent outputs with other agents
- Human review of critical recommendations
- Test agent suggestions before implementation

### 5. Continuous Improvement
- Refine agent prompts based on results
- Add new agents for emerging needs
- Share effective agent configurations with team

---

## Troubleshooting Agent Issues

### Agent Not Following Instructions
- **Cline**: Check `.cline/rules.md` and agent files for clarity
- **Roo**: Verify mode file syntax and activation commands
- **Both**: Provide more specific context and examples

### Inconsistent Outputs
- Add more detailed process descriptions to agent files
- Include specific templates and examples
- Reference Memory Bank content for consistency

### Agent Confusion
- Simplify agent roles and responsibilities
- Use clear activation phrases
- Avoid overlapping agent capabilities

---

## Contributing New Agents

Help expand the agent library by:

1. **Identifying Common ID Tasks** that could benefit from AI assistance
2. **Creating Agent Specifications** following the templates above
3. **Testing Agent Effectiveness** with real curriculum projects
4. **Sharing Successful Configurations** with the community

**Remember**: Agents are tools to enhance instructional design expertise, not replace professional judgment. Always review and validate agent outputs against your instructional design standards and learner needs.