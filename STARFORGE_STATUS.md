# STARFORGE Status

- Development repository: https://github.com/misza3444/starforge
- Read-only source: https://github.com/pioneerspacesim/pioneer
- Imported release: 20260907
- Source SHA: 824ea0318b0843e74d108022e7b81de1fec0dcbf
- Imported engine, data, and licenses.
- Upstream GitHub workflows preserved under `upstream-ci/`.
- Windows Portable build: not completed yet.

All future game development and repository changes take place only in STARFORGE.

## Windows Portable milestone
- Source change: `src/win32/FileSystemWin32.cpp` detects `portable.flag` next to the executable and redirects game data to `data/` and configuration/saves/mods to `userdata/`.
- Build workflow: `.github/workflows/starforge-portable.yml` compiles with Windows MSVC, reuses the Pioneer third-party dependency repository, builds stock models and packages `STARFORGE-Windows-x64-Portable.zip`.
- The third-party repository is fetched read-only during CI; Pioneer upstream remains untouched.
- Windows CI must finish successfully before any portable archive is considered verified.
