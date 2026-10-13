# Awesome Open-Source Solvers

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[日本語版はこちら / Japanese](README.ja.md)

Curated open-source **solvers** and scientific-computing stacks — FEM, BEM, CFD, multibody/dynamics, particle methods, acoustics, electronic circuits/EM, combustion, weather/climate, quantum — plus linear algebra and mesh adjuncts. Prefer well-known, durable projects with official docs or GitHub homes. Overlap with CAD/CAE lists is fine; this list focuses on **solvers**, not CAD apps. ⭐ badges show live GitHub star counts (via shields.io).

## Contents

- [Finite Element (FEM)](#finite-element-fem)
- [Boundary Element (BEM)](#boundary-element-bem)
- [CFD](#cfd)
- [Multibody / structural dynamics](#multibody--structural-dynamics)
- [Particle methods (MD / DEM / SPH / PIC)](#particle-methods-md--dem--sph--pic)
- [Acoustics / vibroacoustics](#acoustics--vibroacoustics)
- [Electronic circuits / electromagnetics](#electronic-circuits--electromagnetics)
- [Combustion / reacting flows](#combustion--reacting-flows)
- [Weather / climate](#weather--climate)
- [Quantum / electronic structure / quantum dynamics](#quantum--electronic-structure--quantum-dynamics)
- [Linear algebra & parallel solvers](#linear-algebra--parallel-solvers)
- [Mesh / pre-post (brief)](#mesh--pre-post-brief)
- [Related lists](#related-lists)
- [Contributing](#contributing)
- [shvyac's awesome lists](#shvyacs-awesome-lists)

---

## Finite Element (FEM)

Libraries and industrial/research FEM codes for structural, thermal, and multiphysics PDEs.

### deal.II
C++ FEM library for adaptive, parallel, and matrix-free discretizations — from laptops to HPC. Strong tutorials and community.

- https://dealii.org/
- https://github.com/dealii/dealii ![GitHub stars](https://img.shields.io/github/stars/dealii/dealii?style=flat&label=%E2%AD%90)

### FEniCS / DOLFINx
Python-first FEM platform for rapid variational formulations and coupled PDEs (FEniCSx / DOLFINx).

- https://fenicsproject.org/
- https://github.com/FEniCS

### MFEM
Lightweight, scalable C++ FEM toolbox for high-order methods, GPU/HPC, and research discretizations (Galerkin, DG, mixed, DPG).

- https://mfem.org/
- https://github.com/mfem/mfem ![GitHub stars](https://img.shields.io/github/stars/mfem/mfem?style=flat&label=%E2%AD%90)

### CalculiX
Abaqus-like open-source 3D structural FEM (ccx solver + cgx). Widely used with FreeCAD FEM and PrePoMax GUIs.

- https://www.dhondt.de/
- https://github.com/Dhondtguido/CalculiX ![GitHub stars](https://img.shields.io/github/stars/Dhondtguido/CalculiX?style=flat&label=%E2%AD%90)
- https://github.com/calculix

### Code_Aster
EDF’s industrial structural mechanics / multiphysics FEM suite; often paired with SALOME-Meca for pre/post.

- https://code-aster.org/
- https://gitlab.com/codeaster

### Elmer
Open multiphysics FEM (fluid, solid, EM, heat, and coupled problems) with GUI and parallel solvers.

- https://www.elmerfem.org/
- https://github.com/ElmerCSC/elmerfem ![GitHub stars](https://img.shields.io/github/stars/ElmerCSC/elmerfem?style=flat&label=%E2%AD%90)

### FreeFEM / SfePy / Firedrake / scikit-fem
PDE/FEM platforms with DSL or Python interfaces for custom physics and research.

- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources ![GitHub stars](https://img.shields.io/github/stars/FreeFem/FreeFem-sources?style=flat&label=%E2%AD%90)
- https://sfepy.org/ — https://github.com/sfepy/sfepy ![GitHub stars](https://img.shields.io/github/stars/sfepy/sfepy?style=flat&label=%E2%AD%90)
- https://www.firedrakeproject.org/ — https://github.com/firedrakeproject/firedrake ![GitHub stars](https://img.shields.io/github/stars/firedrakeproject/firedrake?style=flat&label=%E2%AD%90)
- https://scikit-fem.readthedocs.io/ — https://github.com/kinnala/scikit-fem ![GitHub stars](https://img.shields.io/github/stars/kinnala/scikit-fem?style=flat&label=%E2%AD%90)

### MOOSE / libMesh / GetDP
Multiphysics Object-Oriented Simulation Environment (built on libMesh); GetDP for coupled FEM (often with Gmsh/ONELAB).

- https://mooseframework.inl.gov/ — https://github.com/idaholab/moose ![GitHub stars](https://img.shields.io/github/stars/idaholab/moose?style=flat&label=%E2%AD%90)
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh ![GitHub stars](https://img.shields.io/github/stars/libMesh/libmesh?style=flat&label=%E2%AD%90)
- https://getdp.info/ — https://gitlab.onelab.info/getdp/getdp

### FrontISTR / MYSTRAN / FEBio / NGSolve
Large-scale nonlinear structures (FrontISTR); Nastran-like analysis (MYSTRAN); biomechanics nonlinear FEM (FEBio); Netgen + NGSolve FEM platform.

- https://www.frontistr.com/ — https://gitlab.com/FrontISTR-Commons/FrontISTR (main development; GitHub is a mirror)
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN ![GitHub stars](https://img.shields.io/github/stars/dr-bill-c/MYSTRAN?style=flat&label=%E2%AD%90)
- https://febio.org/ — https://github.com/febiosoftware/FEBio ![GitHub stars](https://img.shields.io/github/stars/febiosoftware/FEBio?style=flat&label=%E2%AD%90)
- https://ngsolve.org/ — https://github.com/NGSolve/ngsolve ![GitHub stars](https://img.shields.io/github/stars/NGSolve/ngsolve?style=flat&label=%E2%AD%90)

### Kratos Multiphysics
BSD-licensed C++/Python framework for parallel multi-disciplinary simulation — structures, fluids, DEM, FSI, and optimization applications.

- https://kratosmultiphysics.github.io/Kratos/
- https://github.com/KratosMultiphysics/Kratos ![GitHub stars](https://img.shields.io/github/stars/KratosMultiphysics/Kratos?style=flat&label=%E2%AD%90)

### OpenCourant (formerly OpenRadioss)
Explicit dynamics FEM solver for crash, impact, drop and blast simulation (AGPL-3.0). Siemens retired OpenRadioss and deleted its GitHub repository in Oct 2026 (now Simcenter Radioss / Radioss R&D program); OpenCourant is the community fork with full commit history, hosted under the Rocky Enterprise Software Foundation (RESF).

- https://opencourant.org/
- https://github.com/OpenCourant/OpenCourant ![GitHub stars](https://img.shields.io/github/stars/OpenCourant/OpenCourant?style=flat&label=%E2%AD%90)

---

## Boundary Element (BEM)

Surface-integral solvers for acoustics, electromagnetics, and exterior problems.

### Bempp
Python BEM platform for electrostatics, acoustics, and electromagnetics; Gmsh/VTK I/O and optional FEniCS FEM–BEM coupling.

- https://bempp.com/
- https://github.com/bempp

### scuff-em
BEM suite for electromagnetic scattering, Casimir/radiative heat transfer, and nanophotonics (EFIE / PMCHWT, RWG bases).

- https://github.com/HomerReid/scuff-em ![GitHub stars](https://img.shields.io/github/stars/HomerReid/scuff-em?style=flat&label=%E2%AD%90)
- http://homerreid.github.io/scuff-em-documentation/

### OpenBEM
MATLAB Helmholtz / acoustic BEM codes for 2D and 3D geometries.

- https://openbem.dk/

---

## CFD

Finite-volume, finite-element, and lattice-Boltzmann fluid solvers.

### OpenFOAM
Most widely used open-source CFD toolbox — incompressible/compressible flow, heat transfer, multiphase, reactions; large ecosystem. Latest OpenCFD release is v2606 (June 2026); its repositories moved to gitlab.com/openfoam in Nov 2025.

- https://www.openfoam.com/ — https://gitlab.com/openfoam
- https://openfoam.org/
- https://github.com/OpenFOAM/OpenFOAM-dev ![GitHub stars](https://img.shields.io/github/stars/OpenFOAM/OpenFOAM-dev?style=flat&label=%E2%AD%90)

### SU2
Multiphysics PDE solver with gradient-based aerodynamic shape optimization and adjoint capabilities.

- https://su2code.github.io/
- https://github.com/su2code/SU2 ![GitHub stars](https://img.shields.io/github/stars/su2code/SU2?style=flat&label=%E2%AD%90)

### Nektar++ / Lethe
Spectral/hp element CFD (Nektar++); high-order CG CFD–DEM (Lethe).

- https://www.nektar.info/ — https://gitlab.nektar.info/nektar/nektar
- https://chaos-polymtl.github.io/lethe/ — https://github.com/chaos-polymtl/lethe ![GitHub stars](https://img.shields.io/github/stars/chaos-polymtl/lethe?style=flat&label=%E2%AD%90)

### PyFR
Python framework for high-order flux reconstruction CFD on unstructured grids — compressible / incompressible Navier–Stokes with GPU backends (CUDA, HIP, OpenCL, Metal) and OpenMP; latest v3.x.

- https://www.pyfr.org/
- https://github.com/PyFR/PyFR ![GitHub stars](https://img.shields.io/github/stars/PyFR/PyFR?style=flat&label=%E2%AD%90)

### Palabos / waLBerla / OpenLB
Lattice Boltzmann Method (LBM) CFD frameworks for complex flows and HPC.

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://www.walberla.net/ — https://github.com/lssfau/walberla ![GitHub stars](https://img.shields.io/github/stars/lssfau/walberla?style=flat&label=%E2%AD%90) (mirror of the official FAU GitLab)
- https://www.openlb.net/ — https://gitlab.com/openlb/release

### Fire Dynamics Simulator (FDS)
NIST fire-driven flow CFD with Smokeview visualization.

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds ![GitHub stars](https://img.shields.io/github/stars/firemodels/fds?style=flat&label=%E2%AD%90)

### Code_Saturne / Nek5000 / nekRS
EDF industrial CFD (Code_Saturne); spectral-element CFD (Nek5000 / nekRS).

- https://www.code-saturne.org/
- https://nek5000.mcs.anl.gov/ — https://github.com/Nek5000/Nek5000 ![GitHub stars](https://img.shields.io/github/stars/Nek5000/Nek5000?style=flat&label=%E2%AD%90)
- https://github.com/Nek5000/nekRS ![GitHub stars](https://img.shields.io/github/stars/Nek5000/nekRS?style=flat&label=%E2%AD%90)

### JAX-Fluids / XLB
GPU-accelerated, differentiable CFD in Python for physics-based ML — compressible/multiphase finite-volume (JAX-Fluids) and lattice Boltzmann on JAX / NVIDIA Warp (XLB).

- https://github.com/tumaer/JAXFLUIDS ![GitHub stars](https://img.shields.io/github/stars/tumaer/JAXFLUIDS?style=flat&label=%E2%AD%90)
- https://github.com/Autodesk/XLB ![GitHub stars](https://img.shields.io/github/stars/Autodesk/XLB?style=flat&label=%E2%AD%90)

---

## Multibody / structural dynamics

Rigid and flexible multibody dynamics, mechanisms, and vehicle/robot simulation.

### Project Chrono
Multiphysics multibody platform — vehicles, robots, granular/DEM contact, FEA co-simulation.

- https://projectchrono.org/
- https://github.com/projectchrono/chrono ![GitHub stars](https://img.shields.io/github/stars/projectchrono/chrono?style=flat&label=%E2%AD%90)

### MBDyn / Simbody / EXUDYN
General-purpose MBD (MBDyn); articulated biomechanics/robotics (Simbody); Python/C++ flexible multibody (EXUDYN).

- https://www.mbdyn.org/ — https://public.gitlab.polimi.it/DAER/mbdyn
- https://github.com/simbody/simbody ![GitHub stars](https://img.shields.io/github/stars/simbody/simbody?style=flat&label=%E2%AD%90)
- https://github.com/jgerstmayr/EXUDYN ![GitHub stars](https://img.shields.io/github/stars/jgerstmayr/EXUDYN?style=flat&label=%E2%AD%90)

### OpenSim / Pinocchio / Drake
Musculoskeletal dynamics (OpenSim); fast rigid-body dynamics for robotics (Pinocchio); robotics & control toolbox with dynamics (Drake).

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio ![GitHub stars](https://img.shields.io/github/stars/stack-of-tasks/pinocchio?style=flat&label=%E2%AD%90)
- https://drake.mit.edu/ — https://github.com/RobotLocomotion/drake ![GitHub stars](https://img.shields.io/github/stars/RobotLocomotion/drake?style=flat&label=%E2%AD%90)

### MuJoCo
Google DeepMind's Multi-Joint dynamics with Contact — fast, accurate rigid-body / contact physics engine for robotics, biomechanics, and RL (Apache-2.0; GPU/JAX via MJX and MuJoCo Warp).

- https://mujoco.org/
- https://github.com/google-deepmind/mujoco ![GitHub stars](https://img.shields.io/github/stars/google-deepmind/mujoco?style=flat&label=%E2%AD%90)

### OpenFAST
NLR (formerly NREL) aero-servo-elastic wind turbine dynamics (coupled CFD/structural loads workflows).

- https://openfast.readthedocs.io/
- https://github.com/OpenFAST/openfast ![GitHub stars](https://img.shields.io/github/stars/OpenFAST/openfast?style=flat&label=%E2%AD%90)

---

## Particle methods (MD / DEM / SPH / PIC)

Molecular dynamics, discrete element, smoothed particle hydrodynamics, and particle-in-cell codes.

### LAMMPS
Large-scale Atomic/Molecular Massively Parallel Simulator — materials MD, coarse-grained and mesoscale particle models.

- https://www.lammps.org/
- https://github.com/lammps/lammps ![GitHub stars](https://img.shields.io/github/stars/lammps/lammps?style=flat&label=%E2%AD%90)

### GROMACS
High-performance molecular dynamics for biomolecules and soft matter; strong GPU support.

- https://www.gromacs.org/
- https://github.com/gromacs/gromacs ![GitHub stars](https://img.shields.io/github/stars/gromacs/gromacs?style=flat&label=%E2%AD%90)

### DualSPHysics / SPHERA / PySPH
SPH free-surface / coastal / industrial flows (DualSPHysics); engineering SPH (SPHERA); Python SPH framework (PySPH).

- https://dual.sphysics.org/ — https://github.com/DualSPHysics/DualSPHysics ![GitHub stars](https://img.shields.io/github/stars/DualSPHysics/DualSPHysics?style=flat&label=%E2%AD%90)
- https://github.com/GiordanoAgateRSE/SPHERA ![GitHub stars](https://img.shields.io/github/stars/GiordanoAgateRSE/SPHERA?style=flat&label=%E2%AD%90)
- https://pysph.readthedocs.io/ — https://github.com/pypr/pysph ![GitHub stars](https://img.shields.io/github/stars/pypr/pysph?style=flat&label=%E2%AD%90)

### LIGGGHTS / Yade / MercuryDPM
DEM for granular materials and industrial particle processes.

- https://www.cfdem.com/liggghtsr-open-source-discrete-element-method-particle-simulation-code — https://github.com/CFDEMproject/LIGGGHTS-PUBLIC ![GitHub stars](https://img.shields.io/github/stars/CFDEMproject/LIGGGHTS-PUBLIC?style=flat&label=%E2%AD%90) (commercial successor: Aspherix)
- https://yade-dem.org/ — https://gitlab.com/yade-dev/trunk
- https://www.mercurydpm.org/ — https://bitbucket.org/mercurydpm/mercurydpm

### WarpX / PIConGPU / Smilei
Exascale electromagnetic PIC (WarpX); GPU PIC (PIConGPU); plasma PIC (Smilei).

- https://warpx.readthedocs.io/ — https://github.com/BLAST-WarpX/warpx ![GitHub stars](https://img.shields.io/github/stars/BLAST-WarpX/warpx?style=flat&label=%E2%AD%90)
- https://picongpu.readthedocs.io/ — https://github.com/ComputationalRadiationPhysics/picongpu ![GitHub stars](https://img.shields.io/github/stars/ComputationalRadiationPhysics/picongpu?style=flat&label=%E2%AD%90)
- https://smileipic.github.io/Smilei/ — https://github.com/SmileiPIC/Smilei ![GitHub stars](https://img.shields.io/github/stars/SmileiPIC/Smilei?style=flat&label=%E2%AD%90)

### HOOMD-blue / OpenMM
GPU-accelerated MD for soft matter (HOOMD-blue); high-performance biomolecular MD toolkit (OpenMM).

- https://glotzerlab.engin.umich.edu/hoomd-blue/ — https://github.com/glotzerlab/hoomd-blue ![GitHub stars](https://img.shields.io/github/stars/glotzerlab/hoomd-blue?style=flat&label=%E2%AD%90)
- https://openmm.org/ — https://github.com/openmm/openmm ![GitHub stars](https://img.shields.io/github/stars/openmm/openmm?style=flat&label=%E2%AD%90)

---

## Acoustics / vibroacoustics

Wave propagation, room/outdoor acoustics, and coupled vibroacoustic solvers.

### FEM vibroacoustics (Code_Aster / Elmer / CalculiX)
Structural–acoustic coupling via industrial FEM suites (see FEM section).

- https://code-aster.org/
- https://www.elmerfem.org/
- https://www.dhondt.de/

### Acoustic BEM (Bempp / OpenBEM / scuff-em)
Exterior and interior Helmholtz / EM–acoustic boundary-element solvers (see BEM section).

- https://bempp.com/
- https://openbem.dk/
- http://homerreid.github.io/scuff-em-documentation/

### k-Wave
MATLAB/C++ toolbox for time-domain acoustic and ultrasound wavefields. v1.4.x is the last full k-Wave-I release; its successor k-Wave-II is developed in a separate repository. Python interface via k-wave-python.

- http://www.k-wave.org/
- https://github.com/ucl-bug/k-wave ![GitHub stars](https://img.shields.io/github/stars/ucl-bug/k-wave?style=flat&label=%E2%AD%90)
- https://github.com/ucl-bug/k-wave-ii ![GitHub stars](https://img.shields.io/github/stars/ucl-bug/k-wave-ii?style=flat&label=%E2%AD%90)
- https://github.com/waltsims/k-wave-python ![GitHub stars](https://img.shields.io/github/stars/waltsims/k-wave-python?style=flat&label=%E2%AD%90)

### GetDP / ONELAB acoustics
Coupled FEM acoustics and multiphysics via GetDP + Gmsh/ONELAB workflows.

- https://getdp.info/
- https://onelab.info/

---

## Electronic circuits / electromagnetics

Circuit (SPICE) simulators and electromagnetic field solvers. See also Elmer / GetDP (FEM electromagnetics) and scuff-em (BEM). Freeware but closed-source tools such as LTspice and QSPICE are out of scope.

### ngspice
Open-source mixed-signal SPICE simulator (successor of Berkeley SPICE3f5); built into KiCad and used as a backend by Qucs-S and PySpice.

- https://ngspice.sourceforge.io/ — https://sourceforge.net/p/ngspice/ngspice/

### Xyce
Sandia's massively parallel, SPICE-compatible circuit simulator for large analog circuits (GPL v3).

- https://xyce.sandia.gov/ — https://github.com/Xyce/Xyce ![GitHub stars](https://img.shields.io/github/stars/Xyce/Xyce?style=flat&label=%E2%AD%90)

### Qucs-S / PySpice
GUI schematic capture and simulation front end driving ngspice, Xyce, or QucsatorRF (Qucs-S); Python interface to ngspice / Xyce for scripted circuit analysis (PySpice; docs site not updated since 2021).

- https://ra3xdh.github.io/ — https://github.com/ra3xdh/qucs_s ![GitHub stars](https://img.shields.io/github/stars/ra3xdh/qucs_s?style=flat&label=%E2%AD%90)
- https://pyspice.fabrice-salvaire.fr/ — https://github.com/PySpice-org/PySpice ![GitHub stars](https://img.shields.io/github/stars/PySpice-org/PySpice?style=flat&label=%E2%AD%90)

### openEMS / Meep
FDTD electromagnetic field solvers — antennas and PCB/RF structures with MATLAB/Octave/Python interfaces (openEMS); nanophotonics and general EM with Python scripting (Meep, MIT).

- https://www.openems.de/ — https://github.com/thliebig/openEMS-Project ![GitHub stars](https://img.shields.io/github/stars/thliebig/openEMS-Project?style=flat&label=%E2%AD%90)
- https://meep.readthedocs.io/ — https://github.com/NanoComp/meep ![GitHub stars](https://img.shields.io/github/stars/NanoComp/meep?style=flat&label=%E2%AD%90)

### Palace
AWS 3D finite-element solver for computational electromagnetics (eigenmodes, frequency/time domain, electrostatics, magnetostatics), used e.g. for superconducting quantum circuits; built on MFEM.

- https://awslabs.github.io/palace/stable/ — https://github.com/awslabs/palace ![GitHub stars](https://img.shields.io/github/stars/awslabs/palace?style=flat&label=%E2%AD%90)

---

## Combustion / reacting flows

Chemical kinetics, reacting CFD, and fire/combustion packages.

### Cantera
Chemical kinetics, thermodynamics, and transport library — mechanisms, 0D/1D reactors, and CFD coupling.

- https://cantera.org/
- https://github.com/Cantera/cantera ![GitHub stars](https://img.shields.io/github/stars/Cantera/cantera?style=flat&label=%E2%AD%90)

### OpenFOAM reacting / combustion solvers
Built-in reacting / chemistry / combustion packages on the OpenFOAM toolboxes.

- https://www.openfoam.com/documentation/overview
- https://openfoam.org/

### Fire Dynamics Simulator (FDS)
Fire-driven reacting buoyancy flows (see also CFD).

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds ![GitHub stars](https://img.shields.io/github/stars/firemodels/fds?style=flat&label=%E2%AD%90)

### PeleC / PeleLMeX / PelePhysics
AMReX-based compressible and low-Mach reacting flow solvers (DOE Exascale combustion stack, now published as the Pele Suite).

- https://pele-suite.github.io/
- https://github.com/Pele-Suite

### CoolProp
Open-source thermodynamic and transport properties (useful adjunct for reacting-flow workflows).

- https://coolprop.org/
- https://github.com/CoolProp/CoolProp ![GitHub stars](https://img.shields.io/github/stars/CoolProp/CoolProp?style=flat&label=%E2%AD%90)

---

## Weather / climate

Numerical weather prediction (NWP), Earth-system / climate models, and machine-learning weather forecasting. Check each model's license for trained weights before use.

### WRF / MPAS
Weather Research and Forecasting model — the most widely used open limited-area NWP model (NCAR); MPAS-Atmosphere, unstructured Voronoi-mesh global-to-regional model (NCAR / LANL).

- https://www.mmm.ucar.edu/models/wrf — https://github.com/wrf-model/WRF ![GitHub stars](https://img.shields.io/github/stars/wrf-model/WRF?style=flat&label=%E2%AD%90)
- https://mpas-dev.github.io/ — https://github.com/MPAS-Dev/MPAS-Model ![GitHub stars](https://img.shields.io/github/stars/MPAS-Dev/MPAS-Model?style=flat&label=%E2%AD%90)

### UFS Weather Model
NOAA Unified Forecast System built on the FV3 dynamical core — the community model behind the operational GFS.

- https://ufs.epic.noaa.gov/
- https://github.com/ufs-community/ufs-weather-model ![GitHub stars](https://img.shields.io/github/stars/ufs-community/ufs-weather-model?style=flat&label=%E2%AD%90)

### ICON
Icosahedral nonhydrostatic weather and climate model of DWD / MPI-M; open source under BSD-3-Clause since 2024.

- https://www.icon-model.org/
- https://gitlab.dkrz.de/icon/icon-model

### CESM / E3SM
Coupled Earth-system models for climate simulation — atmosphere, ocean, land, sea ice (CESM by NCAR; E3SM by US DOE).

- https://www.cesm.ucar.edu/ — https://github.com/ESCOMP/CESM ![GitHub stars](https://img.shields.io/github/stars/ESCOMP/CESM?style=flat&label=%E2%AD%90)
- https://e3sm.org/ — https://github.com/E3SM-Project/E3SM ![GitHub stars](https://img.shields.io/github/stars/E3SM-Project/E3SM?style=flat&label=%E2%AD%90)

### Anemoi / AIFS
ECMWF framework for training and running ML weather models (datasets, graphs, models, training, inference); ECMWF's operational AI forecast AIFS is built on it (weights CC BY 4.0).

- https://anemoi.readthedocs.io/ — https://github.com/ecmwf/anemoi-core ![GitHub stars](https://img.shields.io/github/stars/ecmwf/anemoi-core?style=flat&label=%E2%AD%90)
- https://huggingface.co/ecmwf/aifs-single-1.1

### GraphCast / GenCast / NeuralGCM
Google DeepMind ML medium-range forecasting — deterministic GraphCast and ensemble GenCast (repo renamed from graphcast to weathernext); NeuralGCM, a hybrid differentiable dynamical core + ML atmosphere model.

- https://github.com/google-deepmind/weathernext ![GitHub stars](https://img.shields.io/github/stars/google-deepmind/weathernext?style=flat&label=%E2%AD%90)
- https://neuralgcm.readthedocs.io/ — https://github.com/neuralgcm/neuralgcm ![GitHub stars](https://img.shields.io/github/stars/neuralgcm/neuralgcm?style=flat&label=%E2%AD%90)

### Earth2Studio / Aurora / Pangu-Weather
NVIDIA framework for running AI weather/climate models (FourCastNet and others); Microsoft Aurora Earth-system foundation model; Huawei Pangu-Weather 3D transformer forecaster.

- https://nvidia.github.io/earth2studio/ — https://github.com/NVIDIA/earth2studio ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/earth2studio?style=flat&label=%E2%AD%90)
- https://microsoft.github.io/aurora/ — https://github.com/microsoft/aurora ![GitHub stars](https://img.shields.io/github/stars/microsoft/aurora?style=flat&label=%E2%AD%90)
- https://github.com/198808xc/Pangu-Weather ![GitHub stars](https://img.shields.io/github/stars/198808xc/Pangu-Weather?style=flat&label=%E2%AD%90)

---

## Quantum / electronic structure / quantum dynamics

DFT, many-body electronic structure, and open quantum systems.

### Quantum ESPRESSO
Plane-wave DFT / electronic-structure suite for materials and molecules; large user community.

- https://www.quantum-espresso.org/
- https://gitlab.com/QEF/q-e

### ABINIT / CP2K / SIESTA / GPAW
Plane-wave and localized-orbital DFT codes for solids, chemistry, and nanosystems.

- https://www.abinit.org/ — https://github.com/abinit/abinit ![GitHub stars](https://img.shields.io/github/stars/abinit/abinit?style=flat&label=%E2%AD%90)
- https://www.cp2k.org/ — https://github.com/cp2k/cp2k ![GitHub stars](https://img.shields.io/github/stars/cp2k/cp2k?style=flat&label=%E2%AD%90)
- https://gitlab.com/siesta-project/siesta
- https://gpaw.readthedocs.io/ — https://gitlab.com/gpaw/gpaw

### QuTiP
Quantum Toolbox in Python — open quantum systems, master equations, and quantum optics dynamics.

- https://qutip.org/
- https://github.com/qutip/qutip ![GitHub stars](https://img.shields.io/github/stars/qutip/qutip?style=flat&label=%E2%AD%90)

### NWChem / Psi4 / PySCF
Computational chemistry suites (NWChem); quantum chemistry (Psi4); Python quantum chemistry (PySCF).

- https://nwchemgit.github.io/ — https://github.com/nwchemgit/nwchem ![GitHub stars](https://img.shields.io/github/stars/nwchemgit/nwchem?style=flat&label=%E2%AD%90)
- https://psicode.org/ — https://github.com/psi4/psi4 ![GitHub stars](https://img.shields.io/github/stars/psi4/psi4?style=flat&label=%E2%AD%90)
- https://pyscf.org/ — https://github.com/pyscf/pyscf ![GitHub stars](https://img.shields.io/github/stars/pyscf/pyscf?style=flat&label=%E2%AD%90)

### Yambo / BerkeleyGW / Octopus
Many-body perturbation theory / GW-BSE (Yambo, BerkeleyGW); real-space TDDFT (Octopus).

- https://www.yambo-code.eu/ — https://github.com/yambo-code/yambo ![GitHub stars](https://img.shields.io/github/stars/yambo-code/yambo?style=flat&label=%E2%AD%90)
- https://berkeleygw.org/ — https://berkeleygw.org/download/ (source tarballs; the former BGW-public GitHub repo is gone)
- https://octopus-code.org/ — https://gitlab.com/octopus-code/octopus

---

## Linear algebra & parallel solvers

Sparse iterative/direct solvers and HPC numerical libraries that underpin many of the codes above.

### PETSc (+ TAO)
Portable Extensible Toolkit for Scientific Computation — Krylov solvers, preconditioners, nonlinear/time steppers, and TAO optimization; C/Fortran/Python (petsc4py).

- https://petsc.org/
- https://gitlab.com/petsc/petsc
- https://github.com/petsc/petsc ![GitHub stars](https://img.shields.io/github/stars/petsc/petsc?style=flat&label=%E2%AD%90)

### Trilinos
Package ecosystem for HPC linear algebra, solvers, discretizations, and multiphysics (Belos, Ifpack2, MueLu, Tpetra, …).

- https://trilinos.github.io/
- https://github.com/trilinos/Trilinos ![GitHub stars](https://img.shields.io/github/stars/trilinos/Trilinos?style=flat&label=%E2%AD%90)

### hypre
High-performance parallel multigrid preconditioners and solvers for large sparse systems (BoomerAMG, etc.).

- https://computing.llnl.gov/projects/hypre-scalable-linear-solvers-multigrid-methods
- https://github.com/hypre-space/hypre ![GitHub stars](https://img.shields.io/github/stars/hypre-space/hypre?style=flat&label=%E2%AD%90)

### AMGX / Ginkgo
GPU-accelerated sparse iterative solvers — NVIDIA's distributed algebraic multigrid and Krylov library (AMGX); portable C++ sparse linear algebra with CUDA / HIP / SYCL / OpenMP backends (Ginkgo).

- https://github.com/NVIDIA/AMGX ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/AMGX?style=flat&label=%E2%AD%90)
- https://gko-project.org/ — https://github.com/ginkgo-project/ginkgo ![GitHub stars](https://img.shields.io/github/stars/ginkgo-project/ginkgo?style=flat&label=%E2%AD%90)

### SuperLU / MUMPS / SuiteSparse
Sparse direct solvers — SuperLU / SuperLU_DIST; MUMPS multifrontal; SuiteSparse (UMFPACK, CHOLMOD, SPQR, …).

- https://portal.nersc.gov/project/sparse/superlu/ — https://github.com/xiaoyeli/superlu ![GitHub stars](https://img.shields.io/github/stars/xiaoyeli/superlu?style=flat&label=%E2%AD%90)
- https://mumps-solver.org/
- https://people.engr.tamu.edu/davis/suitesparse.html — https://github.com/DrTimothyAldenDavis/SuiteSparse ![GitHub stars](https://img.shields.io/github/stars/DrTimothyAldenDavis/SuiteSparse?style=flat&label=%E2%AD%90)

### Eigen / OpenBLAS
Dense linear algebra building blocks used inside many solvers.

- https://libeigen.gitlab.io/ — https://gitlab.com/libeigen/eigen
- https://openmathlib.org/OpenBLAS/ — https://github.com/OpenMathLib/OpenBLAS ![GitHub stars](https://img.shields.io/github/stars/OpenMathLib/OpenBLAS?style=flat&label=%E2%AD%90)

### Dakota
Sandia toolkit for optimization, UQ, and model calibration wrapped around simulation codes.

- https://dakota.sandia.gov/
- https://github.com/snl-dakota/dakota ![GitHub stars](https://img.shields.io/github/stars/snl-dakota/dakota?style=flat&label=%E2%AD%90)

### preCICE
Coupling library for partitioned multiphysics (FSI, conjugate heat transfer) with ready adapters for OpenFOAM, CalculiX, Code_Aster, deal.II, FEniCS, SU2, and more.

- https://precice.org/
- https://github.com/precice/precice ![GitHub stars](https://img.shields.io/github/stars/precice/precice?style=flat&label=%E2%AD%90)

---

## Mesh / pre-post (brief)

Geometry meshing and visualization typically paired with the solvers above (not a full CAD list).

### Gmsh
Open-source 3D FE mesh generator with CAD kernel options, `.geo` scripting, and post-processing.

- https://gmsh.info/
- https://gitlab.onelab.info/gmsh/gmsh

### Netgen / SALOME / meshio
Tetrahedral meshing (Netgen); CAD/mesh pre-post platform (SALOME); mesh format I/O in Python (meshio).

- https://ngsolve.org/ — https://github.com/NGSolve/netgen ![GitHub stars](https://img.shields.io/github/stars/NGSolve/netgen?style=flat&label=%E2%AD%90)
- https://www.salome-platform.org/
- https://github.com/nschloe/meshio ![GitHub stars](https://img.shields.io/github/stars/nschloe/meshio?style=flat&label=%E2%AD%90)

### ParaView / VTK / VisIt
Scientific visualization for CFD/FEM results (ParaView, VTK); VisIt for large parallel datasets.

- https://www.paraview.org/ — https://github.com/Kitware/ParaView ![GitHub stars](https://img.shields.io/github/stars/Kitware/ParaView?style=flat&label=%E2%AD%90)
- https://vtk.org/ — https://github.com/Kitware/VTK ![GitHub stars](https://img.shields.io/github/stars/Kitware/VTK?style=flat&label=%E2%AD%90)
- https://visit-dav.github.io/visit-website/ — https://github.com/visit-dav/visit ![GitHub stars](https://img.shields.io/github/stars/visit-dav/visit?style=flat&label=%E2%AD%90)

---

## Related lists

- https://github.com/shvyac/awesome-cad-cae ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90) — CAD / CAE / EDA / formats (broader toolchain)
- https://github.com/mlightcad/awesome-cad ![GitHub stars](https://img.shields.io/github/stars/mlightcad/awesome-cad?style=flat&label=%E2%AD%90) — open-source CAD software & libraries
- https://github.com/kimimgo/awesome-ai-cae ![GitHub stars](https://img.shields.io/github/stars/kimimgo/awesome-ai-cae?style=flat&label=%E2%AD%90) — AI-callable CAE/CAD tooling
- https://awesome.re/ — Awesome manifesto

---

## Contributing

PRs and issues welcome. Prefer **open-source solvers** with durable official or GitHub URLs, a short blurb, and clear category fit. Avoid CAD-only apps (point those to [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae)). Keep EN and JA READMEs in sync.

License for this list: content is dedicated to the public domain where possible; individual linked projects retain their own licenses (GPL, LGPL, BSD, Apache-2.0, etc).

---

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
