# Repository Structure

## Data
The [Data](https://github.com/GwJoCl/ProcessStructureDrift/tree/main/Data) file contains the user behavior data used for evaluation.

The simulated event log collection can be found here: https://gitlab.uni-mannheim.de/processanalytics/concept-drift-characterization

## Implementation
The [Notebooks](https://github.com/GwJoCl/ProcessStructureDrift/tree/main/Notebooks) directory contains all relevant implementations for the paper and is organized as follows:

### Data preparation and utils
- [classes_axillary.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/classes_axillary.ipynb)
- [helpers.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/helpers.ipynb)
- [utilities.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/utilities.ipynb)

### Concept drift detection algorithms
- [Algo1_processGraph.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/Algo1_processGraph.ipynb)
- [Algo2_Bose.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/Algo2_Bose.ipynb)
- [Algo3_Zheng_Source.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/Algo3_Zheng_Source.ipynb)
- [Algo4_EMD_Source.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/Algo4_EMD_Source.ipynb)
- [Algo5_LCDD_Source.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/Algo5_LCDD_Source.ipynb)
- [Algo6_Martjushev.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/Algo6_Martjushev.ipynb)
- [Algo7_proDrift.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/Algo7_proDrift.ipynb)
- [ConceptDriftBPM.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/ConceptDriftBPM.ipynb)

### Evaluation
- [evaluate_v2.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/evaluate_v2.ipynb)
- [evaluate_EyeTracking.ipynb](https://github.com/GwJoCl/ProcessStructureDrift/blob/main/Notebooks/evaluate_EyeTracking.ipynb)

## Parameter Settings

### Simulated data (lags = 5)
(Original tables preserved as text due to Markdown limitations.)

### User Behavior Data – high complexity (lags = 10)
(Tables preserved as text.)

### User Behavior Data – low complexity (lags = 10)
(Tables preserved as text.)

The parameter settings and the results for ProcessGraphs, EMD, Adwin/J, Rinv, Lcdd, Bose/J, and ProDrift are documented in the following repository:
https://gitlab.uni-mannheim.de/processanalytics/concept-drift-characterization

