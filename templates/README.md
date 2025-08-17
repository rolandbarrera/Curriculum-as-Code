# Curriculum Templates

This directory contains templates for different types of curriculum structures. Each template provides a starting point for creating courses, modules, and learning content using the Curriculum as Code methodology.

## Available Templates

### Course Types

- **[eLearning Module](elearning-module/)** Self paced online courses with interactive content
- **[Instructor Led Training](instructor-led/)** Classroom based courses with facilitator guides
- **[Virtual ILT (VILT)](vilt/)** Online instructor led sessions with virtual collaboration
- **[Lab Exercise](lab-exercise/)** Hands on practical training with step by step instructions

### Content Blocks

- **[Assessment Types](content-blocks/assessment-types/)** Reusable assessment templates
- **[Activity Templates](content-blocks/activity-templates/)** Interactive learning activities
- **[Content Structures](content-blocks/content-structures/)** Standard content layouts

## Using Templates

1. **Choose the appropriate template** for your curriculum type
2. **Copy the template folder** to your project location
3. **Customize the metadata** in `metadata/course-info.yml`
4. **Replace placeholder content** with your actual curriculum
5. **Maintain the folder structure** for consistency

## Template Structure

Each template follows this standard structure:

```
template-name/
├── content/                 # All curriculum content in Markdown
├── assets/                  # Media files, images, documents
├── metadata/                # Course information and configuration
└── README.md               # Template-specific instructions
```

## Customization Guidelines

- **Keep folder structures** - They enable tool automation and consistency
- **Use Markdown format** - Ensures portability and version control
- **Include metadata** - Enables automation and content management
- **Follow naming conventions** - Use kebab-case for folders, descriptive names for files

## Contributing Templates

Have a new template idea? Follow these steps:

1. Create the template following the standard structure
2. Include comprehensive README.md with usage instructions
3. Add example content that demonstrates best practices
4. Test the template with real curriculum development
5. Submit as a pull request with documentation

## Best Practices

- **Start simple** - Use basic templates first, then customize
- **Maintain consistency** - Follow established patterns and conventions
- **Document decisions** - Include rationale for template choices
- **Test thoroughly** - Validate templates with actual content creation
- **Share improvements** - Contribute enhancements back to the community