# Copilot Instructions for gdscript
## Code Style

### Indentation
- Use tabs for indentation, not spaces.

### Type System
- Avoid type inference. Always use explicit static types.
- Prefer static typed variables: `var player_id: int = 0`
- Prefer static return types on all functions: `func get_player_id() -> int:`
- Use const declarations instead of magic numbers and strings: `const MOVE_SPEED: float = 5.0`

### Node References
- Use `@onready` with explicit type annotations and node path syntax for local node references.
- Example: `@onready var collision_shape: CollisionShape3D = $CollisionShape3D`
- This pattern ensures type safety, performance optimization (nodes are cached), and self-documenting code.
- Always specify the full type name (e.g., `CollisionShape3D`, not inferred types).

### Naming Conventions
- Use `snake_case` for functions and variables: `var player_position`, `func calculate_damage()`
- Use `PascalCase` for classes and types: `class PlayerController`, `enum GameState`
- Prefix private functions with underscore: `func _process_input() -> void:`

## Code Organization

### Variable Declaration Order
1. Signals
2. Const declarations
3. @export variables
4. @onready variables
5. Regular var declarations

### Function Declaration Order
1. Built-in lifecycle functions (_ready, _process, _physics_process, etc.)
2. Private functions (prefixed with underscore)
3. Public functions

## Control Flow

### Conditionals
- Prefer null checks and early returns over nested conditionals.
- Example: Use guard clauses to exit early rather than deeply nested if/else blocks.

### Error Handling
- Prefer explicit error handling over silent failures.
- Print errors or emit signals when issues occur rather than silently continuing.

## Code Architecture

### Composition Over Inheritance
- Prefer composition and component-based architecture over deep inheritance hierarchies.
- Use scripts as components that can be attached to nodes rather than creating complex base classes.
- Keep inheritance chains shallow (ideally 1-2 levels deep).

### Loose Coupling
- Avoid tight coupling between systems and scripts.
- Use signals and event buses (like `EventBus`) for communication between unrelated systems.
- Pass dependencies explicitly through function parameters or via autoloads when appropriate.
- Minimize direct node references; prefer finding nodes through paths or using signals.

### Modularity
- Keep scripts focused on a single responsibility.
- Split large functionality into separate scripts/components.
- Use the `systems/` directory for cross-cutting concerns and managers.
- Use the `autoloads/` directory for global services that multiple systems depend on.

## Documentation

### Code Comments
- Avoid excess documentation.
- Prefer self-documenting variable and function names that clarify intent.
- Only comment non-obvious logic or complex algorithms.

### Markdown Files
- Avoid generating documentation (.md) files without being explicitly asked.
- Allow the user to request documentation generation when needed.

### UID Files
 - Do not manually create or edit Godot .uid files (for example `*.tscn.uid` or `*.gd.uid`).
	 The Godot editor automatically manages and generates these UID files; creating them by hand
	 can cause conflicts or inconsistent asset metadata. Let the editor handle UID files.