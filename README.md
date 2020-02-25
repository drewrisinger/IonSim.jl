# IonSim.jl 

A simple tool, built on top of [QuantumOptics.jl](https://qojulia.org/), for simulating the dynamics of a configuration of 
trapped ions interacting with laser light.

**IonSim.jl** primarily performs two jobs
1. Keeps track of the physical parameters necessary for describing the system.
2. Using these parameters, constructs a function that quickly computes the system's Hamiltonian as a function of time. 

The functional form of the Hamiltonian can then be used as input to any of the solvers implemented in 
[`QuantumOptics.timeevolution`](https://qojulia.org/documentation/timeevolution/timeevolution/). For more information see:

+ Main code: [https://github.com/HaeffnerLab/IonSim.jl/tree/master/src](https://github.com/HaeffnerLab/IonSim.jl/tree/master/src)
+ Documentation: [https://github.com/HaeffnerLab/IonSim.jl/tree/master/doc](https://github.com/HaeffnerLab/IonSim.jl/tree/master/doc)
+ Examples: [https://github.com/HaeffnerLab/IonSim.jl/tree/master/examples](https://github.com/HaeffnerLab/IonSim.jl/tree/master/examples)
 
## Installation

### Installing [Julia](https://julialang.org/)
[Platform specific instructions found here](https://julialang.org/downloads/)

### Installing IonSim

Once Julia has been installed, open a terminal session and begin a 
[Julia REPL](https://docs.julialang.org/en/v1/stdlib/REPL/#The-Julia-REPL-1) with:

```
$ julia
```

(*If using Windows it's easier to start a REPL with the julia executable available after 
installation.*)


And then enter the following commands:

```julia
julia> using Pkg

julia> Pkg.add(PackageSpec(url="https://github.com/HaeffnerLab/IonSim.jl.git"))
```

You'll also need to download the QuantumOptics package:

```julia
julia> Pkg.add("QuantumOptics")
```

And will probably want to add Jupyter compatability by downloading IJulia:

```julia
julia> Pkg.add("IJulia")
```

after which you'll have the option to start a Julia kernel from Jupyter notebook.
