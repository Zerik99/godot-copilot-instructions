# Godot Copilot Instructions

This repository provides GitHub Copilot instructions specifically tailored for Godot projects. It defines coding standards and workflow rules for Code Style, Organization, Architecture, and Documentation to ensure consistent, maintainable outputs when using Copilot in Godot development.

## Purpose

The goal of these instructions is to guide GitHub Copilot in generating GDScript code that adheres to best practices for Godot game development. By providing clear guidelines on type safety, node references, naming conventions, and architectural patterns, Copilot can produce code that is more aligned with Godot's ecosystem and community standards.

## Installation

To use these Copilot instructions in your Godot project:

1. Copy the `github/` folder from this repository into the root directory of your existing Godot project.
2. The folder contains a `.gdignore` file, which prevents the Godot editor from including it in your project structure.
3. **Important Note**: These instructions only work with external code editors that support GitHub Copilot, such as Visual Studio Code. The Godot editor itself does not use or recognize Copilot instructions. Without a compatible editor, this folder will have no effect on your coding experience.

## Usage

These instructions are primarily designed for use with Visual Studio Code, where GitHub Copilot can read the `copilot-instructions.md` file in the `.github/` directory. Other code editors that support GitHub Copilot instructions may also work, but compatibility is not guaranteed.

The instructions cover:
- **Code Style**: Indentation, type system, node references, and naming conventions.
- **Code Organization**: Variable and function declaration order.
- **Control Flow**: Conditionals and error handling.
- **Code Architecture**: Composition over inheritance, loose coupling, and modularity.
- **Documentation**: Guidelines for comments and avoiding unnecessary documentation.

## Why Copilot Instructions for Godot?

Godot uses GDScript, a Python-like scripting language with unique features and conventions. Without specific guidance, Copilot might generate code that doesn't follow Godot's best practices, such as:
- Overuse of dynamic typing (hinders type safety and performance).
- Tightly coupled node referencing patterns, contrary to Godot's preference for loose coupling.
- Non-standard naming conventions.
- Architectural decisions that don't leverage Godot's component-based design.

These instructions ensure that Copilot-generated code is:
- Type-safe and performant.
- Consistent with Godot's coding standards.
- Maintainable and scalable for game development projects.

## Contributing

Contributions are welcome! If you have suggestions for improving the guidelines or adding new sections, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

