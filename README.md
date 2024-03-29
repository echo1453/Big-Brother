# Big-Brother
This is the source code of the paper 'Big Brother is Listening: A Comprehensive Evaluation Framework on Ultrasonic Microphone Jammers' Resilience'.

## Audio Data
In folder "AudioData", there are the audios provided for testing our codes, which are only part of the data we used in our paper.

Each subfolder is named by the jammer name we used. The wav files in each subfolder are: Raw.wav: the clean speech without any process, A0.wav: the audio jammed by each ultrasonic microphone jammer, A1.wav: the result of the jammed audio processed by blind source separation (BSS), A2: processed by STFT-based notch filter (NF), A3: processed by wide band stop filter (WBSF) of 2 kHz cut-off frequency, and A4: processed by adaptive notch filter (ANF).

## Codes
In folder "Codes", there are the source codes for noise elimination and evaluating jammers' resilience. **Please Remember to Changing Audio Paths before Using.**

### Evaluation
In subfolder "Evaluation", there are the evaluation algorithms we used for the metrics of Intensity and Intelligibility. The Collaborative Recognition Rate is measured with volunteers and provided APIs of commercial automatic speech recognizers (ASRs), so we could not provide them.

The evaluation algrithms rely on https://github.com/schmiph2/pysepm.<br>
Install pysepm with python first:<br>
```
pip3 install https://github.com/schmiph2/pysepm/archive/master.zip
```

### Noise Elimination
In subfolder "NoiseElimination", there are the noise elimination methods we used in our research, i.e., BSS, STFT-based NF, WBSF of 2 kHz cut-off frequency, and ANF.

The code of Independent Component Analysis (ICA) in BSS is modified according to https://github.com/vsubhashini/ica.<br>
The code of Normalized Least Mean Squares (NLMS) algrithm in ANF is modified according to https://github.com/LiXirong/AdaptiveFilterandActiveNoiseCancellation.
