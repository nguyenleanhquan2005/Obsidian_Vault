# Introduction to Calculus

Calculus is a branch of mathematics that studies continuous change. It consists of two main branches: differential calculus and integral calculus, which are connected by the fundamental theorem of calculus.

# Differential Calculus

## Derivatives

The derivative measures the rate at which a function changes. For a function f(x), the derivative is defined as:

$$ f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} $$

## Key Differentiation Rules

- **Power Rule:** If f(x) = x^n, then f'(x) = nx^(n-1)
- **Product Rule:** (fg)' = f'g + fg'
- **Quotient Rule:** (f/g)' = (f'g - fg')/g²
- **Chain Rule:** If h(x) = f(g(x)), then h'(x) = f'(g(x)) · g'(x)

## Applications of Derivatives

- Finding maximum and minimum values
- Analyzing motion and velocity
- Optimization problems
- Related rates

# Integral Calculus

## Integrals

Integration is the reverse process of differentiation. The definite integral represents the area under a curve:

$$ \int_a^b f(x) \, dx $$

## Key Integration Techniques

- **Substitution:** Used when the integrand contains a function and its derivative
- **Integration by Parts:** ∫u dv = uv - ∫v du
- **Partial Fractions:** Breaking rational functions into simpler fractions
- **Trigonometric Substitution:** For integrals involving √(a² - x²), √(a² + x²), or √(x² - a²)

## Applications of Integrals

- Calculating areas and volumes
- Finding arc length
- Work and energy problems
- Probability and statistics

# Fundamental Theorem of Calculus

The fundamental theorem connects differentiation and integration:

**Part 1:** If F(x) = ∫ₐˣ f(t) dt, then F'(x) = f(x)

**Part 2:** ∫ₐᵇ f(x) dx = F(b) - F(a), where F is an antiderivative of f

# Important Concepts

## Limits

Limits form the foundation of calculus, describing the behavior of functions as they approach specific values.

## Continuity

A function is continuous at a point if the limit exists and equals the function's value at that point.

## Series and Sequences

- Arithmetic and geometric series
- Taylor and Maclaurin series
- Convergence tests

# Multivariable Calculus

- Partial derivatives
- Multiple integrals
- Vector calculus
- Gradient, divergence, and curl

# Applications in Real World

- Physics: motion, forces, electricity, and magnetism
- Engineering: optimization and design
- Economics: marginal analysis and cost functions
- Biology: population dynamics and growth models
- Computer Science: algorithms and machine learning

### Outline: Calculus (high-level map)

1. [[**Precalculus foundations**]]
    - Functions and graphs (polynomials, rational, exponential, logarithmic, trig, inverse trig)
    - Transformations, composition, inverses
    - Coordinate geometry and basic modeling
2. **Function and Models**
    - Intuitive idea: approaching a value
    - Limit laws and algebraic techniModelsques
    - One-sided limits and limits at infinity
    - Continuity and types of discontinuities
    - The Squeeze Theorem
    - Formal definition of limit (epsilon–delta) (optional but important for rigor)
3. **Limits and Derivatives (differential calculus)**
    - Derivative as a limit (difference quotient)
    - Interpretations
        - Slope of tangent line
        - Instantaneous rate of change
        - Velocity and acceleration
    - Differentiation rules
        - Power, product, quotient, chain rules
        - Derivatives of trig, exponential, log, inverse trig functions
        - Implicit differentiation
        - Logarithmic differentiation
        - Higher-order derivatives
    - Linear approximation and differentials
    - Related rates
    - Optimization
        - Critical points
        - First and second derivative tests
        - Modeling constraints
    - Curve sketching and function analysis
        - Increasing/decreasing, concavity, inflection points
        - Asymptotes
    - L’Hôpital’s Rule and indeterminate forms
4. **Integrals (integral calculus)**
    - Antiderivatives and indefinite integrals
    - Definite integrals and Riemann sums
    - The Fundamental Theorem of Calculus (both parts)
    - Properties of definite integrals
    - Numerical integration (trapezoid rule, Simpson’s rule)
5.  Multiple Integrals
	- Double Integrals over Rectangles
	- Double integrals over General Regions
	- 




6. **Techniques of integration**
    - Substitution (u-substitution)
    - Integration by parts
    - Trigonometric integrals and identities
    - Trigonometric substitution
    - Partial fractions
    - Improper integrals
    - (Optional) Special functions and integrals without elementary antiderivatives
7. **Applications of integration**
    - Area between curves
    - Volume (disk/washer method, shells)
    - Arc length and surface area
    - Work, fluid force/pressure
    - Mass, center of mass, moments
    - Average value of a function
    - Differential equations (basic growth/decay models as an entry point)
8. **Sequences and series**
    - Sequences and convergence
    - Infinite series and convergence tests
        - Geometric, p-series
        - Comparison tests, ratio/root tests, alternating series test
    - Power series
    - Taylor and Maclaurin series
        - Error estimates and approximation
    - Fourier series (often later/optional)
9. **Parametric equations and polar coordinates**
    - Parametric curves and calculus with parameters
    - Polar coordinates and polar curves
    - Area in polar coordinates
10. **Multivariable calculus**
    - Functions of several variables and 3D geometry
    - Partial derivatives and interpretation
    - Gradients and directional derivatives
    - Optimization in multiple variables
        - Critical points
        - Lagrange multipliers (constraints)
    - Multiple integrals
        - Double and triple integrals
        - Change of variables and Jacobians
    - Vector fields
        - Line integrals
        - Surface integrals and flux
11. **Vector calculus and major theorems**
    - Divergence and curl
    - Green’s Theorem
    - Stokes’ Theorem
    - Divergence (Gauss) Theorem
    - Conservative fields and potential functions
12. **Differential equations (typical next step after single-variable calculus)**
    - First-order ODEs (separable, linear)
    - Second-order linear ODEs (basic forms)
    - Modeling: population, motion, circuits
    - Systems (intro)
    - Qualitative analysis (slope fields, stability)
13. **Theory, rigor, and “why calculus works” (more advanced/optional)**
    - Precise definitions (limits, continuity, derivative)
    - Mean Value Theorem and consequences
    - Uniform continuity and compactness ideas (in more advanced courses)
    - Error bounds and convergence concepts
14. **Common real-world application domains**
    - Physics (motion, fields, energy)
    - Engineering (design optimization, signals, fluids)
    - Economics (marginal analysis, optimization)
    - Biology (growth, diffusion, epidemics)
    - Computer science and data science (optimization, gradients, continuous approximations)

