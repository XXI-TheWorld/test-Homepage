## Why

The background music uses an absolute file path (`D:/youxi/Sakura.mp3`) which only works on the original developer's machine. To make the project portable and work on any machine, the audio source must use a relative path.

## What Changes

- Modify the `<audio>` element's `src` attribute in `index.html` to use a relative path
- Change from: `src="D:/youxi/Sakura.mp3"` (absolute path)
- Change to: `src="./music/Sakura.mp3"` (relative path, works in any checkout of the project)

## Capabilities

### New Capabilities
None - this is a simple path correction, not a new capability.

### Modified Capabilities
None - existing behavior remains the same (playing background music), only the implementation path is corrected.

## Impact

- **Affected file**: `index.html` (audio element src attribute)
- **Music file location**: `./music/Sakura.mp3` (relative to project root)
- **No breaking changes**: Functionality unchanged, only portability improved
