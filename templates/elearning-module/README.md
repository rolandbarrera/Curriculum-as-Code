# eLearning Module Template

This template provides a complete structure for creating self-paced online learning modules using the Curriculum as Code methodology.

## Template Structure

```
elearning-module/
├── content/
│   ├── 01-introduction.md          # Course introduction and overview
│   ├── 02-learning-objectives.md   # Detailed learning objectives
│   ├── 03-lessons/                 # Individual lesson content
│   │   ├── lesson-01.md            # Sample lesson structure
│   │   └── lesson-template.md      # Template for new lessons
│   ├── 04-assessments/             # Quizzes and evaluations
│   │   ├── quiz-01.md              # Sample quiz structure
│   │   └── assessment-template.md  # Template for new assessments
│   └── 05-resources.md             # Additional resources and references
├── assets/                         # Media and supporting files
│   ├── images/                     # Course images and graphics
│   ├── videos/                     # Video content and transcripts
│   └── documents/                  # PDF resources and downloads
├── metadata/                       # Course configuration and data
│   ├── course-info.yml             # Basic course information
│   ├── learning-objectives.yml     # Structured learning objectives
│   └── assessment-rubrics.yml      # Assessment criteria and scoring
└── README.md                       # This file
```

## Getting Started

1. **Copy this template** to your project directory:
   ```bash
   cp -r templates/elearning-module/ my-new-course/
   cd my-new-course/
   ```

2. **Customize course metadata** in `metadata/course-info.yml`:
   ```yaml
   title: "Your Course Title"
   description: "Brief course description"
   target_audience: "Who this course is for"
   estimated_duration: "X hours"
   difficulty_level: "Beginner/Intermediate/Advanced"
   ```

3. **Update learning objectives** in `metadata/learning-objectives.yml`

4. **Replace placeholder content** in the `content/` folder with your actual curriculum

5. **Add your assets** to the appropriate folders in `assets/`

## Content Guidelines

### Lesson Structure
Each lesson should follow this format:
- Clear learning objectives
- Introduction/hook
- Content delivery with examples
- Practice activities
- Knowledge check/quiz
- Summary and next steps

### Assessment Integration
- Formative assessments throughout lessons
- Summative assessments at module completion
- Self-reflection opportunities
- Practical application exercises

### Accessibility Requirements
- Use proper heading hierarchy (H1, H2, H3)
- Include alt text for all images
- Provide transcripts for video content
- Ensure color contrast meets WCAG 2.1 AA standards

## File Naming Conventions

- **Lessons**: `lesson-01-topic-name.md`, `lesson-02-next-topic.md`
- **Assessments**: `quiz-01-knowledge-check.md`, `final-assessment.md`
- **Assets**: `descriptive-name.jpg`, `lesson-01-diagram.png`
- **Videos**: `lesson-01-intro.mp4`, `lesson-01-intro-transcript.txt`

## Metadata Schema

### course-info.yml
```yaml
title: string
description: string
target_audience: string
prerequisites: array
estimated_duration: string
difficulty_level: string
tags: array
language: string
accessibility_features: array
```

### learning-objectives.yml
```yaml
course_objectives:
  - objective: string
    bloom_level: string
    assessment_method: string
module_objectives:
  - module: string
    objectives:
      - objective: string
        bloom_level: string
```

## AI Assistant Integration

This template works optimally with Curriculum as Code AI agents:

- **Curriculum Outline Generator**: Use to structure lessons and flow
- **Content Reviewer**: Review lessons for quality and consistency
- **Assessment Creator**: Generate quizzes and evaluations
- **Accessibility Checker**: Validate accessibility compliance

## Quality Checklist

Before finalizing your eLearning module:

- [ ] All metadata files are complete and accurate
- [ ] Learning objectives are clear and measurable
- [ ] Content follows logical progression
- [ ] Assessments align with learning objectives
- [ ] All assets have appropriate alt text
- [ ] Video content includes transcripts
- [ ] Links are functional and appropriate
- [ ] Consistent formatting throughout
- [ ] Mobile-friendly content structure
- [ ] Accessibility requirements met

## Next Steps

1. Customize this template for your specific course
2. Use AI assistants to generate initial content outlines
3. Develop content following the established structure
4. Test with target audience representatives
5. Iterate based on feedback
6. Publish and maintain using version control

## Support

For questions about using this template:
- Review the main [documentation](../../docs/)
- Check [examples](../../examples/) for inspiration
- Create an issue in the project repository