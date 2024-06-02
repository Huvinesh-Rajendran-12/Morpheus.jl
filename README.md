# Morpheus.jl

[Build Status

Morpheus.jl is a Julia library for numerical computation, similar to PyTorch in Python. It provides a fundamental data structure called Axion for efficient manipulation of scalar values while tracking additional computational information.

## Installation

To use Morpheus.jl, you need to have Julia installed on your system. You can install it using the Julia package manager:

```julia
using Pkg
Pkg.add("Morpheus")
```

## Usage

### Importing Morpheus

```julia
using Morpheus
```

### Axion

Axion is the fundamental data structure used in Morpheus.jl for numerical computation. It is similar to a Tensor in PyTorch but supports only scalar values at the moment. Axion allows you to efficiently manipulate data and track additional computational information.

An Axion has the following properties:

- `data`: the numerical value
- `grad`: the gradient of the value
- `_children`: a tuple of child Axions
- `_op`: the operation that produced the Axion
- `_backward`: a function for backpropagation

Here's an example of creating and manipulating Axions:

```julia
x = Axion(2.0)
# output: Axion(data=2.0, grad=0.0, dtype=Float32)
# note: the default value type is Float32

x.data
# output: 2.0f0

x.grad
# output: 0.0f0

y = Axion(3.0)
z = x + y
# output: Axion(data=5.0, grad=0.0, dtype=Float32)

t = x * y
# output: Axion(data=6.0, grad=0.0, dtype=Float32)
```

Morpheus.jl provides various operations for working with Axions, such as addition, multiplication, and more. You can use these operations to build and train machine learning models.

For more detailed information and examples, please refer to the [Morpheus.jl documentation](https://github.com/Huvinesh-Rajendran-12/Morpheus.jl)[1][2].

Citations:
[1] https://github.com/Huvinesh-Rajendran-12/Morpheus.jl/actions/workflows/CI.yml/badge.svg?branch=main
[2] https://github.com/Huvinesh-Rajendran-12/Micrograd.jl/actions/workflows/CI.yml?query=branch%3Amain
[3] https://docs.nvidia.com/morpheus/_modules/morpheus.html
[4] https://docs.morpheusdata.com/en/latest/library/library.html
[5] https://docs.morpheusdata.com/en/6.2.0/library/library.html
[6] https://wwwapps.grassvalley.com/docs/Manuals/playout/morpheus/Morpheus_Engineers_Manual_v4.6_Rev2.pdf
[7] https://www.soniccouture.com/files/pdf/SC-Morpheus-User-Guide.pdf
