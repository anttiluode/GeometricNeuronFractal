# **Geometric Neuron V5: Brainstem-Modulated Cortical Loop**

![pic](pic.png)

This repository contains an experimental, interactive prototype of a dynamically growing, biologically-inspired neural architecture. Unlike traditional artificial neural networks that rely on dense, static weight matrices, the Geometric Neuron builds a sparse, topological graph in real-time. It maps temporal data into physical spatial dimensions, utilizing wave interference and phase cancellation as its primary computational mechanisms.

## **Overview**

The V5 architecture introduces a hybrid signaling model. It combines a bottom-up, sensory-driven growth mechanism with a top-down, oscillatory "brainstem" drive. The network structurally adapts to its environment (a live webcam feed) while simultaneously modulating its own perception through intrinsic rhythmic agency.

## **Theory of Operation**

The system operates continuously across three fundamental mechanics:

### **1\. Environmental Substrate (Growth Phase)**

The live webcam feed acts as a continuous resource gradient. The algorithm randomly samples pixels, converting RGB data into luminance. Bright areas represent high resource density. Dendritic branches physically grow toward these light sources. Consequently, the geometry of the network natively embeds the structural outline of the visual environment.

### **2\. Top-Down Brainstem Carrier (Anterograde Signaling)**

The root node acts as a central pacemaker or "brainstem." It generates an intrinsic, sinusoidal carrier wave based on a global biological clock. This signal propagates outward (anterograde) from the root to the dendritic tips, applying a continuous, oscillating baseline state to the entire network topology.

### **3\. Hybrid Logic Interference (Retrograde Signaling & Computation)**

Visual data is harvested at the active tips (leaves) and propagates inward (retrograde) toward the root.  
Computation occurs at the bifurcations (where branches split). These junctions act as phase interferometers, executing continuous XOR logic:

* If two converging branches carry high signals simultaneously, they cause **destructive interference** (canceling each other out).  
* If the signal is asymmetric (only one branch is active), the signal propagates through.

**The Hybrid Interaction:** The top-down brainstem wave actively modulates this bottom-up interference. When the brainstem phase is positive, it amplifies the visual filter's sensitivity. When negative, it dampens incoming sensory noise. The final signal reaching the root is the "Root Tensor"—a topologically invariant signature of the environment.

## **Visual Interface & HUD**

The live rendering maps the mathematical state of the graph to visual indicators:

* **White/Cyan Nodes:** Active signal propagation and standard transmission paths.  
* **Red Nodes:** Locations of destructive interference (triggered XOR gates).  
* **Purple/Pulsing Nodes:** The root node and pathways currently dominated by the top-down brainstem pulse.

### **Real-Time Metrics**

* **Complexity (Nodes):** The current size of the network versus the hardware cap.  
* **Fractal Dimension (D):** A real-time approximation of the network's Hausdorff dimension ($D \\approx \\frac{\\ln(N)}{\\ln(R)}$). Watch this shift from sparse, lightning-like 1D structures towards space-filling 2D meshes based on the environment.  
* **Root Tensor:** The final collapsed signal value arriving at the root.  
* **Brainstem (In):** The current phase amplitude of the top-down oscillator.

## **Controls**

The UI features a dynamic control panel allowing you to stress-test the topology:

* **Mouse Drag & Scroll:** Pan and zoom around the expanding structure.  
* **Brainstem Drive Amplitude:** Adjust the strength of the top-down modulating wave. Set to 0 for purely reactive, sensory-driven logic.  
* **Max Node Capacity:** Hardware limiter for the graph size.  
* **Growth Rate:** How aggressively the network samples the environment for new resources per frame.  
* **Signal Decay:** The simulated latency loss as signals traverse the physical graph. Lower values cause signals to die out faster over long branches.  
* **Reset Topology:** Clears the graph and resprouts a new seed from the center.

## **Usage**

This prototype is entirely self-contained within a single HTML file.

1. Save the code as an .html file.  
2. Open it in any modern web browser (Chrome, Edge, Firefox).  
3. Grant the browser permission to access your webcam.  
4. Point the camera at high-contrast, moving objects (like a hand moving across a light source) to watch the topology form and compute.

*Note: Because the graph calculates recursive paths on every frame, setting the Max Node Capacity too high (e.g., \> 50,000) may cause browser stuttering depending on your CPU.*
