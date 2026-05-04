  ## Issues Encountered

- Calibre segmentation fault during metadata editing
- Qt accessibility warnings (QAccessibleTable errors)
- GPU rendering instability on Linux Mint Cinnamon
- Library detection failures inside Flatpak sandbox
- Virtual libraries incorrectly showing mixed content

## Debug Steps

- Disabled GPU rendering (QTWEBENGINE_DISABLE_GPU)
- Forced Fusion Qt theme
- Reset Calibre config directory
- Used Flatpak sandbox isolation
- Added filesystem permissions via override
- Tested safe mode execution
