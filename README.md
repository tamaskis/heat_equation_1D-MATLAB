# `diffusion1D`

Solves the one-dimensional diffusion equation (i.e. heat equation) for Neumann and Dirichlet type boundary conditions using three different methods (FTCS, BTCS, and CTCS (Crank-Nicolson)). Two different implementations of the FTCS method are also used: (1) the looped implementation and (2) the simultaneous implementation.


## Syntax

`[x,f,Fo] = diffusion1D(sol_method,D,L,N,IC,g_func,gType,h_func,hType,dt,tmax)`


## Description

`[x,f,Fo] = diffusion1D(sol_method,D,L,N,IC,g_func,gType,h_func,hType,dt,tmax)` returns the solution of the diffusion equation at time <img src="https://latex.codecogs.com/svg.latex?t_{\mathrm{max}}" title="t_{\mathrm{max}}" /> (as the vector `f`), as well as the spatial domain for the solution (`x`) an the discrete Fourier number (`Fo`).
- `sol_method` - solution method (`FTCS_looped` for looped FTCS, `FTCS_simultaneous` for simultaneous FTCS, `BTCS` for BTCS, and `CTCS` for CTCS (Crank-Nicolson))
- `D` - diffusivity
- `L` - domain length (in meters)
- `IC` - function handle for initial condition
- `g_func` - function handle for left boundary condition
- `gType` - type of boundary condition at left boundary (specify as `Dirichlet` or `Neumann`)
- `h_func` - function handle for right boundary condition
- `hType` - type of boundary condition at right boundary (specify as `Dirichlet` or `Neumann`)
- `dt` - time step (in seconds)
- `tmax` - solution end time (in seconds)
