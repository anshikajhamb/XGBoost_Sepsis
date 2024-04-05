As can be seen, there are several limitations to my XGBoost model given the complexity of the Sepsis dataset (Physionet 2019 Challenge*):

1. I did not take into account the utility function: the challenge data is labelled with the value ‘1’ for pa-tients who develop sepsis where t≥tsepsis −6and 0 for t < tsepsis −6,tsepsis being the time of sepsis on-set as deﬁned by the Sepsis-3 deﬁnition. For patients whonever develop sepsis the data is labelled zero everywhere.Predictions are scored for their binary classiﬁcation per-formance against a utility function described fully in thechallenge description. False positives are penalised in non-septic patients and zero score is given for true negative pre-dictions. For septic patients, early prediction is penalised,false negative predictions are more heavily penalised, andtrue positive predictions yield a positive scor

2. Did not include new hand-crafted features: new features, especially when derived from relevant physiological parameters like heart rate, systolic blood pressure, bilirubin, and creatinine levels, can provide additional information that may enhance the model's ability to detect sepsis accurately. This requires heavy reading of medical literature to familiarise myself with such derived features.  



*Reyna, M. A., Josef, C. S., Jeter, R., Shashikumar, S. P., Westover, M. B., Nemati, S., Clifford, G. D., & Sharma, A. (2020). Early Prediction of Sepsis From Clinical Data: The PhysioNet/Computing in Cardiology Challenge 2019. Critical care medicine, 48(2), 210–217. https://doi.org/10.1097/CCM.0000000000004145
