==================================================
        TWO-COMPARTMENT IV BOLUS PHARMACOKINETIC MODEL
====================================================================
--------------------------------------------------------------------
PROJECT OVERVIEW
--------------------------------------------------------------------
This project simulates and analyzes a **two-compartment pharmacokinetic (PK)** model 
for an intravenous (IV) bolus dose. It demonstrates how to:

1. Build and solve a system of ordinary differential equations (ODEs)
   representing drug distribution between central and peripheral compartments.
2. Generate synthetic observed data by adding Gaussian noise to simulated data.
3. Estimate model parameters using nonlinear least squares optimization.
4. Visualize and compare model-predicted concentrations with observed data.

The workflow is representative of real-world pharmacokinetic model fitting 
used in drug development and clinical pharmacology.
--------------------------------------------------------------------
MODEL DESCRIPTION
--------------------------------------------------------------------
The model assumes a single IV bolus dose administered into the **central compartment**.

Let:
    A1 = amount of drug in the central compartment (mg)
    A2 = amount of drug in the peripheral compartment (mg)

The governing equations are:

    dA1/dt = -(k10 + k12)*A1 + k21*A2
    dA2/dt =  k12*A1 - k21*A2

where:
    k10 : elimination rate constant (1/hr)
    k12 : rate constant for transfer from central to peripheral (1/hr)
    k21 : rate constant for transfer from peripheral to central (1/hr)

Drug concentrations are computed as:
    C1 = A1 / V1
    C2 = A2 / V2

    
--------------------------------------------------------------------
Requirement
--------------------------------------------------------------------

pip install -r requirements.txt


