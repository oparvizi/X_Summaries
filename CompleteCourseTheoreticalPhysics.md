Source: https://link.springer.com/book/10.1007/978-3-030-04360-5
## A Complete Course on Theoretical Physics From Classical Mechanics to Advanced Quantum Statistics:
1 Basics of Experience  
    
1.1 Vector Analysis

              a + b = b + a                  (a + b) + c = a + (b + c) .
   <img width="259" alt="image" src="https://user-images.githubusercontent.com/105786517/219346436-e8902029-8165-4fc5-8f28-c3f4341c07bb.png"><img width="257" alt="image" src="https://user-images.githubusercontent.com/105786517/219346543-9f63ba8a-9e6a-4204-9ea2-432e67e91505.png">    
The scalar product (inner product) a · b    
    
              a · b ≡ a b cos φab .                              -------------------------------------------
              a · b = b · a    and    a · b = 0 ⇐⇒ a ⊥ b or a = 0 or b = 0 .
 The vector product (outer product) a × b
     
              |a × b| = a b sin φab .                            -------------------------------------------
              a × b = −b × a , a × (b + c) = a × b + a × c ,
    and
               a × b = 0 ⇐⇒ a || b or a = 0 or b = 0 .
 Using a right-handed Cartesian coordinate system, we have
    
    ex × ey = ez (and cyclic permutations ey × ez = ex, ...) , and also ex × ex = 0, etc., whence
              a × b = ex (ay bz − az by) + ey (az bx − ax bz) + ez (ax by − ay bx) .
    This implies
              a × (b × c) = (c × b) × a = b c · a − c a · b .

    (This decomposition also follows without calculation because the product depends linearly upon its three factors, lies in the plane spanned by b and c, vanishes for b ∝ c, and points in the direction of b for c = a ⊥ b.) According to the last equation, every vector a can be decomposed into its component along a unit vector e and its component perpendicular to it:
              a = e e · a − e × (e × a) .
    In addition, it satisfies the Jacobi identity (note the cyclic permutation)
              a × (b × c) + b × (c × a) + c × (a × b) = 0 .       -------------------------------------------
    The scalar product of a vector with a vector product, viz.,
              a · (b × c) = b · (c × a) = c · (a × b) ,
    is called the (scalar) triple product of the three vectors. It is positive or negative, if a, b, and c form a right- or left-handed triad, respectively. Its value gives the volume of the parallelepiped with edges a, b, and c. In particular, ex · (ey × ez) = 1. 
1.1.3 Trajectories  
<img width="383" alt="image" src="https://user-images.githubusercontent.com/105786517/219352103-ddf672a9-7513-4960-8126-be5fafb5ebf9.png">
If a vector depends upon a parameter, then we speak of a vector function. The vector function a (t) is continuous at t0, if it tends to a (t0) for t → t0. With the same limit t → t0, the vector differential da and the first derivative da/dt is introduced.

    quantities may be formed for every Cartesian component
              d(a + b) = da + db                  d(αa) = α da + a dα 
              d(a · b) = a · db + b · da          d(a × b) = a × db − b × da .
     Here eT has the direction of v:         
              tangent vector eT ≡ dr/ds = v/v .
              path curvature κ ≡ |deT/ds|= |d^2r/d^s2|
              curvature radius R ≡ 1/κ
              normal vector eN ≡ R deT/ds = R d2r/ds2 .
	      binormal vector eB ≡ eT × eN
 <img width="388" alt="image" src="https://user-images.githubusercontent.com/105786517/219354406-8ec6f76c-d24c-485d-84cf-41aa2fc32f0b.png">
1.1.4 Vector Fields  
   If a vector is associated with each position, we speak of a vector field

	Instead of drawing a vector field with arrows at many positions, it is often visualized by a set of field lines: at every point of a field line the tangent  points in the direction of the vector field. Thus 
	      a || dr and a × dr = 0.
1.1.5 Gradient (Slope Density)  
   The gradient of a scalar function ψ(r) is the vector field 
   
   		grad ψ ≡ ∇ψ , with ∇ψ · dr ≡ dψ ≡ ψ(r + dr) − ψ(r) .
In Cartesian coordinates, we thus have

		∇ψ = ex ∂ψ/∂x + ey ∂ψ/∂y + ez ∂ψ/∂z = (ex ∂/∂x + ey ∂/∂y + ez ∂/∂z)ψ .
