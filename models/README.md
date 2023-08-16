# How to use

The models are listed twice each, once in the non-compiled version and once in the version that was compiled using the mujoco engine and has the low-level parameters explicitely written in the code (e.g. actuators are in generalised form, with all parameters listed).
It is recommended to use the compiled version for optimisation, as it avoids the compiling errors associated with the actuator length calculation (see [here](https://mujoco.readthedocs.io/en/stable/modeling.html?highlight=length#actuator-length-range) for explanation).

# Model versions

The [final model](models/final_model_from_mjc.xml) includes:

- 42 MTC (as outlined on main), with the FDC and FDS represented as straight-line MTC and the EDC represented as two-lever pulleys attached just distal from the PIP joint
- 4 [ORL](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3977782/), which was included to create a mechanical linkage of the PIP and DIP finger joints, ensuring finger curling
- 4 equality constraints, linking the lumbrical MTC and the ORL tendons

This design is partly derived from [Mirakhorlo et al. 2016](https://doi.org/10.1080/23335432.2016.1191373), specifically the inclusion of the ORL elements.

Intermediate versions are included to test the significance of certain mechanical features (e.g. the ORL and final EDC design). 
