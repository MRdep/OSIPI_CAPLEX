# Structure of CAPLEX

CAPLEX is organized into 4 sections which group together similar quantities, models or processes. 

## Quantities (Section Q)
This section contains definitions of variables. A variable is any quantity that can act as input or output to an analysis process, e.g., the longitudinal relaxation rate. 
## Models (Section M)
This section contains definitions of mathematical formulae that relate one quantity to another. These formulae typically describe the functional behaviour (often underlying vascular physiology) of measured data. Signficant effort has been made within CAPLEX to ensure that all models are defined using the same underlying parameterisation, such that outputs from different models can be easily compared and to maintain consistency for reporting. Models are defined along with their input and output quantities. Since it is common to fix parameters during curve fitting, model parameters can be specified as a Model Parameter (free) or Static Model Parameter (fixed). 

## Perfusion Processes and General Purpose Processes (Section P and section G)
This section contains definitions of processes. Processes are operators that generate output quantities from given input quantities. They differ from models in the sense that they map between quantities via a computational operation not an analytical formulae. A process does not define the algorithmic details of the operator, but instead defines semantically what is done, in a similar way to a function or routine name within a programming environment, e.g., Variable Flip Angle is a process that maps signal intensities acquired at multiple flip angles to the longitudinal relaxation rate and equilibrium magnetisation. All the required inputs to this process (quantities, models, and other processes) are defined. This purpose of operators is provide researchers with a checklist of quantities, models, etc to ensure that complex operations are described as completely as possible.

<figure markdown>
  ![Screenshot](osipiImgs/structure.png){ width="1300" }
  <figcaption> Organization of CAPLEX sections: Quantities (Section Q), Perfusion models (Section M), Perfusion processes (Section P), General purpose processes (Section G) and Derived processes (Section D). In the flow charts, quantities are given in orange boxes, processes and models are shown in purple boxes. The pipeline shown in the    perfusion processes box represents a typical pipeline that can be encoded using quantities, processes and models currently defined within CAPLEX version 1.0.3. It is possible to encode pipelines with fewer or entirely different processes than those shown (e.g. using R2 or R2* estimation and leakage correction when reporting DSC-MRI analyses).</figcaption>
</figure>
