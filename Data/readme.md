Lithology Prediction Dataset (FORCE 2020)
This dataset contains well log data for predicting lithology (rock type) from various geophysical measurements. It's part of the FORCE 2020 lithology prediction competition, ideal for developing and testing machine learning models. Well log measurements serve as input features, FORCE_2020_LITHOFACIES_LITHOLOGY is the target variable, and FORCE_2020_LITHOFACIES_CONFIDENCE indicates prediction certainty. Well location and geological information provide additional context.

Columns
Well Identification and Location
WELL: Unique well identifier.
DEPTH_MD: Measured depth (MD) in meters (vertical distance down the wellbore).
X_LOC, Y_LOC: Easting and Northing coordinates (well's horizontal position, likely UTM).
Z_LOC: Depth in a vertical coordinate system (elevation relative to sea level, different from DEPTH_MD).
Geological Information (Ground Truth)
GROUP: Broader geological grouping of formations.
FORMATION: Specific geological formation at a given depth (finer subdivision than GROUP).
FORCE_2020_LITHOFACIES_LITHOLOGY: Target variable: lithology (rock type) at each depth (categorical, with codes for different lithologies).
FORCE_2020_LITHOFACIES_CONFIDENCE: Confidence in the assigned lithology label (important for evaluating model performance).
Well Log Measurements (Features)
CALI: Caliper log (borehole diameter).
RSHA: Shallow resistivity log.
RMED: Medium resistivity log.
RDEP: Deep resistivity log.
RHOB: Bulk density log.
GR: Gamma-ray log.
SGR: Spectral gamma ray log.
NPHI: Neutron porosity log.
PEF: Photoelectric factor log.
DTC: Sonic/acoustic log (sound wave travel time).
SP: Spontaneous potential log.
BS: Bit size (diameter of the drill bit).
ROP: Rate of penetration (drilling speed).
DTS: Shear wave velocity log.
DCAL: Difference between caliper and bit size.
DRHO: Density correction.
MUDWEIGHT: Density of the drilling mud.
RMIC: Micro-resistivity log.
ROPA: Processed/interpreted resistivity measurement.
RXO: Resistivity of the flushed zone.
Dataset Use Cases
This dataset is suited for developing and testing machine learning models for lithology prediction. The various well log measurements provide valuable input features, while the FORCE_2020_LITHOFACIES_LITHOLOGY column serves as the target variable. The well location and geological information (GROUP, FORMATION) can provide additional context for analysis. The target code corresponds to lithologies that are mainly encountered in the North Sea reservoirs. The dataset is highly imbalanced, so keep this in mind.

Code	Lithology
30000	Sandstone
65030	Sandstone/Shale
65000	Shale
80000	Marl
74000	Dolomite
70000	Limestone
70032	Chalk
88000	Halite
86000	Anhydrite
99000	Tuff
90000	Coal
93000	Basement
