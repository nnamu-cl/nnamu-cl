## Nicholas Namusanga

**GPU Kernel Engineer.** CUDA kernel development, PTX/SASS-level performance tuning, 10 years of GPU compute.

I build and optimize CUDA kernels and GPU pipelines for AI and HPC workloads. I work below the framework line: kernels written by hand, SASS read in Nsight Compute, memory traffic priced in bytes per element before the first line is written, and a retro afterwards that says where the model was wrong. Ten years of low-level C++ on compute and memory bound workloads across AI compute, real-time video, simulation and numerical methods.

### Highlights

#### [cuda-orbital-sampler](https://github.com/nnamu-cl/cuda-orbital-sampler) · Optimizing quantum compute on CUDA, Act I

A Monte Carlo sampler for hydrogen electron densities, taken from a CPU loop to 14.6 Gsamples/s on an RTX 2070 Super. The maths per sample is tiny, so the whole problem is DRAM bandwidth and latency: the random number state alone was 86% of the bytes moved in the first six kernels. Nine kernels, a prediction and falsification line before each one, a statistical verify gate that catches the bugs the visualizers on the internet ship with, and Nsight Compute reports for every step. Article in progress.

<p align="center">
  <a href="https://github.com/nnamu-cl/cuda-orbital-sampler">
    <img src="ladder.svg" alt="nine CUDA kernels from 0.56 to 14.6 Gsamples/s against the DRAM write roof" width="100%">
  </a>
</p>

#### [psiEngine](https://github.com/nnamu-cl/psiEngine) · Visual quantum physics compute engine

<table>
<tr>
<td width="180" align="center" valign="middle">
  <a href="https://github.com/nnamu-cl/psiEngine"><img src="https://raw.githubusercontent.com/nnamu-cl/psiEngine/master/docs/images/psi-logo.png" width="150" alt="psiEngine"></a>
</td>
<td valign="middle">
Vulkan rendering, GPU compute in Slang, an ECS with atom components that take (n, l, m) and draw the orbital, a typed node graph that drives component properties, and Lua scripting through sol2. Built because every kernel that produces a cloud of numbers needs a place to rotate the cloud and poke at the parameters. The CUDA sampler above is what feeds it.
</td>
</tr>
</table>

#### [cuda-npp-distance-transform](https://github.com/nnamu-cl/cuda-npp-distance-transform)

Stream parallel Euclidean distance transform in CUDA: custom thresholding and normalisation kernels around NPP's PBA+ transform, run over 64 USC SIPI textures with a synthetic correctness check.

#### [procuda-toolkit](https://github.com/nnamu-cl/procuda-toolkit)

CUDA device memory management helpers: scoped allocation sessions.

### Activity

<p align="center">
  <img src="metrics.svg" alt="activity: isometric calendar, commit habits, languages" width="100%">
</p>

### Focus

CUDA, PTX and SASS, Nsight Compute and Systems, roofline and byte accounting, memory bound kernel design, cuRAND and Philox, Vulkan and Slang compute, low level C++.

### Contact

[namusanga.com](https://namusanga.com) · [LinkedIn](https://www.linkedin.com/in/nichwithn) · [@hey_namusanga](https://x.com/hey_namusanga)
