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
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219373225-9c7d4438-fd4b-4338-a05a-5b5deddd3bca.png">         
1.1.8 Rewriting Products. Laplace Operator     

	∇(φ ψ) = φ ∇ψ + ψ ∇φ ,
	∇ · (ψ a) = ψ ∇ · a + a · ∇ψ ,
	∇ × (ψ a) = ψ ∇ × a − a × ∇ψ ,
	∇ · (a × b) = b · (∇ × a) − a · (∇ × b) ,
	∇ × (a × b) = (b · ∇) a − b (∇ · a) − (a · ∇) b + a (∇ · b) ,
	∇ (a · b) = (b · ∇) a + b × (∇ × a) + (a · ∇) b + a × (∇ × b) .
1.1.9 Integral Theorems for Vector Expressions     






1.1.10 Delta Function    
<img width="385" alt="image" src="https://user-images.githubusercontent.com/105786517/219375011-185f7f69-ff48-4922-892f-003e21a8ac07.png">       
1.1.11 Fourier Transform      
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219375256-add49afb-4ccd-4f4c-b145-da76443af91c.png">      
1.1.12 Calculation of a Vector Field from Its Sources and Curls      
1.1.13 Vector Fields at Interfaces   
<img width="280" alt="image" src="https://user-images.githubusercontent.com/105786517/219375433-815dd942-f128-49ac-a41f-690ab08ffd34.png">        
1.2 Coordinates     
1.2.1 Orthogonal Transformations and Euler Angles    
<img width="296" alt="image" src="https://user-images.githubusercontent.com/105786517/219375525-f5208eeb-7ea3-4889-8a61-cbf5b2935489.png">            
1.2.2 General Coordinates and Their Base Vectors    
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219375840-3114ebd4-f569-4ad0-b262-08e36f15f837.png">            
1.2.3 Coordinate Transformations           
1.2.4 The Concept of a Tensor            
1.2.5 Gradient, Divergence, and Rotation in General Coordinates   
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219375969-04d05b4a-e2df-44c0-aaac-3878dea1baaa.png"><img width="291" alt="image" src="https://user-images.githubusercontent.com/105786517/219376142-928d3cb0-245e-4b5b-b414-ea4b873df431.png">        
1.2.6 Tensor Extension, Christoffel Symbols             
1.2.7 Reformulation of Partial Differential Quotients           
1.3 Measurements and Errors            
1.3.1 Introduction   
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219376507-632afbde-e9fc-41eb-9b5b-b284819871f2.png">      
1.3.2 Mean Value and Average Error            
1.3.3 Error Distribution    
<img width="290" alt="image" src="https://user-images.githubusercontent.com/105786517/219376694-635f8dbc-47e5-4c14-9bb7-05a69427d9a9.png">       
1.3.4 Error Propagation               
1.3.5 Finite Measurement Series and Their Average Error             
1.3.6 Error Analysis    
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219377107-cad30180-ada2-4533-b8d2-e22419bba237.png">       
1.3.7 Method of Least Squares                 
List of Symbols                 
Suggestions for Further Reading             
2 Classical Mechanics              
2.1 Basic Concepts                   
2.1.1 Force and Counter-Force   
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219377287-e15118be-989e-4798-8219-8b87ce2d5846.png">        
2.1.2 Work and Potential Energy            
2.1.3 Constraints: Forces of Constraint, Virtual Displacements, and Principle of Virtual Work   
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219377392-8ee18422-9e96-4337-b182-38231ef5d427.png">          
2.1.4 General Coordinates and Forces         
2.1.5 Lagrangian Multipliers and Lagrange Equations of the First Kind        
2.1.6 The Kepler Problem    
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219377554-4857dd29-7f38-4b8d-9a72-ae3ba3f38847.png"><img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219377769-f2a32fb6-4363-43c4-ac83-d7f97f1d8ad9.png"><img width="290" alt="image" src="https://user-images.githubusercontent.com/105786517/219377985-b6bbea20-0c6f-46c8-9962-ae2712e3ebbc.png"><img width="291" alt="image" src="https://user-images.githubusercontent.com/105786517/219378061-fcd99cc1-0b81-42ec-b6ad-ac936adf2707.png">          
2.1.7 Summary: Basic Concepts         
2.2 Newtonian Mechanics         
2.2.1 Force-Free Motion       
2.2.2 Center-of-Mass Theorem    
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219378268-922250df-187c-480e-841d-15ca84b2cb32.png">        
2.2.3 Collision Laws    
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219378452-f3f2251d-21d8-43be-94b8-8878fc909007.png"><img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219378578-c7796738-3f79-4693-b93c-be1cbbe21308.png">          
2.2.4 Newton’s Second Law         
2.2.5 Conserved Quantities and Time Averages          
2.2.6 Planetary Motion as a Two-Body Problem, and Gravitational Force         
2.2.7 Gravitational Acceleration   
<img width="296" alt="image" src="https://user-images.githubusercontent.com/105786517/219378726-f5bb6cda-57e4-4efd-9cb2-2a06f36eaa3f.png">           
2.2.8 Free-Fall, Thrust, and Atmospheric Drag    
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219378897-a5d4c0a6-5fe1-4fc6-900d-3d0ebfa651a9.png">        
2.2.9 Rigid Bodies       
2.2.10 Moment of Inertia     
2.2.11 Principal Axis Transformation    
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219378989-e2ecc713-8cd1-4106-8082-88ddc9cc948d.png"><img width="294" alt="image" src="https://user-images.githubusercontent.com/105786517/219379107-7cadf69b-b9e0-442c-9fab-952e3fdfd25d.png">         
2.2.12 Accelerated Reference Frames and Fictitious Forces   
<img width="294" alt="image" src="https://user-images.githubusercontent.com/105786517/219379227-2416adc3-28b4-43da-bb1e-c5636cb06caf.png">            
2.2.13 Summary of Newtonian Mechanics       
2.3 Lagrangian Mechanics      
2.3.1 D’Alembert’s Principle        
2.3.2 Constraints         
2.3.3 Lagrange Equations of the Second Kind       
2.3.4 Velocity-Dependent Forces and Friction          
2.3.5 Conserved Quantities. Canonical and Mechanical Momentum       
xvi Contents
2.3.6 Physical Pendulum    
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219379381-994fa981-96d9-49d5-bc7d-401a4afd5285.png"><img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219379566-018bc3a5-910b-4887-b54b-d29ad9c8eeb8.png"><img width="296" alt="image" src="https://user-images.githubusercontent.com/105786517/219379703-d8e214cb-ef36-4e7b-a089-16de4aaacfc9.png"><img width="290" alt="image" src="https://user-images.githubusercontent.com/105786517/219379764-c213a248-61f4-4a6d-a5ae-c61f03737325.png"><img width="290" alt="image" src="https://user-images.githubusercontent.com/105786517/219379846-71dfbe0a-3c08-4fd8-89ee-effe5473aaec.png">      
2.3.7 Damped Oscillation    
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219380017-27aa2a58-8e43-4fac-8c0d-c54b00d3cb90.png"><img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219380115-37a35082-73a7-4f1b-a87e-b99ae59b2e3c.png">          
2.3.8 Forced Oscillation      
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219380219-814a5321-2be6-41eb-9a78-fabdf97e945c.png"><img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219380299-ee41c3bf-c04e-4ddf-8f10-dbdd0f6baa3a.png">        
2.3.9 Coupled Oscillations and Normal Coordinates    
<img width="294" alt="image" src="https://user-images.githubusercontent.com/105786517/219380423-4189cb0b-0039-40cc-9165-482bc8bf5214.png">     
2.3.10 Time-Dependent Oscillator. Parametric Resonance    
<img width="290" alt="image" src="https://user-images.githubusercontent.com/105786517/219380643-dac7651b-6e2a-4d47-a8ce-28af8e879e27.png"><img width="298" alt="image" src="https://user-images.githubusercontent.com/105786517/219380705-e3fdcad2-ae3c-4c19-a05a-c3eb2afadfd6.png">       
2.3.11 Summary: Lagrangian Mechanics          
2.4 Hamiltonian Mechanics    
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219380827-1762a6a5-274a-4369-94d2-5d5aa6aac4c0.png">       
2.4.1 Hamilton Function and Hamiltonian Equations      
2.4.2 Poisson Brackets       
2.4.3 Canonical Transformations        
2.4.4 Infinitesimal Canonical Transformations. Liouville Equation         
2.4.5 Generating Functions        
2.4.6 Transformations to Moving Reference Frames. Perturbation Theory  
2.4.7 Hamilton–Jacobi Theory   
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219381022-b546b53c-d7b9-40c7-873e-fdeee9d1f442.png">         
2.4.8 Integral Principles     
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219381210-7bf8d261-3d0f-4e0b-ab1d-b3f09fe373e8.png">           
2.4.9 Motion in a Central Field       
2.4.10 Heavy Symmetrical Top and Spherical Pendulum   
<img width="291" alt="image" src="https://user-images.githubusercontent.com/105786517/219381339-8007ec5a-30e6-4611-ad9f-523447971c7d.png"><img width="291" alt="image" src="https://user-images.githubusercontent.com/105786517/219381516-6bfca226-b649-4f68-92f5-c7822afd5e4b.png"><img width="296" alt="image" src="https://user-images.githubusercontent.com/105786517/219381576-e3ddac67-44d8-4cfa-8ab0-b037d76f6079.png">          
2.4.11 Canonical Transformation of Time-Dependent Oscillators    
<img width="296" alt="image" src="https://user-images.githubusercontent.com/105786517/219381658-bff16eb3-b0d5-4926-9676-519332a5c660.png">
2.4.12 Summary: Hamiltonian Mechanics 
Problems       
List of Symbols  
References   
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219381805-957cb17d-8205-4cca-9245-6b8bdd873250.png"><img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219381994-11cd5b56-b033-43fb-8704-c166b85ac87f.png"><img width="291" alt="image" src="https://user-images.githubusercontent.com/105786517/219382112-18b34ff3-2bb9-412e-989b-57ea4e75e1a7.png"><img width="294" alt="image" src="https://user-images.githubusercontent.com/105786517/219382175-193c48a0-8b9b-474c-a52f-5252640715a9.png"><img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219382230-e438b599-b2fc-4969-b688-f942f36bb94f.png"><img width="290" alt="image" src="https://user-images.githubusercontent.com/105786517/219382271-57870f65-82d9-4086-badb-561d4dc18b99.png">                   
Suggestions for Textbooks and Further Reading         
3 Electromagnetism         
3.1 Electrostatics        
3.1.1 Overview of Electromagnetism   
3.1.2 Coulomb’s Law—Far or Near Action?   
<img width="291" alt="image" src="https://user-images.githubusercontent.com/105786517/219382532-8745823e-b0bc-4a0b-9739-4a4c7fc5ea1b.png">      
3.1.3 Electrostatic Potential   
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219382628-409330c8-e3aa-4e61-bad5-b8fb1fed10f4.png">        
3.1.4 Dipoles   
<img width="294" alt="image" src="https://user-images.githubusercontent.com/105786517/219382715-eecc8f94-acca-406b-9b10-986f41154c8f.png"><img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219382796-dce775a7-2d41-433c-b86c-2bb79e254eca.png">          
3.1.5 Polarization and Displacement Field        
3.1.6 Field Equations in Electrostatics   
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219382895-38217bba-cf83-4be3-a02a-199ee3209467.png">       
3.1.7 Problems in Electrostatics       
3.1.8 Energy of the Electrostatic Field      
3.1.9 Maxwell Stress Tensor in Electrostatics    
<img width="301" alt="image" src="https://user-images.githubusercontent.com/105786517/219383006-bb8fbb89-43f5-456c-a2d9-6dd5d7956aef.png">           
3.1.10 Summary: Electrostatics       
3.2 Stationary Currents and Magnetostatics        
3.2.1 Electric Current          
3.2.2 Ohm’s Law    
<img width="281" alt="image" src="https://user-images.githubusercontent.com/105786517/219383144-9d307003-a248-4457-b53a-9ee596b5d2cb.png">       
3.2.3 Lorentz Force       
Contents xvii
3.2.4 Magnetic Moments          
3.2.5 Magnetization     
<img width="294" alt="image" src="https://user-images.githubusercontent.com/105786517/219383267-9ceed3be-6097-4989-a70c-63eccf1a63c5.png">         
3.2.6 Magnetic Fields      
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219383384-ee690d26-3555-4d5c-9cbb-1e950efe8734.png">          
3.2.7 Basic Equations of Macroscopic Magnetostatics with Stationary Currents   
<img width="290" alt="image" src="https://user-images.githubusercontent.com/105786517/219383512-9dbba6a5-724a-4701-b9ba-6d455dbf2154.png">     
3.2.8 Vector Potential       
3.2.9 Magnetic Interaction.       
<img width="298" alt="image" src="https://user-images.githubusercontent.com/105786517/219383640-24517a93-3ad9-4553-89d4-36e73f028cb9.png">          
3.2.10 Inductance        
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219383840-8aa5eccc-faa6-4570-8ebf-913f9b6e71c2.png"><img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219383875-2fa0bd3a-e2f8-4b62-8e84-1cdb203120fe.png">      
3.2.11 Summary: Stationary Currents and Magnetostatics         
3.3 Electromagnetic Field        
3.3.1 Charge Conservation and Maxwell’s Displacement
Current         
3.3.2 Faraday Induction Law and Lenz’s Rule   
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219384021-49794224-55b5-48e2-a56c-ac7cd46b820f.png">       
3.3.3 Maxwell’s Equations          
3.3.4 Time-Dependent Potentials       
3.3.5 Poynting’s Theorem   
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219384189-5ba5b885-3dc7-4f49-bd65-b3e11253292f.png">       
3.3.6 Oscillating Circuits       
<img width="274" alt="image" src="https://user-images.githubusercontent.com/105786517/219384297-ac229711-68eb-465a-a508-c49d763d2643.png">       
3.3.7 Momentum of the Radiation Field         
3.3.8 Propagation of Waves in Insulators   
<img width="296" alt="image" src="https://user-images.githubusercontent.com/105786517/219384463-e794c8f3-4106-4e0d-91df-151e7109c17d.png">          
3.3.9 Reflection and Diffraction at a Plane     
<img width="298" alt="image" src="https://user-images.githubusercontent.com/105786517/219384644-f32cb829-d5d2-4894-b768-3338b28a7163.png"><img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219384786-37c2a847-607c-48b7-a24a-a35137a34161.png">       
3.3.10 Propagation of Waves in Conductors    
<img width="294" alt="image" src="https://user-images.githubusercontent.com/105786517/219384924-fe97dd90-57af-40a8-8961-5182359e1bd3.png">       
3.3.11 Summary: Maxwell’s Equations       
3.4 Lorentz Invariance         
3.4.1 Velocity of Light in Vacuum            
3.4.2 Lorentz Transformation   
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219385068-33bb24ce-a4fd-423b-acc0-d3257edee19b.png"><img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219385160-de2bbed5-5569-4794-aeec-c8a0ffde4b25.png">       
3.4.3 Four-Vectors    
3.4.4 Examples of Four-Vectors   
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219385358-2a8e378b-4fe9-4225-81d4-8c4df2fcd96e.png"><img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219385476-1a8694ca-819f-4230-bd7d-7931642f969e.png">    
3.4.5 Conservation Laws     
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219385856-2dbb4f22-3ba1-48c2-84e9-faa8029c2060.png">      
3.4.6 Covariance of the Microscopic Maxwell Equations       
3.4.7 Covariance of the Macroscopic Maxwell Equations      
3.4.8 Transformation Behavior of Electromagnetic Fields     
3.4.9 Relativistic Dynamics of Free Particles   
<img width="292" alt="image" src="https://user-images.githubusercontent.com/105786517/219386002-97487437-cf23-4623-aeb4-19a9ed132985.png">       
3.4.10 Relativistic Dynamics with External Forces     
3.4.11 Energy–Momentum Stress Tensor           
3.4.12 Summary: Lorentz Invariance              
3.4.13 Supplement: Hamiltonian Formalism for Fields       
3.5 Radiation Fields     
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219386173-b118488e-4dea-4179-942d-e4449723dddb.png">       
3.5.1 Solutions of the Inhomogeneous Wave Equations   
3.5.2 Radiation Fields        
3.5.3 Radiation Energy         
3.5.4 Radiation Fields of Point Charges        
<img width="299" alt="image" src="https://user-images.githubusercontent.com/105786517/219386293-370cf2cd-d306-440d-8400-56754b4a6421.png">       
3.5.5 Radiation Fields of Oscillating Dipoles      
3.5.6 Radiation Power for Dipole, Braking, and Synchrotron Radiation  
<img width="299" alt="image" src="https://user-images.githubusercontent.com/105786517/219386449-ee63c888-92fd-46f8-bbfb-2a314370e50b.png"><img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219386582-a8fe3032-6767-4f51-a494-ab7ca9200287.png"><img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219386657-f632e259-eac6-4d75-90bd-5dcbc032378c.png">         
3.5.7 Summary: Radiation Fields Problems   
4 Quantum Mechanics I.   
4.1 Wave–Particle Duality     
4.1.1 Heisenberg’s Uncertainty Relations       
4.1.2 Wave–Particle Dualism           
4.1.3 Probability Waves    
<img width="293" alt="image" src="https://user-images.githubusercontent.com/105786517/219387103-ca9edd08-e85b-4aaa-b996-cfac5c1d6662.png">      
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
<img width="295" alt="image" src="https://user-images.githubusercontent.com/105786517/219387537-c2e83299-3ef6-43b9-8b38-3f8e4d6b1a04.png">         
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
