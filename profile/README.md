![openfluids banner](https://raw.githubusercontent.com/openfluids/.github/main/profile/assets/org-banner-v3.jpg)

**An open state-of-the-art, collaborative workshop for fluid flows, with ultra-modern code.**

We build performant numerical tools for the daily work of flow studies: running 
simulations on clusters, turning snapshots into frames, and pulling structure
out of the data. Each tool does one job, is tested against reference results,
and is meant to be read, reused and combined.

## Stability

**[`linstabpy`](https://github.com/openfluids/linstabpy)**: sparse linear
stability and resolvent analysis of 2D compressible flows.

**[`nekStab`](https://github.com/nekStab/nekStab)**: stability, bifurcation and
sensitivity analysis for Nek5000.

## Analysis

**[`openmodalpy`](https://github.com/openfluids/openmodalpy)**: nine modal
decompositions behind one API: POD, mPOD, PSD-POD, SPOD, ST-POD, DMD/HODMD and
BSMD, from a config file or a CLI. Pure NumPy and SciPy.

**[`dynachaos`](https://openfluids.github.io/dynachaos/)**: dynamical-systems
analysis of time signals: Lyapunov exponents, recurrence, entropy and
coupled-map lattices, with Rust-accelerated kernels.

**[`fftkit`](https://github.com/openfluids/fftkit)**: spectra of physical
signals, and one FFT API over eight backends. `spectrum()` handles resampling,
detrending and windowing, and reports what it did; `backend=` swaps the engine
without touching your code.

**[`dsgbr`](https://github.com/openfluids/dsgbr)**: peak detection for noisy
power spectra that slope over decades, scored against a rolling-median baseline
instead of a fixed threshold.

**[`chaos-atlas`](https://openfluids.github.io/chaos-atlas/)**: an interactive
explorer for chaotic systems: strange attractors, bifurcations, fractals and
coupled-map-lattice patterns, in the browser.

## Optimisation

**[`organa`](https://github.com/openfluids/organa)**: adjoint topology
optimisation for conjugate heat transfer, in parallel with MPI.

## Runs and frames

**[`hpckit`](https://github.com/openfluids/hpckit)**: drives Slurm work from a
local checkout: one environment per commit, run packets, submission and polling,
receipts and artifact sync.

**[`quadros`](https://github.com/openfluids/quadros)**: turns simulation
snapshots into checked frames and videos, locally, over SSH or in a scheduler
job, with a manifest of what it rendered. Nek5000 built in; other formats
through PyVista.

## Solvers

**[`dolfinx-rans`](https://github.com/openfluids/dolfinx-rans)**: RANS k-omega and
k-omega SST turbulence solver for incompressible flow in DOLFINx, validated on
turbulent channel flow.

## How they fit

`openmodalpy` runs its transforms through `fftkit`, so a backend installed once
serves both. `hpckit` submits the run and `quadros` renders what comes back;
they stay separate installs, so a machine that only submits jobs never needs VTK.

## On the bench

More is taking shape in the workshop: new solvers, GPU kernels and tools for
studying how flows behave. They will open as they mature.

All openfluids software is provided "as is", without warranty of any kind. Each
repository's LICENSE sets the terms of use.
