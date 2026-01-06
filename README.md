# cryo-spring

Analyzing material stress in space telescope cryocooler springs to extend their lifetime.

## Problem

[TODO: space telescope, cryocooler, the spring, the problem caused by stress]

## Design

[TODO: kirigami examples (pics), why a kirigami-based design may be better, the high-level approach to test (computer simulation + physical experimentation)]

## Initial Analysis

[TODO: factors that affect stress, the jupyter graphs]

![Stress Analysis for Spiral Design](./pictures/Stress%20vs%20Arms%20%26%20Teardrop.png)

## SolidWorks Simulation

[TODO: the original spiral model & its stress points, the kirigami design & why design it this way & its stress points]

![SolidWorks All Springs](./pictures/SolidWorks%20All%20Springs.png)

## Physical Experiments

My initial experiments featured kirigami designs with 5 rings of concentric cuts. Initial tests showed that this design did not hold up because the effective arms were too thin. In our physical experiments, we tested alternatives with 3 and 4 concentric rings. Our design with 3 rings had the most similar effective arm width to the industry-standard spiral flexure spring with 6 arms.

![xTool All Springs](./pictures/xTool%20All%20Springs.png)

In physical experiments, I aimed to compare the maximum stress in each design. Stress was not possible to measure due to equipment limitations, so I used strain gauges instead. Since strain and stress are proportional in elastic deformation, a comparison of maximum strain can be used to infer the relative differences in stress.

A strain gauge changes resistance based on strain. From my initial tests, these resistance changes were too small to be meaningfully detected (e.g. changing from 120.0 to 120.1 ohms after maximum displacement). I first converted resistance changes to voltage measurements using a Wheatstone bridge. Now, the strain gauge's changes could be measured as a few millivolts. Using a low-power op amp, I amplified this voltage to measurable values. The result was that even a few grams placed on the flexure spring could be measured as a change in voltage, with a proportionality of about 1 mV/g.

Measuring the result, I was able to confirm that the kirigami-inspired design with 3 rings had 7% lower maximum stress than the spiral industry design.

![Circuit](./pictures/Circuit.png)

![Work Station](./pictures/Work%20Station.jpg)

![Voltage vs Mass](./pictures/Voltage%20vs%20Mass.png)

## Future Work

[TODO: more simulation in the future (take from the paper)]

## Acknowledgement

Dr. Hannah Rana at the [Harvard–Smithsonian Center for Astrophysics](https://www.cfa.harvard.edu/) provided the original spiral flexure spring model in SolidWorks. She guided me in the kirigami design and the publication of _[Stress Analysis of Stirling Cryocooler Flexure Springs for Long Space Mission Lifetime](./cec25_paper.pdf)_ at [Cryogenic Engineering Conference (CEC) 2025](https://www.cec-icmc.org/2025/).

Dr. Carl S. Kirkconnel shared thoughts on the potential weaknesses of the kirigami spring design at CEC 2025. This will be a direction of future work.

## References

[TODO: device & materials, key references from the paper]
