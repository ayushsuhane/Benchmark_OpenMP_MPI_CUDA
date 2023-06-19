# Benchmark_OpenMP_MPI_CUDA


This project aims to benchmark the performance of different parallel implementations, i.e. OpenMP, MPI and GPU-acceleration using CUDA. Here, we solve the Laplace equation for fixed boundary conditions. The analytical solution for the simplified 2D square geometry is also known and can be used to verify the implementations. Google Collab provides free access to GPU, and therefore, it is chosen as the platform to benchmark different parallel implementations. The notebook includes the details, and the conclusions are summarized below. 

# Conclusions

- For same setup of Google Collab, GPU provides a speedup of 2x from OpenMPI with 4 threads, and 1.5x from MPI implementation with 4 procs. 
- Huge difference in execution time between laptop and google collab, but the scaling is consistent between OpenMP and MPI, e.g. OpenMP (on average) takes 11 s to finish with 4 threads on GoogleCollab and 2.3 s on my laptop, similarly MPI takes 7 s wit 4 procs on GoogleCollab and 1.37 s on my laptop. Donot have GPU on laptop, and cannot benchmark GoogleCollab with desktop.
- GPU acceleration is not optimized with respect to architecture but still provides a speedup.

# Further improvements

- Individual implementations needs to be further optimized for better performance.
- Have to check: How does hybrid (OpenMP + MPI) perform in comparison to GPU?
