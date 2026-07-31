![openfluids banner](https://raw.githubusercontent.com/openfluids/.github/main/profile/assets/org-banner-v3.jpg)

`openfluids` is a home for small, focused, open packages built around dynamical
systems, chaos, and the spectral analysis of spatiotemporal data. Each tool does
one thing, and is meant to be read, reused, and combined.

## Projects

**[`fftkit`](https://github.com/openfluids/fftkit)** — spectra of physical
signals, and one FFT API over eight backends (SciPy, NumPy, Intel MKL, CuPy,
PyTorch, TensorFlow, pyFFTW, Accelerate). `spectrum()` handles the resampling,
detrending and windowing a non-uniformly sampled record needs, and reports what
it did; below that, swapping `backend=` leaves your call sites alone.

**[`openmodalpy`](https://github.com/openfluids/openmodalpy)** — nine modal
decomposition methods for spatiotemporal data behind one API: POD, mPOD,
PSD-POD, SPOD, ST-POD, DMD/HODMD and BSMD, driven by a config file or a CLI.
Pure NumPy/SciPy, no external solvers.

**[`dynachaos`](https://github.com/openfluids/dynachaos)** — dynamical-systems
analysis of measured or simulated time signals: maps and coupled-map lattices,
Lyapunov exponents, recurrence quantification, entropy diagnostics, correlation
dimension and multifractal spectra, with Rust-accelerated kernels where those
have parity tests.

**[`dsgbr`](https://github.com/openfluids/dsgbr)** — spectral peak detection for
noisy power spectra that slope over several decades, using a Savitzky–Golay
search scored against a rolling-median baseline rather than a fixed threshold.

**[`chaos-atlas`](https://github.com/openfluids/chaos-atlas)** — an interactive
explorer for chaotic dynamical systems: strange attractors, bifurcations,
Lyapunov exponents, fractals and coupled-map-lattice patterns. Runs in the
browser; the map kernels also ship as a Python package.

**[`quadros`](https://github.com/openfluids/quadros)** — turns simulation
snapshots into checked frame sets and videos. Runs locally, over SSH, inside a
container or from a scheduler job without copying scripts into case directories,
and writes a manifest of what it rendered so dense snapshots can be deleted with
something to check against. Nek5000 has dedicated support; other formats go
through PyVista.

**[`hpckit`](https://github.com/openfluids/hpckit)** — drives Slurm work from a
local checkout: remote tool checkouts, an immutable virtualenv per commit, run
packets, submission and polling, receipts and artifact sync. The tools it runs
are declared in your own config file — it ships none of them, and needs nothing
but a YAML parser itself.

They are built to compose: `openmodalpy` runs its transforms through `fftkit`, so
a backend installed once is available to everything above it. `hpckit` and
`quadros` pair the same way — `hpckit` submits the run, `quadros` renders what
comes back — but they stay separate installs on purpose, since a machine that
only submits jobs should not pay for VTK.

More tools will appear here as they are released.
