# NN-based-Control-Stability-Analysis

Neural Network-based Control Stability Analysis for Caputo Fractional-order Autonomous Systems
.
Numerical simulations on stabilizing two Caputo Fractional-order systems are presented here, namely the Fractional Van der Pol Oscillator and the Fractional Lotka-Volterra System.
.
**(codes will soon be uploaded)**
.
The proposed method uses a neural network to generate a candidate Lyapunov function for a Caputo fractional-order nonlinear system. The algorithm starts with a one-hidden-layer neural network model that is initialized with a LQR control gain matrix. The neural network then receives a list of random state values and returns a list of values for the Lyapunov function and a gain matrix. If the Lyapunov candidate function satisfies the falsification conditions, then the algorithm terminates, and the current Lyapunov function is considered valid. If not, terms needed for the calculation of loss are computed by a numerical solver, and the tunable parameters of the model are updated through gradient descent. The algorithm then continues to iterate, generating counterexamples by an SMT solver until the falsification conditions are satisfied. The overall framework of the method is demonstrated in Figure 1 of the paper, and Algorithm 2 in the methodology section provides a more detailed explanation of the main algorithm used.
.
.
<div align=center>
<h2>Fractional Van der Pol Oscillator
</div>
.
The Van der Pol Oscillator is a rich non-linear oscillator used to describe the oscillation of a transistor in a circuit. It was first introduced in 1920 by Balthazar Van der Pol. 
  
.<div align=center>
<img src="https://github.com/user-attachments/assets/7b684e54-ed17-4494-a700-ca641098de25"/>
</div>
.
  
<div align=center>
<h2>Fractional Lotka-Volterra System
</div>
The fractional-order Lotka-Volterra System describes the dynamics of biological systems in which two species interact, typically a predator and a prey. Each state equation represents the rate of change in the population of one species based on both its own population and the population of the other species.
.<div align=center>
<img src="https://github.com/user-attachments/assets/7547f5d2-07d5-4b61-951d-07214e2c15a5"/>
</div>
