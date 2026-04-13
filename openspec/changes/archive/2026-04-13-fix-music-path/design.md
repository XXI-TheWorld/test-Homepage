## Context

The `index.html` file contains an `<audio>` element for background music with an absolute path `src="D:/youxi/Sakura.mp3"`. This path only works on the original developer's machine and breaks when the project is cloned to another location.

## Goals / Non-Goals

**Goals:**
- Make the music source path portable across different machines and checkout locations

**Non-Goals:**
- Not changing audio format, codec, or playback behavior
- Not adding new audio features (loop, controls, etc.)

## Decisions

- **Use relative path `./music/Sakura.mp3`**: The `./` prefix references the project root directory, making the path work regardless of where the project is cloned.

  | Approach | Pros | Cons |
  |----------|------|------|
  | `./music/Sakura.mp3` (chosen) | Works in any checkout, portable | Requires music folder at project root |
  | Absolute path | None for portability | Breaks on other machines |
  | `../music/Sakura.mp3` | None | Incorrect relative to index.html location |

## Risks / Trade-offs

- **Risk**: If the `music` folder is moved or renamed, the path breaks.
  - **Mitigation**: Ensure the `music` folder stays at project root. This is a project convention.
