# Case Study: The First Image of a Black Hole

> **Source**: [`Case Study: The First Image of a Black Hole`](https://numpy.org/case-studies/blackhole-image/) | NumPy (Shaloo Shalini, Ross Barnowski, Inessa Pawson) | 2020 | [Repo](https://github.com/numpy/numpy.org/blob/master/content/en/case-studies/blackhole-image.md)

Saturday, October 10, 2020

- Challenging data processing/reduction pipeline (from petabytes to megabytes).
- "(...) EHT [(Event Horizon Telescope )] generates over 350 Terabytes worth of observed data per day, stored on high-performance helium filled hard drives."
- "The EHT collaboration met these [image reconstruction] challenges by having independent teams evaluate the data using both established and cutting-edge image reconstruction techniques to verify that the resulting images were consistent."
- "(...) the [`eht-imaging`](https://github.com/achael/eht-imaging) Python package provides tools for simulating and performing image reconstruction on VLBI data. NumPy is at the core of array data processing (...)."
- "The standard astronomical file formats and time/coordinate transformations were handled by [Astropy](https://www.astropy.org/) while Matplotlib was used in visualizing data throughout the analysis pipeline, including the generation of the final image of the black hole."
- pandas, SciPy, and Jupyter were also used.
- [PyWavelets](https://pywavelets.readthedocs.io/en/latest/).
- It is interesting to see that the collaboration _mindset_ also includes software.
