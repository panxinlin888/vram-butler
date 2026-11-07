# Contributing

Thanks for your interest in VRAM Butler.

## Development environment

- Windows 10 or Windows 11, 64-bit
- PowerShell 7 for development (the script also runs on Windows PowerShell 5.1)
- [ps2exe](https://github.com/MScholtes/PS2EXE) to build the single-file executable

## Run from source

```powershell
pwsh -STA -File 显存查看与释放.ps1
```

Headless modes:

```powershell
pwsh -File 显存查看与释放.ps1 -帮助
pwsh -File 显存查看与释放.ps1 -后台 -列表 -结果文件 list.json
pwsh -File 显存查看与释放.ps1 -后台 -目标程序 "chrome,msedge" -已授权 -结果文件 run.json
```

## Build the executable

```powershell
Install-Module ps2exe -Scope CurrentUser
Import-Module ps2exe
Invoke-ps2exe -inputFile 显存查看与释放.ps1 -outputFile 显存管家.exe `
  -iconFile 显存管家.ico -noConsole -STA -x64 -DPIAware `
  -title 显存管家 -description "显存查看与释放 · 星辰软件" `
  -company 星辰软件 -product 显存管家 `
  -copyright "© 2026 星辰软件 · qq591277494@126.com" `
  -version 1.0.0.0
```

## Source conventions

- Single file, Chinese identifiers for functions, classes and variables; only platform API references remain in English
- No comments in the source
- UTF-8 with BOM, CRLF line endings (required by Windows PowerShell 5.1)
- Keep the protected process list intact: system components, explorer and agent hosts must never be terminated
- Headless termination must remain gated by the explicit `-已授权` flag and an explicit target list
- UI changes must keep the dark style and must be verified with a screenshot before submitting

## Pull requests

1. Open an issue first for larger changes.
2. Keep the change focused; avoid unrelated refactors.
3. Describe what you tested: interactive UI, headless listing, dry run and authorized release.
4. Update the README and changelog when user-visible behavior changes.

## License of contributions

By contributing, you agree that your contributions are licensed under the PolyForm Noncommercial License 1.0.0, the same license as this project.