<img width="290" alt="image" src="https://user-images.githubusercontent.com/105786517/219357834-8ca1a104-9f66-45e3-bfe8-c898fdf46c98.png">
The gradient is also obtained as a limit of a vectorial integral:
<img width="385" alt="image" src="https://user-images.githubusercontent.com/105786517/219359867-ec9e55d5-95be-41a7-8d33-5d878dab0ef4.png"><img width="386" alt="image" src="https://user-images.githubusercontent.com/105786517/219359941-cf9ff654-2151-4154-988e-8595cd12b7dc.png">
1.1.6 Divergence (Source Density)  
While a vector field has been derived from a scalar field with the help of the gradient, the divergence associates a scalar field with a vector field:

		div a ≡ ∇ · a ≡ lim 1/V integral df · a .
For the same cube as in the last section, the right-hand expression yields
		
		1/dx dy dz [dy dz {ax (x+dx, y, z) −ax (x, y, z)}
			   +dz dx {ay(x, y+dy, z) −ay(x, y, z)}
			   +dx dy {az(x, y, z+dz) −az(x, y, z)}] = ∂ax/∂x+∂ay/∂y+∂az/∂z
scalar product between the vector operator ∇ and the vector a. With this we have also proven Gauss’s theorem			   
		
		integral dV ∇ · a = integral df · a 
The concept of a field-line tube:
<img width="392" alt="image" src="https://user-images.githubusercontent.com/105786517/219360202-a9ce95e4-2235-47af-8681-2afe25cebde6.png">      
1.1.7 Curl (Vortex Density)   















