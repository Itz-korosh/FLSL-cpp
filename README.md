# FLSL-cpp

FLSL makes the annoying stuff you rewrite in every C++ project — batch commands,
file I/O, logging — into simple one-liners.

## Why?

FLSL-cpp is made to make code files smaller, coding simpler, and help the
C++ world grow.

## Status

Pre-release. No builds yet, design in progress.
First release: 0.1 (soon™)

## Planned Features

- File I/O that can't leak — one-line ReadFile / WriteFile
- Run batch / shell commands inline
- FLog — simple logging
- (more as they come)

## Target API (not implemented yet)

**Option 1 — everything in one include:**

```cpp
#include <FlslCpp/Flsl.hpp>

int main() {
    FlslFio::WriteFile("hello.txt", "hi from FLSL");
    auto text = FlslFio::ReadFile("hello.txt");

    FlslBatch::RunBatchInline("echo hello");
}
```

**Option 2 — modular, include only what you need:**

```cpp
#include <FlslCpp/FlslFio.hpp>
#include <FlslCpp/FlslBatch.hpp>

int main() {
    FlslFio::WriteFile("hello.txt", "hi from FLSL");
    auto text = FlslFio::ReadFile("hello.txt");

    FlslBatch::RunBatchInline("echo hello");
}
```

## Author

ItzKorosh (Korosh Jale), Iran. Made with love. 🇮🇷

## License

MIT © 2026 Korosh Jale — see [LICENSE](LICENSE).
