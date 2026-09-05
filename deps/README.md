# Dependencies

This directory should contain the pre-compiled native dependencies.

## For CI (GitHub Actions)
Dependencies are automatically downloaded from the GitHub Release
asset `remill-deps-win32-x64.zip` during the prebuild workflow.

## For local development
Run the full rebuild pipeline from the monorepo:
```powershell
cd extensions/hexcore-remill
python _rebuild_mt.py
```

Or download the deps zip from the latest release:
```powershell
gh release download v0.5.2 -p "remill-deps-win32-x64.zip" -R AkashaCorporation/hexcore-remill
Expand-Archive remill-deps-win32-x64.zip -DestinationPath .
```
