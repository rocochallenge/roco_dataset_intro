# Utility of the Real-World RoCo Dataset

This note can be reused on the project website and in manuscript revisions.

## Why the real-world subset matters

Simulation-only evaluation does not fully capture contact uncertainty, sensing noise, timing mismatch, and correction behavior in collaborative assembly. The real-world subset provides these effects directly and supports reproducible robustness benchmarking.

## Research directions enabled by this data

1. **Human-aware collaborative policy learning**  
   Learn when to continue autonomously vs. assist a human partner.

2. **Error detection and safe recovery**  
   Benchmark methods for identifying incorrect assembly states and correcting them.

3. **Task resumption from partial progress**  
   Study planning and control under interrupted workflows.

4. **Sim-to-real transfer and adaptation**  
   Evaluate representation learning and policy transfer from simulation to physical execution.

5. **Multimodal manipulation representation learning**  
   Use synchronized RGB, proprioception, and action logs for sequence modeling.

6. **Industrial generalization benchmarking**  
   Compare methods on order constraints, recovery quality, and completion under uncertainty.

## Suggested one-paragraph website text

The RoCo real-world subset is designed as a forward-looking benchmark resource for robust collaborative assembly research. Beyond challenge scoring, it enables future studies on human-aware decision-making, safe recovery, and sim-to-real transfer by exposing realistic sensing and execution imperfections that are difficult to model in simulation alone.
