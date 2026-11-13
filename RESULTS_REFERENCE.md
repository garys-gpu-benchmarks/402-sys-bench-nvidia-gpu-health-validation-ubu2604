# Results: 402 NVIDIA System Validation (clocks, temperature, etc.)

**Main goal:** Analyze GPU CUDA runtime environment health  
**Tools:** Run nvidia-smi, nvidia-smi -q, nvidia-smi -L, and dmesg

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 80GB HBM3 (81559 MiB) · Intel(R) Xeon(R) Platinum 8470 · Ubuntu 26.04.1 LTS · kernel 6.8.0-147-generic · driver 595.91.07
- **Run:** 2026-11-12T22:35:47Z · status **N/A-EXPECTED** (exit 0)
- **Time (mm:ss):** setup 00:35 · benchmark 00:06 · whole run 00:48
- **Source:** run 402_20261112_223547
- **Command:** `bash run_benchmark.sh --smoke --monitor-duration-sec 5 --expected-gpu-count 1 --min-pcie-link-width 16`

| # | Metric | Result |
|---|---|---|
| 1 | GPU fault/Xid count (dmesg_nvidia_gpu_fault_xid_count) | na (expected: dmesg not readable) |
| 2 | GPU temperature (gpu_temperature_c) | 27.0 |
| 3 | PCIe link width, lanes (pcie_link_width_lanes) | 16.0 |
| 4 | PCIe link speed, GT/s (pcie_link_speed_gt_s) | 32.0 |
| 5 | CUDA devices visible (cuda_devices_visible) | 1.0 |
<!-- /profile:smoke -->
