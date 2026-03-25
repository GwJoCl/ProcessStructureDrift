# Repository Structure
This directory contains the analysis material for the BPM paper entitled "Explainable Concept Drift Detection based on Multivariate Process Abstraction".

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

| Algorithm      | Parameters                                                    |
|----------------|---------------------------------------------------------------|
| ProcessGraphs  | Window size: 300, max. window size: 400, p-value: 0.1         |
| EMD            | Window size: 150, step size: 1                                |
| Adwin/J        | Min/max adaptive window: 200/700, p-value: 0.4, step size: 20 |
| Rinv           | Minimum relation invariance distance: 600, epsilon: 180       |
| Lcdd           | Window size complete/detection: 400/400, stable period: 5     |
| Bose/J         | Window size: 150, step size: 2                                |
| ProDrift       | Window size: 400, step size: 2                                |
| MVPA           | Window size: 200, penalty = (number of traces)^0.5            |

The parameter settings and the results for ProcessGraphs, EMD, Adwin/J, Rinv, Lcdd, Bose/J, and ProDrift are adapted from:
https://gitlab.uni-mannheim.de/processanalytics/concept-drift-characterization

### User Behavior Data – high complexity (lags = 10)

| Algorithm      | Parameters                                                    |
|----------------|---------------------------------------------------------------|
| ProcessGraphs  | Window size: 15, max. window size: 40, p-value: 1.0           |
| EMD            | Window size: 6, step size: 1                                  |
| Adwin/J        | Min/max adaptive window: 4/16, p-value: 0.6, step size: 2     |
| Rinv           | Minimum relation invariance distance: 10, epsilon: 5          |
| Lcdd           | Window size complete/detection: 15/15, stable period: 5       |
| Bose/J         | Window size: 4, step size: 2                                  |
| ProDrift       | Window size: 2, step size: 1                                  |
| MVPA           | Window size: 14, change points = 1, change point adjustment: cp - (trace length / number of traces x 0.2 x 14)          |

### User Behavior Data – low complexity (lags = 10)

| Algorithm      | Parameters                                                    |
|----------------|---------------------------------------------------------------|
| ProcessGraphs  | Window size: 6, max. window size: 20, p-value: 1.0           |
| EMD            | Window size: 4, step size: 1                                  |
| Adwin/J        | Min/max adaptive window: 4/16, p-value: 0.5, step size: 2     |
| Rinv           | Minimum relation invariance distance: 10, epsilon: 3          |
| Lcdd           | Window size complete/detection: 10/10, stable period: 5       |
| Bose/J         | Window size: 3, step size: 2                                  |
| ProDrift       | Window size: 2, step size: 1                                  |
| MVPA           | Window size: 9, change points = 1, change point adjustment: cp - (trace length / number of traces x 0.45 x 9)          |



