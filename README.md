This is the repositary for problem from Kharkiv Quantum Winter School 2025. Below its formulation:

In the first tutorials we have given additional problems with hardware noise. Hardware noise is simulated by some noise model, which characterizes the noise of the gates execution. The noise influences the final results of measurements. Noise mitigation is a set of strategies aimed at cleaning the results of measurements from the noise effects.

In this problem, we employ the simplest strategy of noise mitigation - the zero noise extrapolation (ZNE). Its idea is quite simple: usually we can not decrease the noise below a certain threshold, but we can artificially increase it. ZNE executes the same circuit with several different magnitudes of noise (where noise is artificially increased in several experiments). The results of the experiments with different noise levels are used to extrapolate the measurement result down to the limit of zero noise.

Your task would be as follows:

Construct some simple circuit you like (it can consist of only 2 or 3 qubits and several  RY,RZ,CX  gates).
Add measurements and compute some observable average for the circuit results (for example, the probability that the first qubit is in the state  |1⟩ ).
Add the noise model to simulator. For simplicity use the depolarizing_error as in the first tutorials. Find your observable expectation value for several values of error rate for the depolarizing error (for example, you can use error rates [0.02, 0.04, 0.06]).
Fit the resulting data with a linear function (or small degree polynomial) in error rate and use this fit to extrapolate the observable result to the limit of zero error rate.
Compare the extrapolation result with the simulation for zero error rate.
Note that the measurements results always have some randomness due to both the hardware noise and the shot noise. Hence, your results will always have some random deviations and curve fits will slightly vary from one simulation to another.