1.1.8 Rewriting Products. Laplace Operator   
1.1.9 Integral Theorems for Vector Expressions    
1.1.10 Delta Function    
1.1.11 Fourier Transform   
1.1.12 Calculation of a Vector Field from Its Sources and Curls      
1.1.13 Vector Fields at Interfaces                 
1.2 Coordinates               
1.2.1 Orthogonal Transformations and Euler Angles             
1.2.2 General Coordinates and Their Base Vectors           
1.2.3 Coordinate Transformations           
1.2.4 The Concept of a Tensor            
1.2.5 Gradient, Divergence, and Rotation in General Coordinates           
1.2.6 Tensor Extension, Christoffel Symbols             
1.2.7 Reformulation of Partial Differential Quotients           
1.3 Measurements and Errors            
1.3.1 Introduction               
1.3.2 Mean Value and Average Error            
1.3.3 Error Distribution                 
xv
1.3.4 Error Propagation               
1.3.5 Finite Measurement Series and Their Average Error             
1.3.6 Error Analysis                
1.3.7 Method of Least Squares                 
List of Symbols                 
Suggestions for Further Reading             
2 Classical Mechanics              
2.1 Basic Concepts                   
2.1.1 Force and Counter-Force             
2.1.2 Work and Potential Energy            
2.1.3 Constraints: Forces of Constraint, Virtual Displacements, and Principle of Virtual Work         
2.1.4 General Coordinates and Forces         
2.1.5 Lagrangian Multipliers and Lagrange Equations of the First Kind        
2.1.6 The Kepler Problem       
2.1.7 Summary: Basic Concepts         
2.2 Newtonian Mechanics         
2.2.1 Force-Free Motion       
2.2.2 Center-of-Mass Theorem        
2.2.3 Collision Laws            
2.2.4 Newton’s Second Law         
2.2.5 Conserved Quantities and Time Averages          
2.2.6 Planetary Motion as a Two-Body Problem,
and Gravitational Force       
2.2.7 Gravitational Acceleration      
2.2.8 Free-Fall, Thrust, and Atmospheric Drag      
2.2.9 Rigid Bodies       
2.2.10 Moment of Inertia     
2.2.11 Principal Axis Transformation     
2.2.12 Accelerated Reference Frames and Fictitious Forces      
2.2.13 Summary of Newtonian Mechanics       
2.3 Lagrangian Mechanics      
2.3.1 D’Alembert’s Principle        
2.3.2 Constraints         
2.3.3 Lagrange Equations of the Second Kind       
2.3.4 Velocity-Dependent Forces and Friction          
2.3.5 Conserved Quantities. Canonical and Mechanical Momentum       
xvi Contents
2.3.6 Physical Pendulum         
2.3.7 Damped Oscillation       
2.3.8 Forced Oscillation        
2.3.9 Coupled Oscillations and Normal Coordinates     
2.3.10 Time-Dependent Oscillator. Parametric Resonance      
2.3.11 Summary: Lagrangian Mechanics          
2.4 Hamiltonian Mechanics         
2.4.1 Hamilton Function and Hamiltonian Equations      
2.4.2 Poisson Brackets       
2.4.3 Canonical Transformations        
2.4.4 Infinitesimal Canonical Transformations. Liouville Equation         
2.4.5 Generating Functions        
2.4.6 Transformations to Moving Reference Frames. Perturbation Theory  
2.4.7 Hamilton–Jacobi Theory   
2.4.8 Integral Principles      
2.4.9 Motion in a Central Field       
2.4.10 Heavy Symmetrical Top and Spherical Pendulum       
2.4.11 Canonical Transformation of Time-Dependent Oscillators    
2.4.12 Summary: Hamiltonian Mechanics Problems       
List of Symbols  
References   
Suggestions for Textbooks and Further Reading         
3 Electromagnetism         
3.1 Electrostatics        
3.1.1 Overview of Electromagnetism   
3.1.2 Coulomb’s Law—Far or Near Action?         
3.1.3 Electrostatic Potential        
3.1.4 Dipoles         
3.1.5 Polarization and Displacement Field        
3.1.6 Field Equations in Electrostatics      
3.1.7 Problems in Electrostatics       
3.1.8 Energy of the Electrostatic Field      
3.1.9 Maxwell Stress Tensor in Electrostatics     
3.1.10 Summary: Electrostatics       
3.2 Stationary Currents and Magnetostatics        
3.2.1 Electric Current          
3.2.2 Ohm’s Law        
3.2.3 Lorentz Force       
Contents xvii
3.2.4 Magnetic Moments          
3.2.5 Magnetization         
3.2.6 Magnetic Fields                 
3.2.7 Basic Equations of Macroscopic Magnetostatics
with Stationary Currents            
3.2.8 Vector Potential       
3.2.9 Magnetic Interaction.       
3.2.10 Inductance        
3.2.11 Summary: Stationary Currents and Magnetostatics         
3.3 Electromagnetic Field        
3.3.1 Charge Conservation and Maxwell’s Displacement
Current         
3.3.2 Faraday Induction Law and Lenz’s Rule     
3.3.3 Maxwell’s Equations          
3.3.4 Time-Dependent Potentials       
3.3.5 Poynting’s Theorem       
3.3.6 Oscillating Circuits       
3.3.7 Momentum of the Radiation Field         
3.3.8 Propagation of Waves in Insulators       
3.3.9 Reflection and Diffraction at a Plane     
3.3.10 Propagation of Waves in Conductors         
3.3.11 Summary: Maxwell’s Equations       
3.4 Lorentz Invariance         
3.4.1 Velocity of Light in Vacuum            
3.4.2 Lorentz Transformation          
3.4.3 Four-Vectors            
3.4.4 Examples of Four-Vectors              
3.4.5 Conservation Laws           
3.4.6 Covariance of the Microscopic Maxwell Equations       
3.4.7 Covariance of the Macroscopic Maxwell Equations      
3.4.8 Transformation Behavior of Electromagnetic Fields     
3.4.9 Relativistic Dynamics of Free Particles     
3.4.10 Relativistic Dynamics with External Forces     
3.4.11 Energy–Momentum Stress Tensor           
3.4.12 Summary: Lorentz Invariance              
3.4.13 Supplement: Hamiltonian Formalism for Fields       
3.5 Radiation Fields         
3.5.1 Solutions of the Inhomogeneous Wave Equations   
3.5.2 Radiation Fields        
3.5.3 Radiation Energy         
3.5.4 Radiation Fields of Point Charges        
3.5.5 Radiation Fields of Oscillating Dipoles      
3.5.6 Radiation Power for Dipole, Braking, and Synchrotron
Radiation       
xviii Contents
3.5.7 Summary: Radiation Fields       
Problems   
List of Symbols        
References       
Suggestions for Textbooks and Further Reading      
4 Quantum Mechanics I.   
4.1 Wave–Particle Duality     
4.1.1 Heisenberg’s Uncertainty Relations       
4.1.2 Wave–Particle Dualism           
4.1.3 Probability Waves         
4.1.4 Pure States and Their Superposition (Superposition Principle)     
4.1.5 Hilbert Space (Four Axioms)       
4.1.6 Representation of Hilbert Space Vectors      
4.1.7 Improper Hilbert Vectors      
4.1.8 Summary: Wave–Particle Dualism        
4.2 Operators and Observables      
4.2.1 Linear and Anti-linear Operators       
4.2.2 Matrix Elements and Representation of Linear Operators.     
4.2.3 Associated Operators    
4.2.4 Eigenvalues and Eigenvectors     
4.2.5 Expansion in Terms of a Basis of Orthogonal Operators. 
4.2.6 Observables. Basic Assumptions    
4.2.7 Uncertainty   
4.2.8 Field Operators    
4.2.9 Phase Operators and Wave–Particle Dualism     
4.2.10 Doublets and Pauli Operators       
4.2.11 Density Operator. Pure States and Mixtures           
4.2.12 Space Inversion and Time Reversal          
4.2.13 Summary: Operators and Observables         
4.3 Correspondence Principle        
4.3.1 Commutation Relations      
4.3.2 Position and Momentum Representations.      
4.3.3 The Probability Amplitude hr j Pi             
4.3.4 Wave Functions           
4.3.5 Wigner Function         
4.3.6 Spin           
4.3.7 Correspondence Principle         
Contents xix
4.3.8 Angular Momentum Operator              
4.3.9 Spherical Harmonics           
4.3.10 Coupling of Angular Momenta         
4.3.11 Summary: Correspondence Principle       
4.4 Time Dependence          
4.4.1 Heisenberg Equation and the Ehrenfest Theorem    
4.4.2 Time Dependence: Heisenberg and Schrödinger Pictures     
4.4.3 Time Dependence of the Density Operator            
4.4.4 Time-Dependent Interaction and Dirac Picture          
4.4.5 Current Density       
4.4.6 Summary: Time Dependence        
4.5 Time-Independent Schrödinger Equation                   
4.5.1 Eigenvalue Equation for the Energy           
4.5.2 Reduction to Ordinary Differential Equations      
4.5.3 Free Particles and the Box Potential        
4.5.4 Harmonic Oscillations      
4.5.5 Hydrogen Atom       
4.5.6 Time-Independent Perturbation Theory          
4.5.7 Variational Method        
4.5.8 Level Splitting         
4.5.9 Summary: Time-Independent Schrödinger Equation          
4.6 Dissipation and Quantum Theory       
4.6.1 Perturbation Theory        
4.6.2 Coupling to the Environment        
4.6.3 Markov Approximation        
4.6.4 Deriving the Rate Equation and Fermi’s Golden Rule        
4.6.5 Rate Equation for Degeneracy. Transitions Between Multiplets       
4.6.6 Damped Linear Harmonic Oscillations     
4.6.7 Summary: Dissipation and Quantum Theory    
Problems       
List of Symbols     
References        
Suggestions for Textbooks and Further Reading       
5 Quantum Mechanics II        
5.1 Scattering Theory            
5.1.1 Introduction          
5.1.2 Basics             
5.1.3 Time Shift Operators in Perturbation Theory         
5.1.4 Time-Dependent Green Functions (Propagators).       
5.1.5 Energy-Dependent Green Functions (Propagators) and Resolvents.  
xx Contents
5.1.6 Representations of the Resolvents
and the Interactions           
5.1.7 Lippmann–Schwinger Equations        
5.1.8 Möller’s Wave Operators       
5.1.9 Scattering and Transition Operators         
5.1.10 The Wave Function hr j k iþ for Large Distances r       
5.1.11 Scattering Cross-Section            
5.1.12 Summary: Scattering Theory        
5.2 Two- and Three-Body Scattering Problems       
5.2.1 Two-Potential Formula of Gell-Mann and Goldberger           
5.2.2 Scattering Phases           
5.2.3 Scattering of Charged Particles          
5.2.4 Effective Hamilton Operator in the Feshbach Theory       
5.2.5 Separable Interactions and Resonances           
5.2.6 Breit–Wigner Formula       
5.2.7 Averaging over the Energy         
5.2.8 Special Features of Three-Body Problems            
5.2.9 The Method of Kazaks and Greider     
5.2.10 Faddeev Equations     
5.2.11 Summary: Two- and Three-Body Scattering Problems        
5.3 Many-Body Systems           
5.3.1 One- and Many-Body States        
5.3.2 Exchange Symmetry         
5.3.3 Symmetric and Antisymmetric States          
5.3.4 Creation and Annihilation Operators for Fermions      
5.3.5 Creation and Annihilation Operators for Bosons      
5.3.6 General Properties of Creation and Annihilation Operators     
5.3.7 The Two-Body System as an Example       
5.3.8 Representation of One-Particle Operators       
5.3.9 Representation of Two-Body Operators          
5.3.10 Time Dependence         
5.3.11 Wave–Particle Dualism          
5.3.12 Summary: Many-Body Systems          
5.4 Fermions                     
5.4.1 Fermi Gas in the Ground State              
5.4.2 Hartree–Fock Equations           
5.4.3 Rest Interaction and Pair Force           
5.4.4 Quasi-Particles in the BCS Formalism      
Contents xxi
5.4.5 Hartree–Fock–Bogoliubov Equations         
5.4.6 Hole States        
5.4.7 Summary: Fermions           
5.5 Photons        
5.5.1 Preparation for the Quantization of Electromagnetic Fields           
5.5.2 Quantization of Photons            
5.5.3 Glauber States                  
5.5.4 Quenched States           
5.5.5 Expansion in Terms of Glauber States              
5.5.6 Density Operator in the Glauber Basis              
5.5.7 Atom in a Light Field             
5.5.8 Summary: Photons           
5.6 Dirac Equation          
5.6.1 Relativistic Invariance     
5.6.2 Quantum Theory              
5.6.3 Dirac Matrices            
5.6.4 Representations of the Dirac Matrices    
5.6.5 Behavior of the Dirac Equation Under Lorentz Transformations          
5.6.6 Adjoint Spinors and Bilinear Covariants         
5.6.7 Space Inversion, Time Reversal, and Charge Conjugation          
5.6.8 Dirac Equation and Klein–Gordon Equation           
5.6.9 Energy Determination for Special Potentials              
5.6.10 Difficulties with the Dirac Theory       
List of Symbols          
References          
Suggestions for Textbooks and Further Reading        
6 Thermodynamics and Statistics         
6.1 Statistics            
6.1.1 Introduction           
6.1.2 Statistical Ensembles and the Notion of Probability        
6.1.3 Binomial Distribution             
6.1.4 Gauss and Poisson Distributions          
6.1.5 Correlations and Partial Systems       
6.1.6 Information Entropy            
6.1.7 Classical Statistics and Phase Space Cells       
6.1.8 Summary: Statistics            
6.2 Entropy Theorem         
6.2.1 Entropy Law and Rate Equation      
6.2.2 Irreversible Changes of State and Relaxation-Time Approximation          
xxii Contents
6.2.3 Liouville and Collision-Free Boltzmann Equation         
6.2.4 Boltzmann Equation      
6.2.5 Proof of the Entropy Law Using the Boltzmann Equation        
6.2.6 Molecular Motion and Diffusion            
6.2.7 Langevin Equation          
6.2.8 Generalized Langevin Equation and the Fluctuation–Dissipation Theorem       
6.2.9 Fokker–Planck Equation       
6.2.10 Summary: Entropy Law        
6.3 Equilibrium Distribution            
6.3.1 Maxwell Distribution     
6.3.2 Thermal Equilibrium         
6.3.3 Micro-canonical Ensemble       
6.3.4 Density of States in the Single-Particle Model    
6.3.5 Mean Values and Entropy Maximum           
6.3.6 Canonical and Grand Canonical Ensembles        
6.3.7 Exchange Equilibria        
6.3.8 Temperature, Pressure, and Chemical Potential        
6.3.9 Summary: Equilibrium Distributions         
6.4 General Theorems of Thermodynamics          
6.4.1 The Basic Relation of Thermodynamics           
6.4.2 Mechanical Work and Heat        
6.4.3 State Variables and Complete Differentials     
6.4.4 Thermodynamical Potentials and Legendre Transformations      
6.4.5 Maxwell’s Integrability Conditions and Thermal Coefficients       
6.4.6 Homogeneous Systems and the Gibbs–Duhem Relation.   
6.4.7 Phase Transitions and the Clausius–Clapeyron Equation    
6.4.8 Enthalpy and Free Energy as State Variables    
6.4.10 Summary: General Theorems of Thermodynamics       
6.5 Results for the Single-Particle Model      
6.5.1 Identical Particles and Symmetry Conditions       
6.5.2 Partition Functions in Quantum Statistics.       
6.5.3 Occupation of One-Particle States        
6.5.4 Ideal Gases       
6.5.5 Mixing Entropy and the Law of Mass Action      
6.5.6 Degenerate Fermi Gas and Conduction Electrons
in Metals      
Contents xxiii
6.5.7 Electromagnetic Radiation in a Cavity        
6.5.8 Lattice Vibrations      
6.5.9 Summary: Results for the Single-Particle Model         
6.6 Phase Transitions         
6.6.1 Van der Waals Equation      
6.6.2 Conclusions Regarding the van der Waals Equation    
6.6.3 Critical Behavior       
6.6.4 Paramagnetism     
6.6.5 Ferromagnetism    
6.6.6 Bose–Einstein Condensation   
6.6.7 Summary: Phase Transitions      
Problems        
List of Symbols      
References     
Suggestions for Textbooks and Further Reading     
Appendix A: Important Constants   
