# Copilot Instructions for AIWorldAlarm_2

## Project Overview
AIWorldAlarm_2 is a Java-based application project. This document provides guidance for GitHub Copilot when assisting with code generation and modifications in this project.

## Technology Stack
- **Language**: Java
- **IDE**: Visual Studio Code
- **Build System**: Java Projects (VS Code Java extension)

## Project Structure
```
AIWorldAlarm_2/
├── .vscode/          # VS Code configuration
│   └── settings.json # Java project settings
├── src/              # Source code directory
│   └── App.java      # Main application entry point
├── lib/              # External dependencies (JAR files)
├── bin/              # Compiled output (generated)
└── README.md         # Project documentation
```

## Development Guidelines

### Code Style and Conventions
- Follow standard Java naming conventions:
  - Classes: PascalCase (e.g., `App`, `AlarmManager`)
  - Methods: camelCase (e.g., `main`, `setAlarm`)
  - Constants: UPPER_SNAKE_CASE (e.g., `MAX_RETRIES`)
  - Variables: camelCase (e.g., `alarmTime`, `userName`)
- Use meaningful variable and method names
- Add Javadoc comments for public classes and methods
- Keep methods focused and single-purpose
- Use proper indentation (4 spaces)

### Project-Specific Guidelines
- Main entry point is in `src/App.java`
- Place all source files in the `src` directory
- External JAR dependencies should be placed in the `lib` directory
- Compiled classes are automatically generated in the `bin` directory

### Code Organization
- Keep the `main` method in the `App` class as the application entry point
- Create separate classes for different functionalities
- Use packages to organize related classes when the project grows

### Error Handling
- Use try-catch blocks for exception handling
- Provide meaningful error messages
- Log errors appropriately for debugging

### Testing
- Write unit tests for new functionality
- Place test files in a separate test directory if needed
- Use JUnit or similar testing frameworks

## Build and Run Instructions

### Compiling the Project
The project uses VS Code's Java extension for compilation. The compiled output is automatically generated in the `bin` folder.

### Running the Application
```bash
# Without external dependencies
java -cp bin App

# With external dependencies (Unix/macOS)
java -cp bin:lib/* App

# With external dependencies (Windows)
java -cp bin;lib/* App
```

### Adding Dependencies
1. Place JAR files in the `lib` directory
2. The `.vscode/settings.json` is configured to include all JAR files from `lib/**/*.jar`

Example `.vscode/settings.json`:
```json
{
    "java.project.sourcePaths": ["src"],
    "java.project.outputPath": "bin",
    "java.project.referencedLibraries": [
        "lib/**/*.jar"
    ]
}
```

## When Generating Code

### DO:
- Follow Java best practices and conventions
- Write clean, readable code with proper formatting
- Add appropriate comments for complex logic
- Handle exceptions properly
- Consider null safety
- Use Java standard library when possible

### DON'T:
- Don't use deprecated Java features
- Don't hardcode sensitive information
- Don't create overly complex nested structures
- Don't ignore compiler warnings
- Don't forget to handle edge cases

## Common Patterns for This Project

### Main Class Structure
```java
public class App {
    public static void main(String[] args) throws Exception {
        // Application logic here
    }
}
```

### Exception Handling Pattern
```java
try {
    // Code that might throw exception
} catch (SpecificException e) {
    System.err.println("Error: " + e.getMessage());
    // Handle or rethrow
}
```

## AI-Assisted Development Tips
- When adding new features, create separate classes in the `src` directory
- Suggest appropriate design patterns for the functionality being implemented
- Recommend relevant Java libraries for common tasks
- Provide complete, compilable code examples
- Include error handling in code suggestions
- Consider Java version compatibility

## Notes for Contributors
- This is a VS Code Java project
- Ensure your code compiles without errors
- Test your changes before committing
- Update this document if project structure or conventions change
