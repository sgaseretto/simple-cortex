# Simple Cortex (SC)

Simple Cortex (SC) is an unsupervised on-line learning machine intelligence architecture based on intelligence principles of the mammalian neocortex and a simple theory of neurons.  SC is:

- **General**: Algorithms can process any form of stimulation (spatio-temporal sensory-motor)
- **Dynamic**: Stored knowledge/memories adapt based on new knowledge and observations
- **Predictive**: Algorithms are able to predict multiple future states based on learned experience
- **Fast**: Algorithms are parallelized in OpenCL for GPU processing (10 billion synapses/sec on GTX 1070 GPU)

## Demos
[YouTube - Ball Demo](https://www.youtube.com/watch?v=iRt8sVPZkss)

![alt tag](https://raw.githubusercontent.com/ddigiorg/neuroowl.github.io/master/webpages/technology/simple-cortex/ball-demo.gif)

## Theory
- Neurons are sensors with memory that respond concurrent stimulae
- Concurrent stimulae are detectable changes in an environment within a time range
- Concurrent neuron activations (a form of stimulae) represent spatio-temporal sensory-motor patterns or sequences

## Architecture



- **Stimulae**: Detectable changes in an environment represented by a binary data vector
- **Synapse**: Fundamental memory storage structure
- **Dendrite**: A collection of Synapses forming a coincidence detector
- **Forest**: A collection of Dendrites used to organize OpenCL buffers
- **Neuron**: A collection of Dendrites forming a sensor that responds to stimulae
- **Area**: A collection of Neurons with activation and inhibition rules

## Algorithms
- **Encode**: Activates Neurons based on Stimulae
  - Overlap Synapses with Stimulae
  - Activate Neurons (and Inhibit if applicable)
  - If no Inhibition, select highest Boost Neurons

- **Learn**: Synapses store knowledge of Stimulae
  - For all Active Neurons: Grow, Shrink, or Move Synapses to Active Stimulae

- **Predict**: Predict Neurons based on Stimulae
  - Overlap Synapses with Stimulae
  - Predict Neurons
  
- **Decode**: Retrieve Stimulae based on Neuron Activations
  - Retrieve Synapse addresses of Active Neurons

## Future Improvements
- Upgrade compute-system and compute-program to use cl2.hpp
- Benchmark performance vs. NUPIC and Ogmaneo
- Upgrade algorithms to allow for observing and learning from scalar data vectors
- Optimize learnSynapses kernel

## Inspiration:
- **Numenta**: Hierarchical Temporal Memory(HTM)
- **Ogma**: Feynman Machine
- **Rebel Science**: Rebel Speech
