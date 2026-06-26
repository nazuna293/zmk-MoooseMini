# MoooseMini ZMK Firmware

## Git Rules

- Never push directly to main. Work on feature branches and merge via PR.
- Never force push (--force, --force-with-lease).
- Never delete branches or tags.
- Never use git reset --hard.
- Do not modify workflow files under .github/.
- Do not perform destructive operations (repo deletion, release deletion, etc.).

## Project

- Board: seeeduino_xiao_ble / Shield: MoooseMini rgbled_adapter / Snippet: studio-rpc-usb-uart
- GitHub Actions builds firmware automatically on push or PR.
- Download build artifacts (.uf2) via `gh run download`.
- Editable files: config/MoooseMini.keymap and config/MoooseMini.conf
- Do not modify device definitions under boards/shields/.

## Modules

Managed in config/west.yml. Follow each module's README for configuration.

| Module | Author | Purpose | Revision |
|--------|--------|---------|----------|
| zmk-pmw3610-driver | badjeff | PMW3610 trackball sensor driver | zmk-0.3 |
| zmk-layout-shift | kot149 | JIS layout support (overrides `&kp`) | v1 |
| zmk-scroll-snap | kot149 | Snap scroll direction to nearest axis | v1 |
| zmk-mouse-gesture | kot149 | Convert mouse strokes to key bindings | v1 |
| zmk-listeners | ssbb | Trigger actions on layer/keycode events | v1 |
| zmk-rgbled-widget | caksoylar | RGB LED battery/BT status display | v0.3 |
