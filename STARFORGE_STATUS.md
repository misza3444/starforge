# STARFORGE Status

- Development repository: https://github.com/misza3444/starforge
- Read-only source: https://github.com/pioneerspacesim/pioneer
- Imported release: 20260907
- Source SHA: 824ea0318b0843e74d108022e7b81de1fec0dcbf
- Imported engine, data, and licenses.
- Upstream GitHub workflows preserved under `upstream-ci/`.
- Windows Portable build: compiled, packaged and uploaded successfully in GitHub Actions run 39678411869 (Windows x64).

All future game development and repository changes take place only in STARFORGE.

## Windows Portable milestone
- Source change: `src/win32/FileSystemWin32.cpp` detects `portable.flag` next to the executable and redirects game data to `data/` and configuration/saves/mods to `userdata/`.
- Build workflow: `.github/workflows/starforge-portable.yml` compiles with Windows MSVC, reuses the Pioneer third-party dependency repository, builds stock models and packages `STARFORGE-Windows-x64-Portable.zip`.
- The third-party repository is fetched read-only during CI; Pioneer upstream remains untouched.
- Windows CI must finish successfully before any portable archive is considered verified.

## Verified build result
- GitHub Actions run: https://github.com/misza3444/starforge/actions/runs/39678411869
- Outcome: success (compile, stock modelcompiler, CMake install, ZIP packaging, artifact upload).
- Artifact name: STARFORGE-Windows-x64-Portable
- Artifact ID: 12381229642
- Artifact size: 685227995 bytes; archive is wrapped by GitHub Actions artifact packaging.
- Expiry: 2026-11-04 UTC (14-day retention).
- Manual Windows launch and save/load smoke testing remain to be performed.
