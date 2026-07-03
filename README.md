# Geometric Neuron Fractal

![pic](pic.png)

**Dynamic Topology, Oscillator Arithmetic, and Resonant Memory**

*Where `1 + 1 + 1 = π`*

Traditional Artificial Neural Networks (ANNs) rely on rigid, static weight matrices and linear addition. The **Geometric Neuron** abandons this in favor of dynamic, biological fractal growth and continuous wave interference.

In a standard digital adder, `1 + 1 = 10` (binary). In a resonant phasor network, discrete signals are mapped as complex wave phases (`1 → -1`, `0 → +1`). When you add sequential signals across spatial delays, you are not accumulating scalar values; you are rotating a vector through phase space. Accumulating discrete logical "ones" across a cyclic topology maps directly onto a continuous circular geometry—meaning logical addition fundamentally equals `π`.

## The Architecture

This repository contains a live, browser-based implementation of a foveated cortical loop. The network physically builds itself in real time by sampling a webcam feed and growing a topological map of its environment.

### Core Mechanics

1. **Environmental Substrate (Growth)**  
   Dendritic branches dynamically sprout toward high-luminance gradients in the live video feed. The network remains inherently sparse, only expending computational resources where environmental data exists.

2. **Top-Down Brainstem Pulse (Anterograde)**  
   The root node (the "Soma") acts as a biological pacemaker. It generates a continuous sinusoidal carrier wave that washes outward through the entire dendritic tree.

3. **Bottom-Up Sensory Interference (Retrograde)**  
   The active tips harvest visual data and propagate it back toward the root. As signals converge at branch bifurcations they undergo constructive and destructive interference, naturally implementing logic such as XOR and AND through wave cancellation.

4. **Resonant Memory Loops**  
   The network features topological memory. Nodes acting as leaky integrators trap propagating brainstem and sensory waves. When local geometry sustains a standing wave, the branch becomes a "frozen" memory register (visualized as purple clusters), locking in short-term spatial representations.

## Try It Live

You can run the project directly in your browser—no local web server required.

**Live Demo:**  
https://anttiluode.github.io/GeometricNeuronFractal/

## HUD & Controls

- **Mouse Drag & Scroll** — Pan and zoom through the fractal topology.
- **Root Tensor** — Displays the final collapsed wave signature arriving at the root node.
- **Brainstem Amp** — Adjusts the amplitude of the top-down oscillatory drive.
- **Growth Rate** — Controls how aggressively the network samples the environment each frame.
- **Toggle Memory Loops** — Enables or disables topological standing-wave memory.

## Future Development

This prototype lays the groundwork for translating temporal data into spatial geometry. Future iterations will integrate `resonatorCompute()` phasor logic at every node, allowing the fractal to function as a complete, topology-driven analog arithmetic logic unit (ALU), with computation emerging from resonance rather than static weights.

## License

See the repository license for details.
