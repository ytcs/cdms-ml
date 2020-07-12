# cdms-ml

The repo contains standardized tasks which build towards developing a fully functional reconstruction pipeline for SuperCDMS detectors. Think of this as CIFAR or MNIST for CDMS.

The reconstruction pipeline consists of two main building blocks:

1. NN Event Simulation

   This model provides a "neuralized" version of the DMC. Accurate neuralization allows the DMC to be inverted efficiently and reliably. The goal is to be able to input various parameters (energy, position, ...) into a network that produces detector traces.
   
2. NN Trace Refinement

   This model allows us to fold in noise and other imperfections into the detector response that are impossible/impractical to simulate. The goal is to have a network that transform a simulated trace (either from the actual DMC or the neuralized version) into a "refined" trace that is indistinguishable to real data (including noise profile and other quirks).
   
The combination of the above networks will allow us to perform full event NN-based reconstruction.

We strongly encourage all members of the collaboration to take part in the various challenges.

All submissions should be compatible with Keras.
## List of open challenges:
 - [Two-pole simulation](simulation/twopole/README.md)

## References:
 -	[arXiv:1802.03325](https://arxiv.org/abs/1802.03325)
