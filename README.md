# BCI-I & IDUN EEG Challenge: onset-locked features + EM prior adaptation

Late submission to the [BCI-I & IDUN EEG Analysis Challenge](https://www.kaggle.com/competitions/bci-i-idun-eeg-analysis-challenge):
**private 0.833 · public 0.789** weighted F1 (best leaderboard score: 0.630).

Kaggle notebook: https://www.kaggle.com/code/polsalvatella/sleep-eeg-analysis

Classifies 30 s windows of single-channel in-ear EEG (IDUN Guardian) into 7 sleep events, training on
3 subjects and testing on an unseen 4th. The model uses band envelopes locked to the event onset and
normalised to each subject's whole night, plus sleep-context features from the raw recording. These go
into a logistic regression, and the test subject's spindle / K-complex / REM mix is re-estimated by EM.
Leave-one-subject-out weighted F1: 0.804.

The competition data is not included; download it from the competition's Data tab.
