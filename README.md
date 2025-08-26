# converter3Dto_dat_nc_etcetera

A simple converter for scientific workflows.  
It converts **3D models (.obj)** into various formats used in geoscience and simulation tasks.

## Measures

- If you’re using Blender to create the model, make sure its dimensions are in metric units.
- By default, 1 voxel = 1 meter. You can change this via the vox_size variable in the obj2dat script.
- To prevent meters from being interpreted as geographic degrees, the coordinate origin is set to Moscow; distances in meters are converted to degrees using Moscow’s latitude.

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
