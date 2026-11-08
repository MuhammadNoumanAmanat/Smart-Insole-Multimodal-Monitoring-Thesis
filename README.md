# Wearable Smart Insole for Early Diabetic Foot Ulcer Prediction Using Multi-Modal Sensing

**Bachelor's Thesis / Final-Year Project · BSc Electrical Engineering · Information Technology University of the Punjab (ITU), Lahore · 2025**

**Authors:** Muhammad Nouman and Abdul Rahman  
**Supervisor:** Prof. Dr. Qasim Mehmood  
**Co-supervisor:** Dr. Sadia Noureen  
**Publication:** [IEEE INMIC 2025](https://doi.org/10.1109/INMIC65900.2025.11348422) · DOI: [10.1109/INMIC65900.2025.11348422](https://doi.org/10.1109/INMIC65900.2025.11348422)

## Thesis and project materials

The **university-approved bachelor's thesis** and **research poster** are publicly available here, together with prototype visuals, results, CAD files, and a short demonstration video. The university, supervisors, and co-authors have approved sharing the thesis and poster, as confirmed by the project team.

- 📄 **[Read the bachelor's thesis (PDF)](docs/Muhammad_Nouman_Bachelors_Thesis.pdf)**
- 🖼️ **[View the research poster (PDF)](docs/Muhammad_Nouman_Thesis_poster.pdf)**
- 🎬 **[Watch the initial hardware demonstration](Hardware_Initial_Demo.mp4)**
- 📷 **[Explore prototype photographs](Hardware-Images/Hardware_Prototype/)**
- 📊 **[Explore experimental results and visualizations](Hardware-Images/Results/)**
- 🧩 **[Browse 3D hardware and enclosure models](Hardware_Files/)**

**Public release scope:** The thesis, poster, selected images, video, and mechanical CAD/STL models are public. **Python/MATLAB/microcontroller source code, trained models, and research datasets remain private.** This repository documents the project and does not claim to provide a fully reproducible software implementation.

## Overview

Diabetic foot ulcers can be associated with abnormal plantar loading and changes in local physiological conditions. Our final-year project investigated a **wearable multimodal smart-insole prototype** for collecting and visualizing relevant sensor measurements and assessing patterns in time-series data with machine learning.

The prototype combines pressure and physiological sensors, microcontroller-based data acquisition, wireless transmission, MATLAB visualization, and an experimental Long Short-Term Memory (LSTM) classification workflow. The work brings together **embedded electronics, biomedical sensing, signal processing, and applied machine learning**.

## System architecture

```mermaid
flowchart LR
    A["6 × FSR 402<br/>plantar pressure"] --> D["Arduino Mega 2560"]
    B["2 × SHT31<br/>temperature / humidity"] --> D
    C["MAX30102<br/>pulse oximetry / heart rate"] --> D
    D --> E["HC-12 wireless link"]
    E --> F["Sensor-data acquisition"]
    F --> G["MATLAB visualizations<br/>and pressure mapping"]
    F --> H["Preprocessing /<br/>time-series features"]
    H --> I["LSTM classifier"]
    I --> J["Experimental<br/>risk-category output"]
```

### Prototype components

| Component | Purpose |
| --- | --- |
| FSR 402 force-sensitive resistors (6) | Measure plantar pressure at selected locations |
| SHT31 sensors (2) | Measure local temperature and humidity |
| MAX30102 | Record pulse-oximetry and heart-rate signals |
| Arduino Mega 2560 | Collect sensor readings |
| HC-12 radio modules | Transmit readings to the receiving system |
| MATLAB | Real-time sensor visualization and pressure mapping |
| Python / TensorFlow | LSTM-based experimental analysis |
| Custom enclosure and insole assembly | Package the wearable electronics |

The component configuration above follows the **published IEEE INMIC paper**. Different design iterations may be described in earlier project notes.

## Machine-learning approach

The bachelor's thesis (Chapter 6) describes a time-series classification pipeline:

1. Acquire sensor readings and arrange measurements in CSV-formatted time series.
2. Normalize inputs, calculate descriptive temporal features, and address reported class imbalance with augmentation.
3. Train an LSTM network with two 128-unit recurrent layers, dropout, and a dense classification head.
4. Evaluate on the reported **70% training / 15% validation / 15% testing** split using accuracy, precision, recall, F1 score, and a confusion matrix.

**Reported results (not independently reproduced in this repository):**

| Evaluation | Result as reported |
| --- | --- |
| Study participants | 22 volunteers (IEEE INMIC paper) |
| Thesis-reported test accuracy | 92% (bachelor's thesis, §6.6) |
| Thesis-reported high-risk precision / recall | 89% / 87% (bachelor's thesis, §6.6) |
| Conference paper's LSTM classification result | 94–96% (IEEE INMIC paper, §4.4) |

These figures come from different sections/documents; they **should not be treated as directly equivalent benchmark runs**. Source code, evaluation splits, label definitions, and the precise experimental protocol need to be checked before stronger reproducibility claims are made. The project has not established clinical diagnostic accuracy or prospective prediction of future ulceration.

## Selected visuals

| Hardware prototype | Plantar pressure monitoring |
| :---: | :---: |
| ![Assembled wearable insole prototype](Hardware-Images/Hardware_Prototype/2.png) | ![Recorded FSR plantar pressure values](Hardware-Images/Results/FSR%20Sensors%20Pressure%20Monitoring.png) |

| Classification confusion matrix | Gait-cycle analysis |
| :---: | :---: |
| ![Experimental classification confusion matrix](Hardware-Images/Results/Confusion_Matrix.png) | ![Gait-cycle monitoring results](Hardware-Images/Results/Gait%20Cycle%20Results.png) |

Additional materials include [FSR sensor sensitivity](Hardware-Images/Results/FSR_Sensors_Sensitivity_Analysis.png), [SHT31 temperature and humidity measurements](Hardware-Images/Results/SHT31%20Temperature%20%26%20Humidity%20Monitoring.png), [MAX30102 pulse oximetry and heart-rate monitoring](Hardware-Images/Results/MAX30102%20Spo2%20and%20Heart%20Rate%20Monitoring.png), and [the sensor-input radar chart](Hardware-Images/Results/Sensors_Input_Radar.png). Figures are presented as project outputs; they do not establish clinical effectiveness.

## Research outputs

| Material | Availability |
| --- | --- |
| **Bachelor's thesis (PDF)** | **[Read the full approved dissertation](docs/Muhammad_Nouman_Bachelors_Thesis.pdf)** |
| **Research poster (PDF)** | **[View the approved poster](docs/Muhammad_Nouman_Thesis_poster.pdf)** |
| **IEEE INMIC 2025 paper** | [Publisher record and DOI](https://doi.org/10.1109/INMIC65900.2025.11348422) |
| Prototype photographs and result plots | **[Hardware photographs](Hardware-Images/Hardware_Prototype/)** · **[Results and graphs](Hardware-Images/Results/)** |
| CAD assemblies and STL hardware models | **[Receiver-side files](Hardware_Files/Receiver%20Side/)** · **[Transmitter-side files](Hardware_Files/Transmitor%20Side/)** |
| Python, MATLAB, and microcontroller source code | **Private — not being released** |
| Trained model/checkpoints | **Private — not being released** |
| Participant-level/raw biomedical data | **Private — not publicly released** |
| Initial hardware demonstration video | **[View demo](Hardware_Initial_Demo.mp4)** |

This repository is a **research documentation and hardware-design portfolio**, not a fully reproducible software release. The thesis documents, prototype imagery, visualizations, demonstration video and CAD/STL hardware assets are available above; underlying software and datasets are not publicly distributed.

## Limitations and responsible use

- The participant study was limited in size; there is no documented large-scale, independent clinical validation.
- Classification metrics should not be interpreted as reliable clinical screening performance.
- Sensor readings can depend on placement, motion, calibration, and participant characteristics.
- To protect research participants and comply with the chosen sharing scope, **all raw data, trained models and source code are excluded from public release**.
- The published conference article is linked via its official DOI instead of uploading an unlicensed publisher PDF.

## Citation

Muhammad Nouman and Abdul Rahman, **“Wearable Smart Insole for Early Diabetic Foot Ulcer Prediction Using Multi-Modal Sensing,”** *2025 27th International Multitopic Conference (INMIC)*, IEEE, 2025. https://doi.org/10.1109/INMIC65900.2025.11348422

## Acknowledgments

This final-year project was carried out at the **Department of Electrical Engineering, Information Technology University of the Punjab**, with the guidance of Prof. Dr. Muhammad Qasim Mehmood and Dr. Sadia Noureen. The IEEE publication notes equal contributions from both authors.

---

**Contact:** [Muhammad Nouman](https://github.com/MuhammadNoumanAmanat) · [ORCID](https://orcid.org/0009-0008-6085-4282)
