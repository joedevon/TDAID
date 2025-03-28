# Test-Driven AI Development (TDAID)

> **Applying TDD principles to improve LLM-generated code quality and speed**

## What is TDAID?

Test-Driven AI Development (TDAID) combines the concepts of [Test-Driven Development (TDD)](https://martinfowler.com/bliki/TestDrivenDevelopment.html) with [vibe-coding](https://x.com/karpathy/status/1886192184808149383) to create a more effective way to develop AI-assisted software that is more reliable than vibe-coding alone, while being much faster than traditional TDD.

Instead of manually writing all tests and implementation code, you provide examples of your coding style and testing patterns, then let AI assist in generating both tests and implementation code.

This project aims to coin and define "Test-Driven AI Development" (TDAID) as a new term and methodology in software development, providing a structured approach to leveraging AI in the TDD process.

## ⚠️ Important Note

TDAID trades significantly faster development cycles compared to traditional TDD for increased code review time. You should not skip a robust code review process.

## The TDAID Workflow

1. **Write initial code** - Develop a portion of your feature or system manually
2. **Write initial tests** - Create tests for your initial code implementation
3. **Teach the AI** - These initial code and tests serve as examples for the AI to understand your:
   - Coding style and conventions
   - Project structure
   - Logging patterns
   - Test methodology
4. **AI-assisted test creation** - Ask the AI to write additional test cases
5. **AI-assisted implementation** - Let the AI implement code to pass those tests
6. **Review and refine** - Evaluate the AI-generated code and tests, making adjustments as needed

## Why TDAID Works

LLMs excel at pattern recognition and can quickly learn from your examples. By providing both implementation code and corresponding tests, you're effectively teaching the AI your development approach. The AI can then extend this pattern to similar tasks, maintaining consistency with your existing codebase.

## Origin Story

The concept of TDAID emerged during work on an accessibility evaluation project focused on the Top 6 [WebAIM Million issues](https://webaim.org/projects/million/). The project's structure presented a pattern where similar functionality needed to be implemented across multiple evaluation criteria.

After developing approximately half of the required functionality and corresponding tests, it became apparent that the remaining implementations would follow similar patterns. This created an ideal opportunity to experiment with an AI-assisted approach.

The LLM was provided with the existing codebase and test suite as examples, then tasked with writing additional test cases for the remaining functionality. This established a clear set of expectations through the tests before any implementation code was written – maintaining the core TDD principle.

What was particularly notable was what happened next: After the AI wrote the tests, it was simply asked to run them. Without any explicit prompting to fix the failing tests, the AI recognized that the tests were failing (as expected in TDD) and immediately proceeded to implement the necessary code to make them pass. 

The quality of this unprompted, AI-generated code proved surprisingly high, maintaining consistent style, error handling approaches, and architectural patterns already established in the codebase. This demonstrated an impressive understanding of both the testing intent and implementation requirements.

This experience demonstrated that when provided with sufficient examples of both implementation and testing approaches, LLMs can extend these patterns effectively across similar functionality, potentially offering significant development efficiency while maintaining code quality.

## Best Practices

1. **Start small** - Begin with a well-defined, contained feature
2. **Provide clear examples** - Include several representative code and test examples
3. **Be specific** - Clearly communicate what you want the AI to test and implement
4. **Iterative approach** - Review and refine the AI's work, then ask for improvements
5. **Maintain quality control** - Always review AI-generated code for correctness

## Limitations

TDAID works best when:
- Tasks are similar to your provided examples
- The AI has enough context to understand your project structure
- Requirements can be clearly communicated

It may be less effective for:
- Entirely new features with no similar examples
- Highly complex or specialized algorithms
- Projects with unusual or inconsistent code patterns

## Credits

Created by [Joe Devon](https://www.linkedin.com/in/joedevon/).

## Author

### Joe Devon
- 🐦 Social Media: @joedevon
- 🎙️ Podcast: [Accessibility and Gen. AI](https://www.youtube.com/@a11ygenai)
- 📫 Newsletter: [Joe Dev On Tech](https://www.linkedin.com/newsletters/joe-dev-on-tech-7240847501472194560/) - subscribe to get updates on my projects and articles

## Contributing

This project is in early development. Contributions and feedback are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.