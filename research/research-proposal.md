# A Feasibility Study of Edge-Based Deep Learning for Early-Stage Crop Water Stress Detection Using Thermal and Visible Imagery

## Subject of Study
Traditional cloud-based agriculture faces a major obstacle in unreliable internet connectivity. This research proposes an edge computing framework with deep learning models deployed on Unmanned Aerial Vehicle (UAV) platforms for near–real-time early-stage crop water stress detection.

The proposed system analyzes Thermal Infrared (TIR) and visible imagery to identify temperature- and vegetation-based indicators of early-stage water stress. This study evaluates whether deep learning models deployed on UAV edge devices can reliably detect early-stage crop water stress by comparing their performance with traditional empirical methods.

The findings aim to assess the practicality of edge-based stress detection as a decision-support tool for timely irrigation management in remote and connectivity-constrained agricultural environments.

---

## Research Questions
1. Can lightweight deep learning models deployed on UAV edge devices accurately detect early-stage crop water stress under offline operating conditions?
2. What are the trade-offs between classification accuracy, inference latency, and energy consumption when deploying edge-based deep learning models for UAV water stress monitoring?
3. How does offline, edge-based water stress detection compare with cloud-based approaches in connectivity-constrained agricultural environments?
4. To what extent can early-stage water stress detection enable more timely irrigation decision-making compared to conventional visual or delayed monitoring methods?

---

## Analysis of the Problem
Agricultural production in arid and semi-arid regions is increasingly constrained by limited water availability, rising temperatures, and irregular rainfall patterns. In such environments, water resources must be managed with high precision. Traditional irrigation practices rely on fixed schedules and reactive assessments of crop health, which are poorly suited to dynamic climatic conditions.

Policies such as the European Union’s Common Agricultural Policy (CAP) emphasize sustainable water use to reduce the environmental impact of agricultural practices, placing additional pressure on farmers to optimize water consumption while maintaining profitability.

Despite these imperatives, many existing agricultural monitoring systems remain ineffective in real-world deployment. These systems often depend on reliable connectivity, lack robustness across varying climates and crop types, and fail to detect subtle early-stage water stress indicators. There is a clear need for systems capable of early, reliable stress detection that are deployable in real agricultural environments.

---

## Research Methodology
This study employs an experimental feasibility evaluation to assess deep learning models under UAV-relevant constraints for early-stage crop water stress detection using TIR and visible imagery.

### Data Acquisition and Preprocessing
Primary data will be sourced from the publicly available dataset by Fevgas et al., containing paired radiometric TIR and RGB images of lettuce plants under controlled irrigation conditions. Although collected in a ground-based setting, the dataset provides high-resolution thermal signatures relevant to UAV-based monitoring.

Preprocessing steps include plant canopy segmentation, normalization, and noise reduction to improve model robustness.

### Model Architecture
Lightweight Convolutional Neural Networks (e.g., MobileNetV3) will be trained for patch-level or image-level water stress classification. Trained models will be deployed on edge devices such as the NVIDIA Jetson Nano to enable offline inference.

### Evaluation
Model performance will be evaluated using cross-validation with time-aware data splits to assess early stress detection before visible symptoms emerge. Evaluation metrics include:

- Classification accuracy
- Precision, recall, and F1-score
- Inference latency
- Memory footprint
- Estimated energy consumption

Performance will be compared against:
1. Traditional empirical water stress indicators  
2. Non–deep learning methods reported by Fevgas et al.  
3. Ablation variants excluding thermal–visible fusion or denoising  

---

## Preliminary Answers
It is expected that lightweight deep learning models can identify early-stage crop water stress from thermal and visible imagery with reasonable accuracy under edge computing constraints. These models are anticipated to demonstrate higher sensitivity to early stress indicators compared to empirical methods, at the cost of increased energy and computational requirements.

Offline edge processing is expected to be faster and more reliable than cloud-based approaches in low-connectivity scenarios. The integration of thermal and visible imagery is anticipated to improve detection robustness compared to single-modality approaches. Overall, edge-based deep learning is expected to be practical for early-stage crop water stress detection.

---

## Academic Contributions of the Study
- Demonstrates the feasibility of deep learning for early-stage water stress detection on edge devices
- Advances thermal and visible image fusion techniques under edge constraints
- Provides a comparative analysis between deep learning and empirical baselines
- Proposes a reusable experimental evaluation pipeline for UAV deployments
- Contributes insights toward precision irrigation and reduced fertilizer and nitrate runoff

---

## Literature Review
Crop water stress detection has long been an active research area due to its direct impact on yield and sustainability. Traditional methods rely on empirical and physically derived indicators that exploit relationships between transpiration, canopy temperature, and atmospheric conditions. While simple and interpretable, these approaches often lack adaptability and sensitivity to early stress signals.

Recent advances in deep learning have shown strong performance in detecting moderate to severe water stress using thermal and visible imagery. However, early-stage stress detection remains challenging due to the subtle nature of the signals. The dataset introduced by Fevgas et al. provides paired radiometric TIR and RGB imagery of lettuce plants grown under controlled irrigation conditions, enabling fine-grained analysis of early stress patterns. Although laboratory-based, the dataset serves as a suitable foundation for feasibility studies focused on constrained edge deployments.

---

## References
- Clarke, T. R. (1997). An Empirical Approach for Detecting Crop Water Stress Using Multispectral Airborne Sensors. *HortTechnology, 7*(1), 9–16. https://doi.org/10.21273/horttech.7.1.9  
- Dong, H., Dong, J., Sun, S., et al. (2024). Crop water stress detection based on UAV remote sensing systems. *Agricultural Water Management, 303*, 109059. https://doi.org/10.1016/j.agwat.2024.109059  
- European Union. (2025). Water. *Agriculture and Rural Development*. https://agriculture.ec.europa.eu/cap-my-country/sustainability/environmental-sustainability/natural-resources/water_en  
- Fevgas, G., Lagkas, T., Argyriou, V., & Sarigiannidis, P. (2025). A Dataset of Thermal Infrared (TIR) and RGB Images of Lettuces. *Mendeley Data*. https://doi.org/10.17632/294zk6k5wf.2  
- Fevgas, G., Lagkas, T., Papadopoulos, P., et al. (2025). Integrating Thermal Infrared and RGB Imaging for Early Detection of Water Stress in Lettuces. *Smart Agricultural Technology*, 100881. https://doi.org/10.1016/j.atech.2025.100881  
- Shaikh, M. S., Jha, A. K., Soni, B. R., et al. (2025). Flying Edge Intelligence. *ICETEA 2025*, 1–6. https://doi.org/10.1109/icetea64585.2025.11099749  
- United Nations. (2022). Water. https://www.un.org/en/UN-system/water
