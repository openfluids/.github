# OpenFluids

Open-source tools for nonlinear dynamics, chaos, and the spectral analysis of
spatiotemporal data.

OpenFluids is a home for small, focused, open packages built around dynamical
systems and the data they produce. Each tool does one thing and is meant to be
read, reused, and combined.

## Projects

- [`openmodalpy`](https://github.com/openfluids/openmodalpy) — modal decomposition of
  spatiotemporal data: POD, mPOD, PSD-POD, SPOD, ST-POD, DMD/HODMD, and BSMD behind
  one API, driven by a config file or a CLI. Pure NumPy/SciPy, no external solvers.
  Imports as `modalpy`.
  ```bash
  pip install openmodalpy
  ```
- [`fftkit`](https://github.com/openfluids/fftkit) — one FFT API over eight backends
  (SciPy, NumPy, Intel MKL, CuPy, PyTorch, TensorFlow, pyFFTW, Accelerate). Reports
  which are available on the machine and benchmarks which is fastest for your array
  sizes, without rewriting call sites.
  ```bash
  pip install fftkit
  ```
- [`dsgbr`](https://github.com/openfluids/dsgbr) — spectral peak detection for noisy,
  sloped power spectra, using a Savitzky–Golay search over a rolling-median baseline.
  ```bash
  pip install dsgbr
  ```
- [`chaos-atlas`](https://github.com/openfluids/chaos-atlas) — interactive explorer for
  chaotic dynamical systems: strange attractors, bifurcations, Lyapunov exponents,
  fractals, and coupled-map lattice patterns.

They are built to compose: `openmodalpy` runs its transforms through `fftkit`, so a
backend installed once is available to everything above it.

More tools will appear here as they are released.

## License

Licenses are per-repository — `openmodalpy` and `fftkit` are MIT, `dsgbr` is
BSD-3-Clause. Check the `LICENSE` file in each repo.
