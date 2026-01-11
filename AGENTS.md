# Agent Guidelines for Hyprland Config

## Build & Test
- **Reload Config**: `hyprctl reload` (Apply changes immediately).
- **Test Shader**: `hyprshade on <name_without_extension>` (e.g., `hyprshade on amber`).
- **Validation**: No strict linter; check Hyprland logs (`$XDG_RUNTIME_DIR/hypr/hyprland.log`) for errors.

## Code Style
- **Hyprland Conf**:
  - **Comments**: Use `#` for comments.
  - **Indentation**: 4 spaces.
  - **Structure**: Modularize using `source = ...`. Override defaults from `~/.local/share/omarchy` in `~/.config/hypr`.
  - **Naming**: Use lowercase directives (e.g., `windowrulev2`, `bind`).
- **GLSL Shaders**:
  - **Header**: Always include `#version 300 es` and `precision highp float;`.
  - **Indentation**: 4 spaces.
  - **Comments**: Use `//`.

## Conventions
- **Overrides**: NEVER edit files in `~/.local/share/omarchy/`. Create/Edit local overrides instead.
- **Paths**: Use `~` for home directory paths.
- **Scripts**: Ensure shell scripts have shebangs and are executable (`chmod +x`).
