# Awesome Open-Source Solvers（日本語）

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[English README](README.md)

オープンソースの**ソルバ**と科学計算スタックのキュレーション — FEM、BEM、CFD、マルチボディ／ダイナミクス、粒子法、音響、電子回路／電磁界、燃焼、気象／気候、量子、および線形代数・メッシュ補助。公式ドキュメントや GitHub のある耐久性の高いプロジェクトを優先。CAD/CAE リストとの重複は可。本リストは CAD アプリではなく**ソルバ**に焦点を当てる。⭐ バッジは GitHub のスター数をリアルタイム表示します(shields.io)。

## 目次

- [有限要素法（FEM）](#有限要素法fem)
- [境界要素法（BEM）](#境界要素法bem)
- [CFD](#cfd)
- [マルチボディ／構造ダイナミクス](#マルチボディ構造ダイナミクス)
- [粒子法（MD / DEM / SPH / PIC）](#粒子法md--dem--sph--pic)
- [音響／構造音響](#音響構造音響)
- [電子回路／電磁界](#電子回路電磁界)
- [燃焼／反応流れ](#燃焼反応流れ)
- [気象／気候](#気象気候)
- [量子／電子構造／量子ダイナミクス](#量子電子構造量子ダイナミクス)
- [線形代数と並列ソルバ](#線形代数と並列ソルバ)
- [メッシュ／プリポスト（簡潔）](#メッシュプリポスト簡潔)
- [関連リスト](#関連リスト)
- [コントリビューション](#コントリビューション)
- [shvyac の awesome リスト](#shvyac-の-awesome-リスト)

---

## 有限要素法（FEM）

構造・熱・マルチフィジックス PDE 向けのライブラリおよび産業／研究用 FEM コード。

### deal.II
適応・並列・行列フリー離散化向けの C++ FEM ライブラリ。ノート PC から HPC まで。チュートリアルとコミュニティが充実。

- https://dealii.org/
- https://github.com/dealii/dealii ![GitHub stars](https://img.shields.io/github/stars/dealii/dealii?style=flat&label=%E2%AD%90)

### FEniCS / DOLFINx
変分定式化と連成 PDE を迅速に書ける Python ファーストの FEM プラットフォーム（FEniCSx / DOLFINx）。

- https://fenicsproject.org/
- https://github.com/FEniCS

### MFEM
高次手法・GPU/HPC・研究向け離散化（Galerkin、DG、混合、DPG）のための軽量でスケーラブルな C++ FEM ツールボックス。

- https://mfem.org/
- https://github.com/mfem/mfem ![GitHub stars](https://img.shields.io/github/stars/mfem/mfem?style=flat&label=%E2%AD%90)

### CalculiX
Abaqus 風のオープンソース 3D 構造 FEM（ccx ソルバ + cgx）。FreeCAD FEM や PrePoMax GUI と広く併用。

- https://www.dhondt.de/
- https://github.com/Dhondtguido/CalculiX ![GitHub stars](https://img.shields.io/github/stars/Dhondtguido/CalculiX?style=flat&label=%E2%AD%90)
- https://github.com/calculix

### Code_Aster
EDF の産業向け構造力学／マルチフィジックス FEM スイート。プリ／ポストは SALOME-Meca と組み合わせることが多い。

- https://code-aster.org/
- https://gitlab.com/codeaster

### Elmer
流体・固体・電磁・熱および連成問題向けのオープンなマルチフィジックス FEM。GUI と並列ソルバあり。

- https://www.elmerfem.org/
- https://github.com/ElmerCSC/elmerfem ![GitHub stars](https://img.shields.io/github/stars/ElmerCSC/elmerfem?style=flat&label=%E2%AD%90)

### FreeFEM / SfePy / Firedrake / scikit-fem
カスタム物理や研究向けに、DSL または Python インタフェースを持つ PDE/FEM プラットフォーム。

- https://freefem.org/ — https://github.com/FreeFem/FreeFem-sources ![GitHub stars](https://img.shields.io/github/stars/FreeFem/FreeFem-sources?style=flat&label=%E2%AD%90)
- https://sfepy.org/ — https://github.com/sfepy/sfepy ![GitHub stars](https://img.shields.io/github/stars/sfepy/sfepy?style=flat&label=%E2%AD%90)
- https://www.firedrakeproject.org/ — https://github.com/firedrakeproject/firedrake ![GitHub stars](https://img.shields.io/github/stars/firedrakeproject/firedrake?style=flat&label=%E2%AD%90)
- https://scikit-fem.readthedocs.io/ — https://github.com/kinnala/scikit-fem ![GitHub stars](https://img.shields.io/github/stars/kinnala/scikit-fem?style=flat&label=%E2%AD%90)

### MOOSE / libMesh / GetDP
libMesh 上のマルチフィジックス環境（MOOSE）。GetDP は連成 FEM（しばしば Gmsh/ONELAB と併用）。

- https://mooseframework.inl.gov/ — https://github.com/idaholab/moose ![GitHub stars](https://img.shields.io/github/stars/idaholab/moose?style=flat&label=%E2%AD%90)
- https://libmesh.github.io/ — https://github.com/libMesh/libmesh ![GitHub stars](https://img.shields.io/github/stars/libMesh/libmesh?style=flat&label=%E2%AD%90)
- https://getdp.info/ — https://gitlab.onelab.info/getdp/getdp

### FrontISTR / MYSTRAN / FEBio / NGSolve
大規模非線形構造（FrontISTR）；Nastran 風解析（MYSTRAN）；生体力学の非線形 FEM（FEBio）；Netgen + NGSolve FEM プラットフォーム。

- https://www.frontistr.com/ — https://gitlab.com/FrontISTR-Commons/FrontISTR （主開発。GitHub はミラー）
- https://mystran.com/ — https://github.com/dr-bill-c/MYSTRAN ![GitHub stars](https://img.shields.io/github/stars/dr-bill-c/MYSTRAN?style=flat&label=%E2%AD%90)
- https://febio.org/ — https://github.com/febiosoftware/FEBio ![GitHub stars](https://img.shields.io/github/stars/febiosoftware/FEBio?style=flat&label=%E2%AD%90)
- https://ngsolve.org/ — https://github.com/NGSolve/ngsolve ![GitHub stars](https://img.shields.io/github/stars/NGSolve/ngsolve?style=flat&label=%E2%AD%90)

### Kratos Multiphysics
並列マルチディシプリン・シミュレーション向けの BSD ライセンス C++/Python フレームワーク — 構造・流体・DEM・FSI・最適化アプリケーション。

- https://kratosmultiphysics.github.io/Kratos/
- https://github.com/KratosMultiphysics/Kratos ![GitHub stars](https://img.shields.io/github/stars/KratosMultiphysics/Kratos?style=flat&label=%E2%AD%90)

### OpenCourant（旧 OpenRadioss）
衝突・衝撃・落下・爆発解析向けの陽解法動的 FEM ソルバ（AGPL-3.0）。Siemens は 2026年10月に OpenRadioss を終了し GitHub リポジトリを削除（現在は Simcenter Radioss / Radioss R&D プログラム）。OpenCourant は全コミット履歴を引き継いだコミュニティフォークで、Rocky Enterprise Software Foundation（RESF）傘下で運営。

- https://opencourant.org/
- https://github.com/OpenCourant/OpenCourant ![GitHub stars](https://img.shields.io/github/stars/OpenCourant/OpenCourant?style=flat&label=%E2%AD%90)

---

## 境界要素法（BEM）

音響・電磁・外部問題向けの表面積分ソルバ。

### Bempp
静電・音響・電磁向けの Python BEM プラットフォーム。Gmsh/VTK I/O、FEniCS による FEM–BEM 連成も可能。

- https://bempp.com/
- https://github.com/bempp

### scuff-em
電磁散乱、Casimir／放射熱伝達、ナノフォトニクス向け BEM スイート（EFIE / PMCHWT、RWG 基底）。

- https://github.com/HomerReid/scuff-em ![GitHub stars](https://img.shields.io/github/stars/HomerReid/scuff-em?style=flat&label=%E2%AD%90)
- http://homerreid.github.io/scuff-em-documentation/

### OpenBEM
2D／3D 幾何向けの MATLAB Helmholtz／音響 BEM コード集。

- https://openbem.dk/

---

## CFD

有限体積・有限要素・格子ボルツマンによる流体ソルバ。

### OpenFOAM
最も広く使われるオープンソース CFD ツールボックス — 非圧縮／圧縮流れ、伝熱、多相、反応。大きな生態系。OpenCFD 版の最新は v2606（2026年6月）。同版のリポジトリは 2025年11月に gitlab.com/openfoam へ移転。

- https://www.openfoam.com/ — https://gitlab.com/openfoam
- https://openfoam.org/
- https://github.com/OpenFOAM/OpenFOAM-dev ![GitHub stars](https://img.shields.io/github/stars/OpenFOAM/OpenFOAM-dev?style=flat&label=%E2%AD%90)

### SU2
勾配ベースの空力形状最適化と随伴機能を備えたマルチフィジックス PDE ソルバ。

- https://su2code.github.io/
- https://github.com/su2code/SU2 ![GitHub stars](https://img.shields.io/github/stars/su2code/SU2?style=flat&label=%E2%AD%90)

### Nektar++ / Lethe
スペクトル／hp 要素 CFD（Nektar++）；高次 CG CFD–DEM（Lethe）。

- https://www.nektar.info/ — https://gitlab.nektar.info/nektar/nektar
- https://chaos-polymtl.github.io/lethe/ — https://github.com/chaos-polymtl/lethe ![GitHub stars](https://img.shields.io/github/stars/chaos-polymtl/lethe?style=flat&label=%E2%AD%90)

### PyFR
非構造格子上の高次 Flux Reconstruction 法による Python CFD フレームワーク — 圧縮性／非圧縮性 Navier–Stokes。GPU バックエンド（CUDA、HIP、OpenCL、Metal）と OpenMP に対応。最新は v3.x。

- https://www.pyfr.org/
- https://github.com/PyFR/PyFR ![GitHub stars](https://img.shields.io/github/stars/PyFR/PyFR?style=flat&label=%E2%AD%90)

### Palabos / waLBerla / OpenLB
複雑流れと HPC 向けの格子ボルツマン法（LBM）CFD フレームワーク。

- https://palabos.unige.ch/ — https://gitlab.com/unigespc/palabos
- https://www.walberla.net/ — https://github.com/lssfau/walberla ![GitHub stars](https://img.shields.io/github/stars/lssfau/walberla?style=flat&label=%E2%AD%90) （公式 FAU GitLab のミラー）
- https://www.openlb.net/ — https://gitlab.com/openlb/release

### Fire Dynamics Simulator (FDS)
NIST の火災駆動流れ CFD。Smokeview 可視化付き。

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds ![GitHub stars](https://img.shields.io/github/stars/firemodels/fds?style=flat&label=%E2%AD%90)

### Code_Saturne / Nek5000 / nekRS
EDF 産業向け CFD（Code_Saturne）；スペクトル要素 CFD（Nek5000 / nekRS）。

- https://www.code-saturne.org/
- https://nek5000.mcs.anl.gov/ — https://github.com/Nek5000/Nek5000 ![GitHub stars](https://img.shields.io/github/stars/Nek5000/Nek5000?style=flat&label=%E2%AD%90)
- https://github.com/Nek5000/nekRS ![GitHub stars](https://img.shields.io/github/stars/Nek5000/nekRS?style=flat&label=%E2%AD%90)

### JAX-Fluids / XLB
物理ベース ML 向けの GPU 加速・微分可能な Python CFD — 圧縮性／多相の有限体積法（JAX-Fluids）、JAX / NVIDIA Warp 上の格子ボルツマン法（XLB）。

- https://github.com/tumaer/JAXFLUIDS ![GitHub stars](https://img.shields.io/github/stars/tumaer/JAXFLUIDS?style=flat&label=%E2%AD%90)
- https://github.com/Autodesk/XLB ![GitHub stars](https://img.shields.io/github/stars/Autodesk/XLB?style=flat&label=%E2%AD%90)

---

## マルチボディ／構造ダイナミクス

剛体・柔軟マルチボディ、機構、車両／ロボットシミュレーション。

### Project Chrono
車両・ロボット・粉体／DEM 接触・FEA 連成などのマルチフィジックス・マルチボディ基盤。

- https://projectchrono.org/
- https://github.com/projectchrono/chrono ![GitHub stars](https://img.shields.io/github/stars/projectchrono/chrono?style=flat&label=%E2%AD%90)

### MBDyn / Simbody / EXUDYN
汎用 MBD（MBDyn）；関節付き生体力学／ロボティクス（Simbody）；Python/C++ 柔軟マルチボディ（EXUDYN）。

- https://www.mbdyn.org/ — https://public.gitlab.polimi.it/DAER/mbdyn
- https://github.com/simbody/simbody ![GitHub stars](https://img.shields.io/github/stars/simbody/simbody?style=flat&label=%E2%AD%90)
- https://github.com/jgerstmayr/EXUDYN ![GitHub stars](https://img.shields.io/github/stars/jgerstmayr/EXUDYN?style=flat&label=%E2%AD%90)

### OpenSim / Pinocchio / Drake
筋骨格ダイナミクス（OpenSim）；ロボティクス向け高速剛体ダイナミクス（Pinocchio）；ダイナミクス付きロボティクス／制御（Drake）。

- https://opensim.stanford.edu/ — https://github.com/opensim-org
- https://github.com/stack-of-tasks/pinocchio ![GitHub stars](https://img.shields.io/github/stars/stack-of-tasks/pinocchio?style=flat&label=%E2%AD%90)
- https://drake.mit.edu/ — https://github.com/RobotLocomotion/drake ![GitHub stars](https://img.shields.io/github/stars/RobotLocomotion/drake?style=flat&label=%E2%AD%90)

### MuJoCo
Google DeepMind の Multi-Joint dynamics with Contact — ロボティクス・生体力学・強化学習向けの高速・高精度な剛体／接触物理エンジン（Apache-2.0。MJX や MuJoCo Warp で GPU/JAX 対応）。

- https://mujoco.org/
- https://github.com/google-deepmind/mujoco ![GitHub stars](https://img.shields.io/github/stars/google-deepmind/mujoco?style=flat&label=%E2%AD%90)

### OpenFAST
NLR（旧 NREL）の空力・サーボ・弾性風力タービンダイナミクス（CFD／構造荷重連成ワークフロー）。

- https://openfast.readthedocs.io/
- https://github.com/OpenFAST/openfast ![GitHub stars](https://img.shields.io/github/stars/OpenFAST/openfast?style=flat&label=%E2%AD%90)

---

## 粒子法（MD / DEM / SPH / PIC）

分子動力学、離散要素、SPH、粒子インセルのコード。

### LAMMPS
大規模原子／分子質量並列シミュレータ — 材料 MD、粗視化・メソスケール粒子モデル。

- https://www.lammps.org/
- https://github.com/lammps/lammps ![GitHub stars](https://img.shields.io/github/stars/lammps/lammps?style=flat&label=%E2%AD%90)

### GROMACS
生体分子・ソフトマター向け高性能分子動力学。GPU サポートが強い。

- https://www.gromacs.org/
- https://github.com/gromacs/gromacs ![GitHub stars](https://img.shields.io/github/stars/gromacs/gromacs?style=flat&label=%E2%AD%90)

### DualSPHysics / SPHERA / PySPH
自由表面／沿岸／産業流れの SPH（DualSPHysics）；工学 SPH（SPHERA）；Python SPH フレームワーク（PySPH）。

- https://dual.sphysics.org/ — https://github.com/DualSPHysics/DualSPHysics ![GitHub stars](https://img.shields.io/github/stars/DualSPHysics/DualSPHysics?style=flat&label=%E2%AD%90)
- https://github.com/GiordanoAgateRSE/SPHERA ![GitHub stars](https://img.shields.io/github/stars/GiordanoAgateRSE/SPHERA?style=flat&label=%E2%AD%90)
- https://pysph.readthedocs.io/ — https://github.com/pypr/pysph ![GitHub stars](https://img.shields.io/github/stars/pypr/pysph?style=flat&label=%E2%AD%90)

### LIGGGHTS / Yade / MercuryDPM
粉粒体・産業粒子プロセス向け DEM。

- https://www.cfdem.com/liggghtsr-open-source-discrete-element-method-particle-simulation-code — https://github.com/CFDEMproject/LIGGGHTS-PUBLIC ![GitHub stars](https://img.shields.io/github/stars/CFDEMproject/LIGGGHTS-PUBLIC?style=flat&label=%E2%AD%90) （商用後継は Aspherix）
- https://yade-dem.org/ — https://gitlab.com/yade-dev/trunk
- https://www.mercurydpm.org/ — https://bitbucket.org/mercurydpm/mercurydpm

### WarpX / PIConGPU / Smilei
エクサスケール電磁 PIC（WarpX）；GPU PIC（PIConGPU）；プラズマ PIC（Smilei）。

- https://warpx.readthedocs.io/ — https://github.com/BLAST-WarpX/warpx ![GitHub stars](https://img.shields.io/github/stars/BLAST-WarpX/warpx?style=flat&label=%E2%AD%90)
- https://picongpu.readthedocs.io/ — https://github.com/ComputationalRadiationPhysics/picongpu ![GitHub stars](https://img.shields.io/github/stars/ComputationalRadiationPhysics/picongpu?style=flat&label=%E2%AD%90)
- https://smileipic.github.io/Smilei/ — https://github.com/SmileiPIC/Smilei ![GitHub stars](https://img.shields.io/github/stars/SmileiPIC/Smilei?style=flat&label=%E2%AD%90)

### HOOMD-blue / OpenMM
ソフトマター向け GPU 加速 MD（HOOMD-blue）；高性能生体分子 MD ツールキット（OpenMM）。

- https://glotzerlab.engin.umich.edu/hoomd-blue/ — https://github.com/glotzerlab/hoomd-blue ![GitHub stars](https://img.shields.io/github/stars/glotzerlab/hoomd-blue?style=flat&label=%E2%AD%90)
- https://openmm.org/ — https://github.com/openmm/openmm ![GitHub stars](https://img.shields.io/github/stars/openmm/openmm?style=flat&label=%E2%AD%90)

---

## 音響／構造音響

波動伝播、室内／屋外音響、連成構造音響ソルバ。

### FEM 構造音響（Code_Aster / Elmer / CalculiX）
産業向け FEM スイートによる構造–音響連成（FEM 節を参照）。

- https://code-aster.org/
- https://www.elmerfem.org/
- https://www.dhondt.de/

### 音響 BEM（Bempp / OpenBEM / scuff-em）
境界要素による外部／内部 Helmholtz／電磁–音響ソルバ（BEM 節を参照）。

- https://bempp.com/
- https://openbem.dk/
- http://homerreid.github.io/scuff-em-documentation/

### k-Wave
時間領域の音響／超音波波動場向け MATLAB/C++ ツールボックス。v1.4.x が k-Wave-I の最終版となり、後継の k-Wave-II は別リポジトリで開発中。Python インタフェース（k-wave-python）あり。

- http://www.k-wave.org/
- https://github.com/ucl-bug/k-wave ![GitHub stars](https://img.shields.io/github/stars/ucl-bug/k-wave?style=flat&label=%E2%AD%90)
- https://github.com/ucl-bug/k-wave-ii ![GitHub stars](https://img.shields.io/github/stars/ucl-bug/k-wave-ii?style=flat&label=%E2%AD%90)
- https://github.com/waltsims/k-wave-python ![GitHub stars](https://img.shields.io/github/stars/waltsims/k-wave-python?style=flat&label=%E2%AD%90)

### GetDP / ONELAB 音響
GetDP + Gmsh/ONELAB ワークフローによる連成 FEM 音響とマルチフィジックス。

- https://getdp.info/
- https://onelab.info/

---

## 電子回路／電磁界

回路（SPICE）シミュレータと電磁界ソルバ。Elmer / GetDP（FEM 電磁界）や scuff-em（BEM）も参照。LTspice や QSPICE のように無料でもソース非公開のツールは対象外。

### ngspice
オープンソースのミックスドシグナル SPICE シミュレータ（Berkeley SPICE3f5 の後継）。KiCad に組み込まれ、Qucs-S や PySpice のバックエンドとしても使われる。

- https://ngspice.sourceforge.io/ — https://sourceforge.net/p/ngspice/ngspice/

### Xyce
Sandia による大規模並列・SPICE 互換の回路シミュレータ。大規模アナログ回路向け（GPL v3）。

- https://xyce.sandia.gov/ — https://github.com/Xyce/Xyce ![GitHub stars](https://img.shields.io/github/stars/Xyce/Xyce?style=flat&label=%E2%AD%90)

### Qucs-S / PySpice
ngspice・Xyce・QucsatorRF を駆動する回路図入力＋シミュレーションの GUI フロントエンド（Qucs-S）；ngspice / Xyce を Python から操作してスクリプトで回路解析（PySpice。ドキュメントサイトは 2021 年以降更新なし）。

- https://ra3xdh.github.io/ — https://github.com/ra3xdh/qucs_s ![GitHub stars](https://img.shields.io/github/stars/ra3xdh/qucs_s?style=flat&label=%E2%AD%90)
- https://pyspice.fabrice-salvaire.fr/ — https://github.com/PySpice-org/PySpice ![GitHub stars](https://img.shields.io/github/stars/PySpice-org/PySpice?style=flat&label=%E2%AD%90)

### openEMS / Meep
FDTD 法による電磁界ソルバ — MATLAB/Octave/Python インタフェースでアンテナや基板・高周波構造を解析（openEMS）；Python スクリプトによるナノフォトニクス・汎用電磁界解析（Meep、MIT）。

- https://www.openems.de/ — https://github.com/thliebig/openEMS-Project ![GitHub stars](https://img.shields.io/github/stars/thliebig/openEMS-Project?style=flat&label=%E2%AD%90)
- https://meep.readthedocs.io/ — https://github.com/NanoComp/meep ![GitHub stars](https://img.shields.io/github/stars/NanoComp/meep?style=flat&label=%E2%AD%90)

### Palace
AWS による計算電磁気学向け 3D 有限要素ソルバ（固有モード、周波数／時間領域、静電界、静磁界）。超伝導量子回路などに利用。MFEM ベース。

- https://awslabs.github.io/palace/stable/ — https://github.com/awslabs/palace ![GitHub stars](https://img.shields.io/github/stars/awslabs/palace?style=flat&label=%E2%AD%90)

---

## 燃焼／反応流れ

化学反応速度論、反応 CFD、火災／燃焼パッケージ。

### Cantera
化学反応速度・熱力学・輸送ライブラリ — 反応機構、0D/1D 反応器、CFD 連成。

- https://cantera.org/
- https://github.com/Cantera/cantera ![GitHub stars](https://img.shields.io/github/stars/Cantera/cantera?style=flat&label=%E2%AD%90)

### OpenFOAM 反応／燃焼ソルバ
OpenFOAM ツールボックス上の reacting／chemistry／combustion パッケージ。

- https://www.openfoam.com/documentation/overview
- https://openfoam.org/

### Fire Dynamics Simulator (FDS)
火災駆動の反応浮力流れ（CFD 節も参照）。

- https://pages.nist.gov/fds-smv/
- https://github.com/firemodels/fds ![GitHub stars](https://img.shields.io/github/stars/firemodels/fds?style=flat&label=%E2%AD%90)

### PeleC / PeleLMeX / PelePhysics
AMReX ベースの圧縮性／低マッハ反応流れソルバ（DOE エクサスケール燃焼スタック。現在は Pele Suite として公開）。

- https://pele-suite.github.io/
- https://github.com/Pele-Suite

### CoolProp
オープンソースの熱力学・輸送物性（反応流れワークフローの補助として有用）。

- https://coolprop.org/
- https://github.com/CoolProp/CoolProp ![GitHub stars](https://img.shields.io/github/stars/CoolProp/CoolProp?style=flat&label=%E2%AD%90)

---

## 気象／気候

数値天気予報（NWP）、地球システム／気候モデル、機械学習による気象予測。学習済み重みのライセンスはモデルごとに異なるため、利用前に確認すること。

### WRF / MPAS
世界で最も広く使われるオープンな領域数値予報モデル（WRF、NCAR）；非構造ボロノイメッシュによる全球〜領域モデル（MPAS-Atmosphere、NCAR / LANL）。

- https://www.mmm.ucar.edu/models/wrf — https://github.com/wrf-model/WRF ![GitHub stars](https://img.shields.io/github/stars/wrf-model/WRF?style=flat&label=%E2%AD%90)
- https://mpas-dev.github.io/ — https://github.com/MPAS-Dev/MPAS-Model ![GitHub stars](https://img.shields.io/github/stars/MPAS-Dev/MPAS-Model?style=flat&label=%E2%AD%90)

### UFS Weather Model
FV3 力学コアに基づく NOAA の統合予報システム — 現業の GFS を支えるコミュニティモデル。

- https://ufs.epic.noaa.gov/
- https://github.com/ufs-community/ufs-weather-model ![GitHub stars](https://img.shields.io/github/stars/ufs-community/ufs-weather-model?style=flat&label=%E2%AD%90)

### ICON
DWD / MPI-M の正二十面体格子・非静力学の気象・気候モデル。2024年から BSD-3-Clause でオープンソース化。

- https://www.icon-model.org/
- https://gitlab.dkrz.de/icon/icon-model

### CESM / E3SM
大気・海洋・陸面・海氷を結合した気候シミュレーション向け地球システムモデル（CESM は NCAR、E3SM は米国 DOE）。

- https://www.cesm.ucar.edu/ — https://github.com/ESCOMP/CESM ![GitHub stars](https://img.shields.io/github/stars/ESCOMP/CESM?style=flat&label=%E2%AD%90)
- https://e3sm.org/ — https://github.com/E3SM-Project/E3SM ![GitHub stars](https://img.shields.io/github/stars/E3SM-Project/E3SM?style=flat&label=%E2%AD%90)

### Anemoi / AIFS
ML 気象モデルの学習・実行のための ECMWF のフレームワーク（データセット、グラフ、モデル、学習、推論）。ECMWF の現業 AI 予報 AIFS はこれで構築（重みは CC BY 4.0）。

- https://anemoi.readthedocs.io/ — https://github.com/ecmwf/anemoi-core ![GitHub stars](https://img.shields.io/github/stars/ecmwf/anemoi-core?style=flat&label=%E2%AD%90)
- https://huggingface.co/ecmwf/aifs-single-1.1

### GraphCast / GenCast / NeuralGCM
Google DeepMind の ML 中期予報 — 決定論的な GraphCast とアンサンブルの GenCast（リポジトリは graphcast から weathernext に改名）；微分可能な力学コアと ML を組み合わせたハイブリッド大気モデル NeuralGCM。

- https://github.com/google-deepmind/weathernext ![GitHub stars](https://img.shields.io/github/stars/google-deepmind/weathernext?style=flat&label=%E2%AD%90)
- https://neuralgcm.readthedocs.io/ — https://github.com/neuralgcm/neuralgcm ![GitHub stars](https://img.shields.io/github/stars/neuralgcm/neuralgcm?style=flat&label=%E2%AD%90)

### Earth2Studio / Aurora / Pangu-Weather
AI 気象・気候モデル（FourCastNet など）を実行する NVIDIA のフレームワーク；Microsoft の地球システム基盤モデル Aurora；Huawei の 3D Transformer 予報モデル Pangu-Weather。

- https://nvidia.github.io/earth2studio/ — https://github.com/NVIDIA/earth2studio ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/earth2studio?style=flat&label=%E2%AD%90)
- https://microsoft.github.io/aurora/ — https://github.com/microsoft/aurora ![GitHub stars](https://img.shields.io/github/stars/microsoft/aurora?style=flat&label=%E2%AD%90)
- https://github.com/198808xc/Pangu-Weather ![GitHub stars](https://img.shields.io/github/stars/198808xc/Pangu-Weather?style=flat&label=%E2%AD%90)

---

## 量子／電子構造／量子ダイナミクス

DFT、多体電子構造、開放量子系。

### Quantum ESPRESSO
材料・分子向け平面波 DFT／電子構造スイート。大きなユーザコミュニティ。

- https://www.quantum-espresso.org/
- https://gitlab.com/QEF/q-e

### ABINIT / CP2K / SIESTA / GPAW
固体・化学・ナノ系向けの平面波および局在軌道 DFT コード。

- https://www.abinit.org/ — https://github.com/abinit/abinit ![GitHub stars](https://img.shields.io/github/stars/abinit/abinit?style=flat&label=%E2%AD%90)
- https://www.cp2k.org/ — https://github.com/cp2k/cp2k ![GitHub stars](https://img.shields.io/github/stars/cp2k/cp2k?style=flat&label=%E2%AD%90)
- https://gitlab.com/siesta-project/siesta
- https://gpaw.readthedocs.io/ — https://gitlab.com/gpaw/gpaw

### QuTiP
Python の量子ツールボックス — 開放量子系、マスター方程式、量子光学ダイナミクス。

- https://qutip.org/
- https://github.com/qutip/qutip ![GitHub stars](https://img.shields.io/github/stars/qutip/qutip?style=flat&label=%E2%AD%90)

### NWChem / Psi4 / PySCF
計算化学スイート（NWChem）；量子化学（Psi4）；Python 量子化学（PySCF）。

- https://nwchemgit.github.io/ — https://github.com/nwchemgit/nwchem ![GitHub stars](https://img.shields.io/github/stars/nwchemgit/nwchem?style=flat&label=%E2%AD%90)
- https://psicode.org/ — https://github.com/psi4/psi4 ![GitHub stars](https://img.shields.io/github/stars/psi4/psi4?style=flat&label=%E2%AD%90)
- https://pyscf.org/ — https://github.com/pyscf/pyscf ![GitHub stars](https://img.shields.io/github/stars/pyscf/pyscf?style=flat&label=%E2%AD%90)

### Yambo / BerkeleyGW / Octopus
多体摂動論／GW-BSE（Yambo、BerkeleyGW）；実空間 TDDFT（Octopus）。

- https://www.yambo-code.eu/ — https://github.com/yambo-code/yambo ![GitHub stars](https://img.shields.io/github/stars/yambo-code/yambo?style=flat&label=%E2%AD%90)
- https://berkeleygw.org/ — https://berkeleygw.org/download/ （ソース tarball。旧 BGW-public GitHub リポジトリは消滅）
- https://octopus-code.org/ — https://gitlab.com/octopus-code/octopus

---

## 線形代数と並列ソルバ

上記の多くのコードを支える疎行列反復／直接ソルバと HPC 数値ライブラリ。

### PETSc（+ TAO）
科学計算向けポータブル拡張ツールキット — Krylov ソルバ、前処理、非線形／時間積分、TAO 最適化。C/Fortran/Python（petsc4py）。

- https://petsc.org/
- https://gitlab.com/petsc/petsc
- https://github.com/petsc/petsc ![GitHub stars](https://img.shields.io/github/stars/petsc/petsc?style=flat&label=%E2%AD%90)

### Trilinos
HPC 線形代数・ソルバ・離散化・マルチフィジックス向けパッケージ群（Belos、Ifpack2、MueLu、Tpetra など）。

- https://trilinos.github.io/
- https://github.com/trilinos/Trilinos ![GitHub stars](https://img.shields.io/github/stars/trilinos/Trilinos?style=flat&label=%E2%AD%90)

### hypre
大規模疎行列向け高性能並列マルチグリッド前処理・ソルバ（BoomerAMG など）。

- https://computing.llnl.gov/projects/hypre-scalable-linear-solvers-multigrid-methods
- https://github.com/hypre-space/hypre ![GitHub stars](https://img.shields.io/github/stars/hypre-space/hypre?style=flat&label=%E2%AD%90)

### AMGX / Ginkgo
GPU 加速の疎行列反復ソルバ — NVIDIA の分散代数的マルチグリッド／Krylov ライブラリ（AMGX）；CUDA / HIP / SYCL / OpenMP バックエンドを持つポータブルな C++ 疎行列線形代数（Ginkgo）。

- https://github.com/NVIDIA/AMGX ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/AMGX?style=flat&label=%E2%AD%90)
- https://gko-project.org/ — https://github.com/ginkgo-project/ginkgo ![GitHub stars](https://img.shields.io/github/stars/ginkgo-project/ginkgo?style=flat&label=%E2%AD%90)

### SuperLU / MUMPS / SuiteSparse
疎行列直接ソルバ — SuperLU / SuperLU_DIST；MUMPS マルチフロンタル；SuiteSparse（UMFPACK、CHOLMOD、SPQR など）。

- https://portal.nersc.gov/project/sparse/superlu/ — https://github.com/xiaoyeli/superlu ![GitHub stars](https://img.shields.io/github/stars/xiaoyeli/superlu?style=flat&label=%E2%AD%90)
- https://mumps-solver.org/
- https://people.engr.tamu.edu/davis/suitesparse.html — https://github.com/DrTimothyAldenDavis/SuiteSparse ![GitHub stars](https://img.shields.io/github/stars/DrTimothyAldenDavis/SuiteSparse?style=flat&label=%E2%AD%90)

### Eigen / OpenBLAS
多くのソルバ内部で使われる密行列線形代数の部品。

- https://libeigen.gitlab.io/ — https://gitlab.com/libeigen/eigen
- https://openmathlib.org/OpenBLAS/ — https://github.com/OpenMathLib/OpenBLAS ![GitHub stars](https://img.shields.io/github/stars/OpenMathLib/OpenBLAS?style=flat&label=%E2%AD%90)

### Dakota
シミュレーションコードを包む Sandia の最適化・UQ・モデル校正ツールキット。

- https://dakota.sandia.gov/
- https://github.com/snl-dakota/dakota ![GitHub stars](https://img.shields.io/github/stars/snl-dakota/dakota?style=flat&label=%E2%AD%90)

### preCICE
分離型マルチフィジックス（FSI、共役熱伝達）向け連成ライブラリ。OpenFOAM、CalculiX、Code_Aster、deal.II、FEniCS、SU2 などのアダプタあり。

- https://precice.org/
- https://github.com/precice/precice ![GitHub stars](https://img.shields.io/github/stars/precice/precice?style=flat&label=%E2%AD%90)

---

## メッシュ／プリポスト（簡潔）

上記ソルバと組み合わせる幾何メッシングと可視化（フル CAD リストではない）。

### Gmsh
CAD カーネルオプション、`.geo` スクリプト、ポスト処理を備えたオープンソース 3D FE メッシュ生成器。

- https://gmsh.info/
- https://gitlab.onelab.info/gmsh/gmsh

### Netgen / SALOME / meshio
四面体メッシング（Netgen）；CAD／メッシュのプリポスト（SALOME）；Python メッシュ形式 I/O（meshio）。

- https://ngsolve.org/ — https://github.com/NGSolve/netgen ![GitHub stars](https://img.shields.io/github/stars/NGSolve/netgen?style=flat&label=%E2%AD%90)
- https://www.salome-platform.org/
- https://github.com/nschloe/meshio ![GitHub stars](https://img.shields.io/github/stars/nschloe/meshio?style=flat&label=%E2%AD%90)

### ParaView / VTK / VisIt
CFD/FEM 結果の科学可視化（ParaView、VTK）；大規模並列データ向け VisIt。

- https://www.paraview.org/ — https://github.com/Kitware/ParaView ![GitHub stars](https://img.shields.io/github/stars/Kitware/ParaView?style=flat&label=%E2%AD%90)
- https://vtk.org/ — https://github.com/Kitware/VTK ![GitHub stars](https://img.shields.io/github/stars/Kitware/VTK?style=flat&label=%E2%AD%90)
- https://visit-dav.github.io/visit-website/ — https://github.com/visit-dav/visit ![GitHub stars](https://img.shields.io/github/stars/visit-dav/visit?style=flat&label=%E2%AD%90)

---

## 関連リスト

- https://github.com/shvyac/awesome-cad-cae ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90) — CAD / CAE / EDA / フォーマット（より広いツールチェーン）
- https://github.com/mlightcad/awesome-cad ![GitHub stars](https://img.shields.io/github/stars/mlightcad/awesome-cad?style=flat&label=%E2%AD%90) — オープンソース CAD ソフトウェアとライブラリ
- https://github.com/kimimgo/awesome-ai-cae ![GitHub stars](https://img.shields.io/github/stars/kimimgo/awesome-ai-cae?style=flat&label=%E2%AD%90) — AI 呼び出し可能な CAE/CAD ツール
- https://awesome.re/ — Awesome manifesto

---

## コントリビューション

PR と issue を歓迎。耐久性のある公式または GitHub URL、短い説明、明確なカテゴリ適合を持つ**オープンソースソルバ**を優先。CAD のみのアプリは避け、[awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) へ誘導。EN と JA の README を同期すること。

本リストのライセンス：可能な範囲でパブリックドメイン相当。リンク先プロジェクトは各々のライセンス（GPL、LGPL、BSD、Apache-2.0 など）を保持。

---

## shvyac の awesome リスト

[shvyac](https://github.com/shvyac) が管理しているキュレーションリストの一覧:

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
