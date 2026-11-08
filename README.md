# legacy-c-inventory-fortran

Demo legacy system for [REPLIC8](https://github.com/jaiom-rola-sp/REPLIC8): the old inventory and shipping software of "Subsidiary C", an industrial logistics and manufacturing company. Written in Fortran 90 (gfortran). All data is made up.

- `src/inventory.f90`: the program. `data/stock.dat` and `data/lanes.dat`: fixed-width data.
- Read-only operations: `check_stock`, `get_shipping_options`.
- Line protocol: the first stdin line is the command, then `KEY=VALUE` lines, then `END`. Output is `KEY=VALUE` lines; `BEGIN-ITEMS` starts a list and `--` closes each item.
- Shared keys with the maintenance system: part ID (for example `PMP-2210`) and site region (for example `PERMIAN`).
