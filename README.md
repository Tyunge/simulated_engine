# Simulated Engine

This simulated engine [starfall](https://github.com/thegrb93/StarfallEx) script provides the building blocks for creating a realistic mobility system for garry's mod. The goal of this project is either to replace the existing mobility portion of [ACF](https://github.com/nrlulz/ACF), or to become it's own standalone mod. 

You can find videos of this script in use at my [YouTube Channel](https://www.youtube.com/@Tyunge).

## Dependencies 
> Requirements for this script to work

- [Starfall](https://github.com/thegrb93/StarfallEx)
- [SProps](https://steamcommunity.com/sharedfiles/filedetails/?id=173482196&searchtext=sprops)
- [WireMod](https://github.com/wiremod/wire)

Place each of these dependencies into your `garrysmod/garrysmod/addons` folder

## Installation
> Installation of this starfall script

Folder location:
- `garrysmod/garrysmod/data/starfall`

If you are downloading this project as a ZIP remember to rename the zip from `simulated_engine-main` to `simulated_engine`

Steps for proper unzipping:
1. Unzip folder into `garrysmod/garrysmod/data/starfall`
2. Verify the Unzipped folder has this structure `simulated_engine-main/simulated_engine-main/...`
3. Rename the **second** `simulated_engine-main` folder to `simulated_engine`
4. Drag `simulated_engine` folder into the root `data/starfall` folder
5. Delete the now empty `simulated_engine-main` folder

The folder contents should appear as such in the in-game starfall directory:

![Screenshot_108](https://user-images.githubusercontent.com/21030699/234411513-42b3a5ef-2c31-4faf-9757-b9d8a26311a4.png)





# How-To...

## Spawn the components
- **ALL** components must be an Advanced Wire Entity Marker
- Engine model must be `models/sprops/cuboids/height12/size_1/cube_12x18x12.mdl`
- Transmission model must be `models/sprops/cuboids/height06/size_1/cube_6x24x6.mdl`
- Transfer Case model must be `models/sprops/cuboids/height06/size_1/cube_6x18x6.mdl`
- Differential  model must be `models/sprops/cuboids/height06/size_1/cube_6x12x6.mdl`

The console command for changing the Advanced Wire Entity Marker is 

`wire_adv_emarker_model MODEL_TO_CHANGE_TO`.

## Link the components
>Link the advanced wire entity markers to each in this order

:warning: Differential orientation is important. Have the differential long ways between the wheels. :warning:
### RWD/FWD systems

`Engine => Transmission => Differential => Wheels`
### AWD systems

`Engine => Transmission => TransferCase => Differentials => Wheels`

## Initialize the starfall script
:warning: Parent **ALL** components directly to your baseplate first :warning:
1. Select the file named `main.txt` and spawn it into the world.
2. Wire both the `POD` input and `Engine` input.
3. Refresh the chip

## Control the script
- `W` is 75% throttle.
- `L.Alt` is 25% throttle.
- `S` is brakes.
- `Mouse1` change gears up
- `Mouse2` change gears down
- `L.Shift` is clutch

# To-Do:
- [ ] Engine Stalling
- [ ] Differential Lock Ratio
- [ ] Transfer Case Power Bias
- [ ] Transaxle 
- [ ] Turbos
- [ ] Supercharger
- [ ] Engine Braking
- [ ] Interpolated Sound Built-In
- [ ] Fuel Tanks
- [ ] Step by Step video guide
