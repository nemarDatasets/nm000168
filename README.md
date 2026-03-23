# BNCI 2015-013 Error-Related Potentials dataset

BNCI 2015-013 Error-Related Potentials dataset.

## Dataset Overview

- **Code**: BNCI2015-013
- **Paradigm**: p300
- **DOI**: 10.1109/TNSRE.2010.2053387
- **Subjects**: 6
- **Sessions per subject**: 20
- **Events**: Target=1, NonTarget=2
- **Trial interval**: [0, 0.6] s
- **File format**: matlab

## Acquisition

- **Sampling rate**: 512.0 Hz
- **Number of channels**: 64
- **Channel types**: eeg=64
- **Channel names**: Fp1, AF7, AF3, F1, F3, F5, F7, FT7, FC5, FC3, FC1, C1, C3, C5, T7, TP7, CP5, CP3, CP1, P1, P3, P5, P7, P9, PO7, PO3, O1, Iz, Oz, POz, Pz, CPz, Fpz, Fp2, AF8, AF4, AFz, Fz, F2, F4, F6, F8, FT8, FC6, FC4, FC2, FCz, Cz, C2, C4, C6, T8, TP8, CP6, CP4, CP2, P2, P4, P6, P8, P10, PO8, PO4, O2
- **Montage**: standard_1020
- **Hardware**: Biosemi ActiveTwo
- **Sensor type**: active
- **Line frequency**: 50.0 Hz

## Participants

- **Number of subjects**: 6
- **Health status**: patients
- **Clinical population**: Healthy
- **Age**: mean=27.83, std=2.23
- **Gender distribution**: male=5, female=1
- **Handedness**: not reported
- **BCI experience**: not reported
- **Species**: human

## Experimental Protocol

- **Paradigm**: p300
- **Task type**: monitoring
- **Number of classes**: 2
- **Class labels**: Target, NonTarget
- **Trial duration**: 2.0 s
- **Study design**: Error-related potential (ErrP) monitoring task where subjects observe a cursor moving towards a target. The cursor moves autonomously with 20% or 40% error probability. Subjects monitor performance without control.
- **Feedback type**: visual
- **Stimulus type**: cursor_movement
- **Stimulus modalities**: visual
- **Primary modality**: visual
- **Synchronicity**: synchronous
- **Mode**: offline
- **Training/test split**: True
- **Instructions**: Subjects seat in front of a computer screen and monitor a moving cursor (green square) and target location (blue for left, red for right). No control over cursor movement, only assess whether it performs properly. Fixate center of screen.

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  Target
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Target

  NonTarget
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Non-target

```
## Paradigm-Specific Parameters

- **Detected paradigm**: p300

## Data Structure

- **Trials**: ~50 trials per block, ~64 trials per block for error_prob=0.20
- **Blocks per session**: 10
- **Block duration**: 180.0 s
- **Trials context**: per_block

## Preprocessing

- **Data state**: raw
- **Preprocessing applied**: False

## Signal Processing

- **Classifiers**: Gaussian classifier
- **Feature extraction**: event-related potentials
- **Frequency bands**: analyzed=[1.0, 10.0] Hz

## Cross-Validation

- **Method**: train-test split
- **Evaluation type**: cross_session

## Performance (Original Study)

- **Accuracy**: 75.8%
- **Correct Recognition Rate**: 63.2
- **Error Recognition Rate**: 75.8

## BCI Application

- **Applications**: error_detection
- **Environment**: laboratory
- **Online feedback**: False

## Tags

- **Pathology**: Healthy
- **Modality**: Cognitive
- **Type**: ErrP

## Documentation

- **Description**: Dataset on EEG error-related potentials (ErrPs) elicited when users monitor the behavior of an external autonomous agent. One of the first studies showing that error correlates can be observed and decoded during monitoring of external agents without user control.
- **DOI**: 10.1109/TNSRE.2010.2053387
- **License**: CC-BY-NC-ND-4.0
- **Investigators**: Ricardo Chavarriaga, José del R. Millán
- **Senior author**: José del R. Millán
- **Contact**: ricardo.chavarriaga@epfl.ch; jose.millan@epfl.ch
- **Institution**: Ecole Polytechnique Fédérale de Lausanne
- **Department**: Defitech Chair in Brain-Machine Interface, CNBI, Center for Neuroprosthetics
- **Country**: CH
- **Repository**: BNCI Horizon
- **Publication year**: 2010
- **Funding**: EC under Contract BACS FP6-IST-027140
- **Keywords**: error-related potentials, ErrP, brain-computer interface, reinforcement learning, monitoring, error detection

## References

Chavarriaga, R., & Millán, J. D. R. (2010). Learning from EEG error-related potentials in noninvasive brain-computer interfaces. IEEE Trans. Neural Syst. Rehabil. Eng., 18(4), 381-388. https://doi.org/10.1109/TNSRE.2010.2053387

Notes

.. versionadded:: 1.2.0
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
