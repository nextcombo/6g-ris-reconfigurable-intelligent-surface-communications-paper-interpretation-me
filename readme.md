# 6G RIS (Reconfigurable Intelligent Surface) Communications Paper Interpretation | Message-Passing Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [with MATLAB Code]

6G RIS (Reconfigurable Intelligent Surface) communication paper interpretation | Message-Passing Based Multi-User Joint Channel Estimation and Signal Recovery✨Paper Information
Title: Joint Channel Estimation and Signal Recovery for RIS-Empowered Multi-User Communications
Publication: IEEE Transactions on Communications
Research Direction: Reconfigurable Intelligent Surface (RIS), Multi-User Communication, Channel Estimation, Signal Recovery, Message Passing Algorithms
🔎 Research Background The Reconfigurable Intelligent Surface (RIS) is a core candidate technology for 5G-A/6G. It relies on a massive number of passive reflective units to dynamically remodel the wireless propagation environment, offering advantages such as low power consumption, low cost, wide coverage, low latency, and massive connectivity compared to traditional relay devices. Compared to traditional relay equipment, it is more suitable for new generation communication networks.
Due to hardware limitations, the implementation of RIS systems faces many practical challenges: the large number of reflective units introduces a vast number of unknown parameters, significantly increasing the difficulty of cascading channel estimation; existing research mostly assumes ideal channel conditions, which is disconnected from engineering practice.
Traditional solutions generally adopt a "estimate the channel first, then recover the signal" stepwise processing mode, not only leading to high pilot training overhead but also failing to explore the correlation features between the channel and the signal. Meanwhile, mainstream AMP-type algorithms are easily affected by sick measurement matrices, and the iteration process tends to diverge. In summary, joint channel estimation and signal recovery in multi-user scenarios of RIS is a key technical challenge that needs to be addressed urgently.
💡 Shortcomings of Existing Solutions Currently, mainstream technological approaches have significant limitations, making it difficult to balance performance, complexity, and real-world implementation:
1. Deep learning solutions rely on large-scale offline training, with weak generalization capabilities;
2. Compressed sensing solutions require additional active units, increasing hardware costs and power consumption;
3. Parallel factor analysis (PARAFAC) decomposition has strict constraints, and the computational complexity increases sharply with an increase in the number of RIS units;
4.
Layered Training Algorithm: Relies on multiple time-slot iterations, inefficient in multi-user scenarios;
Separated Estimation Algorithm: Separates channel estimation from signal recovery, unable to achieve global optimality, leading to high pilot resource consumption.
Currently, most research focuses solely on channel estimation, with integrated joint processing solutions being scarce.
🚀 Core Research Contribution This paper addresses the RIS-assisted multi-user uplink communication system, combining factor graph and message passing ideas, proposing two sets of novel joint estimation algorithms. These breakthroughs are evident across four dimensions: precision, convergence, robustness, and engineering practicality. The core value is clear:
1. Establishing a low-complexity joint processing framework for RIS multi-user communication system modeling, utilizing factor graph to represent the probability relationships between variables. By employing Taylor series expansion + Gaussian approximation to simplify the message passing iteration rules, the algorithm's computational overhead is significantly reduced while maintaining accuracy.
2. Two bidirectional improved algorithms specifically address industry challenges. BAMP Bidirectional Approximate Message Passing (BAMP) algorithm introduces damping factors to optimize the iterative logic, effectively suppressing algorithm divergence issues, achieving simultaneous estimation of channel and signal.
📌 BUTAMP Circular Transform Bidirectional AMP (BUTAMP) algorithm combines singular value decomposition (SVD) for circular transformation, completely avoiding the negative impact of ill-conditioned matrices. This algorithm is insensitive to damping factors and converges faster, demonstrating stronger engineering adaptability.
3. Solving inherent blurriness issues, clarifying complexity boundaries for matrix decomposition-induced scale and phase blurriness problems, a cost-effective strategy is designed; the overall algorithm complexity is (iterations), primarily involving matrix vector operations, fully meeting the requirements for engineering implementation.
4. Simulation performance outperforms traditional solutions by a significant margin. Compared to the classic BiGAMP + least squares stepwise scheme, the proposed algorithm demonstrates superior advantages:
Under equal pilot length, NMSE performance improvement of 18dB;
Even when the baseline scheme increases the number of pilots, there is a performance gap of more than 4dB;
The algorithm's performance remains stable under changes in RIS unit count, pilot ratio, and channel parameters.
📡 System Model Overview
This study investigates the uplink communication scenario with a multi-antenna base station and multiple single-antenna users assisted by a RIS, where there is no direct link between the user and the base station:
Base Station: Root Antenna
Mobile User: Single-antenna User
RIS: Passive Reflector Unit
System Received Signal Model: RIS Phase Diagonal Matrix; User to RIS Channel; RIS to Base Station Channel; User Transmitted Signal; Additive White Gaussian Noise.
The paper further maps the channel into the beam domain, leveraging its inherent sparse nature to provide reliable prior support for joint estimation.
⚙️ Core Design Concept of the Algorithm
1. Factor graph modeling divides variables such as channels and signals into nodes, constructing a bidirectional message passing architecture that consists of a forward and backward dual-layer iterative structure.
2. 
3. Gaussian Approximation + Taylor Expansion performs Gaussian approximation on complex message distributions, combined with Taylor expansion to simplify the iterative formulas, balancing algorithm accuracy with computational complexity.
4. 
5. Backward Iteration after the dual-layer bidirectional iterative process: Reversely derive the channel and transmitted signal from the received signal; forward iteration: Update the intermediate matrix based on estimated results in a forward direction, cycling through until convergence; inner layer integrates an AMP improvement strategy to ensure stability of the iteration.
6. 
7. Fuzzy Termination combines channel sparsity constraints, known channel vectors, full-rank signal design, etc., to eliminate phase and scale fuzziness, further enhancing estimation accuracy.
📊 Key Simulation Results (Engineering Value)
1. Low Guidance Overhead: With only 0.3% of the pilot overhead, performance can be approached close to the upper limit, significantly saving spectrum resources;
2. 
3. Scalability: The number of RIS units increases, leading to more unknown variables, but overall operation remains stable;
4. 
5. High Efficiency in Convergence: Under the same SNR condition, BUTAMP requires fewer iterations than BAMP, requiring only 18 iterations under a 20dB scenario;
6. 
7. Robustness: BAMP's performance is easily affected by the noise factor, whereas BUTAMP is almost unaffected by parameter perturbations, making field deployment more convenient.
🌟 Application and expansion direction: This algorithm framework is highly versatile, extendable to multiple mainstream 6G application scenarios, with extremely high commercial potential.
1  
Compatible with multi-antenna users and downlink multi-user communication scenarios.
2  
Adapts to 6G ultra-dense network, terahertz communication, and distributed RIS networking.
3  
The low pilot frequency and low complexity characteristics perfectly match the massive terminals of the Internet of Things (IoT) to avoid authorization access needs.
4  
Provides a complete theoretical basis and practical implementation plan for the algorithm design and engineering implementation of RIS commercial receivers.
This article breaks away from the traditional "channel estimation + signal recovery" step-by-step processing mindset, creating a new joint processing algorithm based on message passing architecture. It comprehensively surpasses existing technology in terms of estimation accuracy, convergence speed, parameter robustness, and implementation complexity, providing a novel approach and feasible solution for 6G RIS communication receiver design.

## Images

[6G RIS Communication Paper Interpretation | Message-Passing-Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [Attached MATLAB Code]](01.jpg)
[6G RIS Communication Paper Interpretation | Message-Passing-Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [Attached MATLAB Code]](02.jpg)
[6G RIS Communication Paper Interpretation | Message-Passing-Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [Attached MATLAB Code]](03.jpg)
[6G RIS Communication Paper Interpretation | Message-Passing-Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [Attached MATLAB Code]](04.jpg)
[6G RIS Communication Paper Interpretation | Message-Passing-Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [Attached MATLAB Code]](05.jpg)
[6G RIS Communication Paper Interpretation | Message-Passing-Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [Attached MATLAB Code]](06.jpg)
[6G RIS Communication Paper Interpretation | Message-Passing-Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [Attached MATLAB Code]](07.jpg)
[6G RIS Communication Paper Interpretation | Message-Passing-Based Multi-User Joint Channel Estimation and Signal Recovery for RIS [Attached MATLAB Code]](08.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
