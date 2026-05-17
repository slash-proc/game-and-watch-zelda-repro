# Zelda Game & Watch (2021) Reproduction Board

An open-source hardware attempt to reproduce and clone the PCB layout of the **Nintendo Game & Watch: The Legend of Zelda (2021 Edition)**. 

The goal of this project is to create a drop-in hardware reproduction that honors the mechanical constraints, component alignment, and routing logic of the original handheld, utilizing modern EDA workflows.

## Project Structure

This project is fully self-contained and structured for **KiCad 10.0+**. All non-standard footprints, 3D models, and schematic symbols are bundled locally to ensure environment portability.

```text
.
├── fp-lib-table        # Footprint library mapping table
├── sym-lib-table       # Symbol library mapping table
├── libs/               # Unified local project asset directory
│   ├── gnw.kicad_sym   # Custom schematic symbols (MCU, connectors, etc.)
│   ├── gnw.pretty/     # Custom physical footprint components
│   └── gnw.3dshapes/   # Component 3D assets (.step/.wrl)
├── subsheets/          # Modular schematic hierarchy
│   ├── audio.kicad_sch
│   ├── buttons.kicad_sch
│   ├── lcd.kicad_sch
│   ├── mcu.kicad_sch
│   ├── power.kicad_sch
│   └── spi_flash.kicad_sch
├── zelda-gnw-repro.kicad_pcb  # Main PCB routing layout
├── zelda-gnw-repro.kicad_sch  # Top-level master schematic
└── zelda-gnw-repro.kicad_pro  # KiCad project configuration
