# Amorphous-Anamorphic-Base-Modulus
Amorphous/Anamorphic Base/Modulus



Amorphous Mathematics Library
![alt text](https://img.shields.io/badge/License-MIT-yellow.svg)

![alt text](https://img.shields.io/badge/python-3.7+-blue.svg)
The Amorphous Mathematics Library is a unique Python library that implements amorphous and anamorphous arithmetic. It introduces controlled fluidity, variability, and unpredictability into standard mathematical functions, transforming them into powerful tools for creative coding, simulation, and security applications.
This library moves beyond deterministic calculations to provide operations that are mathematically coherent yet organically variable, making them ideal for generating complex, non-linear, and natural-looking patterns.
Core Concepts
Amorphous Operations: These are variations of traditional functions (like log or modulus) that incorporate a controlled amount of randomness. For example, amorphous_base calculates a logarithm where the base itself fluctuates around a nominal value.
Anamorphous Operations: These are inverse-like transformations that take an amorphous result and reconstruct a value, but with additional, non-linear distortion. They are excellent for creating complex, hard-to-predict data mappings.
Fluidity: The key parameter, typically ranging from 0.0 (no randomness, standard behavior) to 1.0 (maximum randomness), that controls the degree of variation and unpredictability in all amorphous operations.
Key Features
Fluid Mathematical Operations: amorphous_base and amorphous_modulus functions with adjustable fluidity.
Complex Non-linear Transformations: anamorphous_base and anamorphous_modulus for distortion and reconstruction.
High-Level API: A AmorphousFunctionSuite for easy access, batch processing, and state management.
Reproducible Randomness: Use a seed to get consistent results for testing and deterministic generation.
Operation History & Statistics: Track all operations and get statistical summaries of the results.
Pure Python: No complex dependencies outside of numpy.
Installation
Currently, the library is provided as a single Python file. To use it in your project, simply save the library code as amorphous_math.py in your project directory.
You will also need numpy and matplotlib (for the examples):
Generated bash
pip install numpy matplotlib
Use code with caution.
Bash
Quick Start
The easiest way to get started is by using the direct, stateless functions. Let's compare a standard logarithm with its amorphous counterpart.
Generated python
import numpy as np
from amorphous_math import amorphous_base

# --- Standard Calculation ---
value = 100
base = 10
standard_result = np.log(value) / np.log(base)
print(f"Standard log₁₀(100) = {standard_result:.4f}")
# Output: Standard log₁₀(100) = 2.0000

# --- Amorphous Calculation ---
# Let's run it a few times to see the variation
print("\nAmorphous log₁₀(100) with fluidity=0.2:")
for i in range(3):
    amorphous_result = amorphous_base(value, base, fluidity=0.2)
    print(f"  Run {i+1}: {amorphous_result:.4f}")

# --- Reproducible Amorphous Calculation ---
result1 = amorphous_base(value, base, fluidity=0.2, seed=42)
result2 = amorphous_base(value, base, fluidity=0.2, seed=42)
print(f"\nWith a seed=42, the result is always: {result1:.4f}")
print(f"Running again with the same seed: {result2:.4f}")
Use code with caution.
Python
Applications & Examples
This library is highly versatile. The included examples.py file demonstrates several powerful use cases.
1. Generative Art
The organic, non-repeating nature of amorphous functions makes them perfect for generative art. By driving parameters like angle, step size, and color with amorphous operations, you can create beautiful, complex visual patterns.
Example Output from examples.py:
2. Scientific Simulation
Model natural phenomena that have inherent randomness.
Brownian Motion: Simulate random particle paths using amorphous_modulus to generate unpredictable steps.
Population Dynamics: Model population growth with chaotic environmental factors driven by anamorphous_base.
Population Dynamics Plot from examples.py:
3. Cryptography & Security
The non-linear and stateful properties can be used to create simple cryptographic primitives.
Key Schedule Generation: Create a sequence of round keys where each key is a complex, non-linear transformation of the previous one.
Data Obfuscation: Transform data in a way that is difficult to reverse-engineer, as identical inputs can produce different outputs depending on the operator's internal state.
Generated python
from amorphous_math import AmorphousArithmetic

# Obfuscating the same data twice yields different results
# due to the internal state of the random number generator.
crypto = AmorphousCrypto(seed=101)
original_data = [72, 101, 108, 108, 111] # "Hello"

obfuscated_1 = crypto.obfuscate_data(original_data)
obfuscated_2 = crypto.obfuscate_data(original_data)

print(f"Original:   {original_data}")
print(f"Obfuscated 1: {obfuscated_1}")
print(f"Obfuscated 2: {obfuscated_2}")
# Note that Obfuscated 1 and 2 are different!
Use code with caution.
Python
API Reference
Core Classes
AmorphousArithmetic(config=None, seed=None): The main class for performing stateful amorphous operations. Each call updates the internal random state.
AmorphousFunctionSuite(config=None, seed=None): A high-level wrapper around AmorphousArithmetic that provides convenient methods for batch processing and statistics.
AmorphousConfig(...): A configuration object to customize default fluidity, precision, etc.
Direct Functions
For simple, one-off calculations.
amorphous_base(value, base, fluidity, seed=None)
amorphous_modulus(dividend, divisor, fluidity, seed=None)
anamorphous_base(value, base, fluidity, distortion, seed=None)
anamorphous_modulus(dividend, divisor, fluidity, reconstruction, seed=None)
Author
Shaun Paul
License
This project is licensed under the MIT License. See the LICENSE file for details.
Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to contribute.
