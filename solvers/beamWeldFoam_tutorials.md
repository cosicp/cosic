---
title: beamWeldFoam tutorials
layout: page
nav_order: 2
parent: beamWeldFoam
---

## Tutorial cases
To run any of the tutorials in serial mode:
```
delete any old simulation files, e.g:
$ rm -r 0* 1* 2* 3* 4* 5* 6* 7* 8* 9*
Then:
$ cp -r initial 0
$ blockMesh
$ setFields
$ beamWeldFoam
```
For parallel deployment, using MPI, following the setFields command:
```
$ decomposePar
$ mpirun -np 6 beamWeldFoam -parallel >log &
```
for deployment on 6 cores.

### Gallium Melting Case
A commonly used validation case for heat and mass transfer where melting and solidification is involved, is the simulation of Gallium melting in an enclosed container. In this example the beamWeldFoam solver is used to simulate the melting of the Gallium and the subsequent flow due to buoyancy. as time progresses the hot wall on the left-hand-side of the computational domain causes the Gallium in the local vicinity to melt. As the melt volume increases, buoyancy driven flow begings to dominate as the hot liquid Gallium rises and generates vortical flow structures in the liquid. The predicted melt profiles are in excellent agreement with those reported elsewhere, both numerically and experimentally [1].

### Marangoni Flow (Sen and Davies) Case
Another useful validation case for the solver is one in which a 2D cavity is partially filled such that the interface between the phases is initially flat. A temperature gradient is then developed across the domain. This temperature gradient induces a flow tangential to the interface due to the dependence on temperature of the surface tension, aka Marangoni flow. An analytical steasy-state solution for the free surface deformation exists for this case [2]. excellent agreement between the beamWeldFoam solver and the analytical solution is observed.