# converter3Dto_dat_nc_etcetera

A simple converter for scientific workflows.  
It converts **3D models (.obj)** into various formats used in geoscience and simulation tasks.

## Features

- **OBJ → DAT**  
  Converts `.obj` into a *mask-typed* `.dat` file:  
  - `0` = inside the object  
  - `1` = outside  

- **OBJ → NC (NetCDF)**  
  Two-step workflow:  
  1. Convert `.obj` to `.dat` with `obj2dat`  
  2. Convert `.dat` to self-describing `.nc` (NetCDF format)  

- **OBJ → TOPO**  
  Generates a topographic map: `z`-depth of the model is mapped into topographic height values.  

## Installation

```bash
git clone https://github.com/garlicpunk02/converter3Dto_dat_nc_etcetera.git
cd converter3Dto_dat_nc_etcetera
python setup.py install 
