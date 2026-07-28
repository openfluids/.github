![openfluids banner](https://raw.githubusercontent.com/openfluids/.github/main/profile/assets/org-banner-v1.jpg)

`openfluids` is a home for small, focused, open packages built around dynamical
systems, chaos, and the spectral analysis of spatiotemporal data. Each tool does
one thing, and is meant to be read, reused, and combined.

## Projects

- [`fftkit`](https://github.com/openfluids/fftkit) — spectra of physical signals,
  and one FFT API over eight backends (SciPy, NumPy, Intel MKL, CuPy, PyTorch,
  TensorFlow, pyFFTW, Accelerate). `spectrum()` handles the resampling,
  detrending and windowing a non-uniformly sampled record needs, and reports what
  it did; below that, swapping `backend=` leaves your call sites alone.
  ```bash
  pip install fftkit
  ```
- [`openmodalpy`](https://github.com/openfluids/openmodalpy) — nine modal
  decomposition methods for spatiotemporal data behind one API: POD, mPOD,
  PSD-POD, SPOD, ST-POD, DMD/HODMD and BSMD, driven by a config file or a CLI.
  Pure NumPy/SciPy, no external solvers.
  ```bash
  pip install openmodalpy
  ```
- [`dynachaos`](https://github.com/openfluids/dynachaos) — dynamical-systems
  analysis of measured or simulated time signals: maps and coupled-map lattices,
  Lyapunov exponents, recurrence quantification, entropy diagnostics, correlation
  dimension and multifractal spectra, with Rust-accelerated kernels where those
  have parity tests.
  ```bash
  pip install dynachaos
  ```
- [`dsgbr`](https://github.com/openfluids/dsgbr) — spectral peak detection for
  noisy power spectra that slope over several decades, using a Savitzky–Golay
  search scored against a rolling-median baseline rather than a fixed threshold.
  ```bash
  pip install dsgbr
  ```
- [`chaos-atlas`](https://github.com/openfluids/chaos-atlas) — an interactive
  explorer for chaotic dynamical systems: strange attractors, bifurcations,
  Lyapunov exponents, fractals and coupled-map-lattice patterns. Runs in the
  browser; the map kernels also ship as a Python package.
  ```bash
  pip install chaos-atlas
  ```

They are built to compose: `openmodalpy` runs its transforms through `fftkit`, so
a backend installed once is available to everything above it.

More tools will appear here as they are released.

## License

Licences are per-repository. See the `LICENSE` and `NOTICE` files in each
repository for the authoritative terms.
