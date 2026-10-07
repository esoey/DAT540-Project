| Feature | Correlated with | \|Correlation value\| | Mutual Information |
|---|---|---:|---:|
| Total Body Fat Ratio (TBFR) | <span style="color:red">Lean Mass (LM)</span> | 0.993000 | 0.000000 |
| <span style="color:red">Lean Mass (LM)</span> | Total Body Fat Ratio (TBFR) | 0.993000 | 0.001378 |
| <span style="color:red">Total Body Water (TBW)</span> | Muscle Mass (MM) | 0.917678 | 0.000000 |
| Muscle Mass (MM) | <span style="color:red">Total Body Water (TBW)</span> | 0.917678 | 0.012192 |
| <span style="color:red">Total Body Water (TBW)</span> | Extracellular Water (ECW) | 0.903692 | 0.000000 |
| Extracellular Water (ECW) | <span style="color:red">Total Body Water (TBW)</span> | 0.903692 | 0.103296 |
| Body Mass Index (BMI) | Total Fat Content (TFC) | 0.898746 | 0.031273 |
| Total Fat Content (TFC) | Body Mass Index (BMI) | 0.898746 | 0.047288 |
| Total Cholesterol (TC) | LDL | 0.892628 | 0.070471 |
| LDL | Total Cholesterol (TC) | 0.892628 | 0.000000 |
| Intracellular Water (ICW) | Muscle Mass (MM) | 0.891041 | 0.100820 |
| Muscle Mass (MM) | Intracellular Water (ICW) | 0.891041 | 0.012192 |


Decision:

- We remove Lean Mass (LM) due to it being highly correlated with Total Body Fat Ratio (TBFR) (-0.993000). They are basically opposites. Both achieve low scores of Mutual Information (MI).

- We remove Total Body Water (TBW) due to it being highly correlated with Extracellular Water (ECW) (0.903692). Total Body Water (TBW) consists of  Intracellular Water (ICW) and Extracellular Water (ECW). The ECW achieves a much higher Mutual Information score than TBW, which indicates that ECW is much more important for the target label (Gallstone Disease).  

- In addition, a decision was made to remove the feature Obesity (%). This was due to several factors, such as clear and obvious error in one of the patients, uncertainties around how the value is calculated, and due to other features providing similar information. Our first thought was to remove this patient, however due to a low number of patients in the dataset, it was decided to keep the patient and remove the feature.  