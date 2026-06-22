# The 5-Project Systems Engineering Portfoilio by Antt Bhone Yaung Thwe

A portfolio of zero-bloat, high-performance computing infrastructure engines built from scratch using pure **C++20**, **CUDA**, and the **Linux Systems API**. 

Targeting production-grade infrastructure, bare-metal hardware optimization, and absolute zero-memory-leak designs for deep-tech roles.

---

## ⚡ Key Architecture Philosophy
* **Zero Dependencies:** No frameworks, no external math wrappers, no heavy runtimes.
* **Bare-Metal Mastery:** Manual memory layout control, strict hardware cache line alignment, and explicit thread configuration.
* **RAII & Performance:** Pure Object-Oriented tracking with custom destructors and move semantics to bypass expensive Operating System copy calls.

---

## 📂 Project Architecture

```text
├── 01_zero_bloat_llm/            # 1B Parameter LLM Engine from scratch
│   ├── include/                  # Tokenizer, Matrix, and Linear Algebra headers
│   ├── src/                      # Host CPU engine & custom CUDA kernels
│   └── benchmarks/               # High-resolution time-profile logs
│
├── 02_robotics_allocator/        # Deterministic Lock-Free Pool Allocator
│   ├── include/                  # Atomic free-list definitions
│   └── test/                     # Valgrind profiles & fragmentation analysis
│
├── 03_cpu_rasterizer/            # 3D Graphics Engine without external tools
│   ├── src/                      # SIMD vectorization loops & Z-buffer depth calculations
│   └── main.cpp                  # Mini window bridge layer
│
├── 04_embedded_robot_agent/     # Capstone: Integrated Virtual 3D Simulation Loop
│   └── src/                      # Double-buffering state & backpropagation loops
│
└── 05_linux_terminal_shell/      # Custom Unix Shell Interface via POSIX System APIs
    └── shell.cpp                 # Process splitting, fork(), dup2(), and piping
```

---

## 🚀 Execution & Tracking Matrix

### 🟢 Project 1: The Zero-Bloat 1B Parameter LLM Engine
* [ ] **Phase 1: C++ Host Foundation** (Row-major arrays, Tokenizer, CPU GEMM, GELU, Argmax, `<chrono>` stopwatches)
* [ ] **Phase 2: CUDA Hardware Step** (`nvcc` compiler, `cudaMalloc`, `cudaMemcpyAsync`, Pinned memory, Warp alignment)
* [ ] **Phase 3: Core Transforms & Parallel Math** (Coalesced 2D Grids, Warp Shuffles, Fused Kernels, Embedding Lookup)
* [ ] **Phase 4: Low-Memory Edge Design** (INT4/INT8 Quantization, Custom Bit-shifting, Sparse Matrices)

### ⚪ Project 2: Deterministic Fixed-Block Pool Allocator for Robotics
* [ ] Pre-allocate massive continuous chunks upfront to eliminate 20%+ OS system call overhead.
* [ ] Implement compile-time `alignas` operators to prevent CPU hardware cache line thrashing.
* [ ] Convert singly linked block trackers into lock-free lists via `std::atomic_compare_exchange_weak`.
* [ ] Ensure absolute zero memory fragmentation under intensive Valgrind testing profiles.

### ⚪ Project 3: Pure C++ CPU Software Rasterizer (3D Graphics Engine)
* [ ] Code raw geometric transformations, `Matrix4x4` projectors, and custom triangle vertex maps.
* [ ] Accelerate pixel evaluations using explicit SIMD instructions (`<immintrin.h>`).
* [ ] Build a manual Z-Buffer to handle spatial depth pixel-by-pixel.

### ⚪ Project 4: Embedded Real-Time Robotics Agent Integration (Capstone)
* [ ] Load the custom Software Rasterizer engine to map dynamic physical barriers inside a 3D arena.
* [ ] Pass matrix pointers directly from the Project 2 Allocator to Project 1's CUDA tensor layer.
* [ ] Program backpropagation calculus loops to train a robotic agent via local reward profiles.

### ⚪ Project 5: Custom Linux Command-Line Terminal Shell
* [ ] Program an infinite Read-Eval-Print Loop (REPL) parser splitting text boundaries.
* [ ] Implement low-level POSIX process duplication architecture via `fork()`, `execvp()`, and `waitpid()`.
* [ ] Prevent system resource leaks and zombie process accumulation using `sigaction()` via `SIGCHLD`.
* [ ] Build native support for environmental paths (`$PATH` parsing) to locate program binaries.
* [ ] Configure low-level I/O Redirection (`>`, `<`) and Inter-process Piping (`|`) using `dup2()` and `pipe()`.
* [ ] Mitigate process hangs by systematically managing pipe file descriptor closures (`close(pipefd)`).

---

## 📚 Essential Masterclass Study Material
* **Mechanics:** Andrej Karpathy's *"Neural Networks: Zero to Hero"* series (Focus on the raw backpropagation mechanics lecture).
* **Scaling:** Andrej Karpathy's *"Let's reproduce GPT-2 (124M)"* technical walkthrough.
* **GPU Engine:** CUDA-MODE deep-dives:
  * Lecture 3: Getting Started with CUDA
  * Lecture 4: Compute and Memory Arc

---

## 🛠️ Global Environment & Compilation Target
```bash
# General C++20 Target
g++ -O3 -std=c++20 -Wall -Wextra main.cpp -o engine

# NVIDIA CUDA Compiler Target
nvcc -O3 -arch=sm_80 kernels.cu main.cpp -o cuda_engine
```

## 📚 Time Required To Finish
* 7 years.
