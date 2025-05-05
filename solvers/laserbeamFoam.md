---
title: laserBeamFoam
layout: page
nav_order: 2
parent: Solvers
---

# laserBeamFoam

## Description
<style>body {text-align: justify}A volume-of-fluid (VOF) solver for studying high energy density laser-based
advanced manufacturing processes and laser-substrate interactions. This
implementation treats the metallic substrate and shielding gas phase as
in-compressible. The solver fully captures the metallic substrate's
fusion/melting state transition. For the vapourisation of the substrate, the
explicit volumetric dilation due to the vapourisation state transition is
neglected; instead, a phenomenological recoil pressure term is used to capture
the contribution to the momentum and energy fields due to vaporisation events.
laserbeamFoam also captures surface tension effects, the temperature dependence
of surface tension (Marangoni) effects, latent heat effects due to
melting/fusion (and vapourisation), buoyancy effects due to the thermal
expansion of the phases using a Boussinesq approximation, and momentum damping
due to solidification.
A ray-tracing algorithm is implemented that permits the incident Gaussian laser
beam to be discretised into several 'Rays' based on the computational grid
resolution. The 'Rays' of this incident laser beam are then tracked through the
domain through their multiple reflections, with the energy deposited by each
ray determined through the Fresnel equations. The solver approach is extended
from the adiabatic two-phase interFoam code developed by
[OpenCFD Ltd.](http://openfoam.com/) to include non-isothermal state transition
physics and ray-tracing heat source application.</style>

<p>
A volume-of-fluid (VOF) solver for studying high energy density laser-based
advanced manufacturing processes and laser-substrate interactions. This
implementation treats the metallic substrate and shielding gas phase as
in-compressible. The solver fully captures the metallic substrate's
fusion/melting state transition. For the vapourisation of the substrate, the
explicit volumetric dilation due to the vapourisation state transition is
neglected; instead, a phenomenological recoil pressure term is used to capture
the contribution to the momentum and energy fields due to vaporisation events.
laserbeamFoam also captures surface tension effects, the temperature dependence
of surface tension (Marangoni) effects, latent heat effects due to
melting/fusion (and vapourisation), buoyancy effects due to the thermal
expansion of the phases using a Boussinesq approximation, and momentum damping
due to solidification.
A ray-tracing algorithm is implemented that permits the incident Gaussian laser
beam to be discretised into several 'Rays' based on the computational grid
resolution. The 'Rays' of this incident laser beam are then tracked through the
domain through their multiple reflections, with the energy deposited by each
ray determined through the Fresnel equations. The solver approach is extended
from the adiabatic two-phase interFoam code developed by
[OpenCFD Ltd.](http://openfoam.com/) to include non-isothermal state transition
physics and ray-tracing heat source application. </p>

$$ 
\frac{\partial \omega}{\partial x}
$$