SLT Arctic Corpus
=================

Demo data: 
----------
arctic_a0001 -- arctic_a0060 (60 utterances) <br/>
Data distribution: Train: 50; Valid: 5; Test: 5;

Full data: 
----------
arctic_a0001 -- arctic_b0539 (1132 utterances) <br/>
Data distribution: Train: 1000; Valid: 66; Test: 66;

RESULTS
=======

Baseline results from demo data
-------------------------------

Objective scores from duration model: <br/>
Labels: state_align; Network: [416->5] LR 0.002 [4 TANH] [4*512]; <br/>
Valid -- RMSE: 6.826 frames/phoneme; CORR: 0.624; <br/>
Test  -- RMSE: 7.840 frames/phoneme; CORR: 0.562;

Labels: phone_align; Network: [416->1] LR 0.002 [4 TANH] [4*512]; <br/>
Valid -- RMSE: 6.777 frames/phoneme; CORR: 0.633; <br/> 
Test  -- RMSE: 7.665 frames/phoneme; CORR: 0.593;

Objective scores from acoustic model: <br/> 
Labels: state_align; Network: [425->187], LR 0.002 [4 TANH] [4*512]; <br/>
Valid -- MCD: 6.559 dB; BAP: 0.242 dB; F0:- RMSE: 19.573 Hz; CORR: 0.529; VUV: 11.655%  <br/>
Test  -- MCD: 6.586 dB; BAP: 0.259 dB; F0:- RMSE: 15.309 Hz; CORR: 0.701; VUV: 8.821%

Labels: phone_align; Network: [420->187], LR 0.002 [4 TANH] [4*512]; <br/>
Valid -- MCD: 6.762 dB; BAP: 0.246 dB; F0:- RMSE: 19.433 Hz; CORR: 0.538; VUV: 11.403% <br/>
Test  -- MCD: 6.704 dB; BAP: 0.262 dB; F0:- RMSE: 15.264 Hz; CORR: 0.700; VUV: 8.907%


Baseline results from full data
-------------------------------

Objective scores from duration model: [416->5] LR 0.002 [4 TANH] [4*512] <br/>
Valid -- RMSE: 6.810 frames/phoneme; CORR: 0.758; <br/>
Test  -- RMSE: 6.330 frames/phoneme; CORR: 0.773;

Objective scores from acoustic model: [425->187] LR 0.002 [4 TANH] [4*512] <br/>
Valid -- MCD: 5.067 dB; BAP: 0.228 dB; F0:- RMSE: 11.186 Hz; CORR: 0.761; VUV: 6.312%  <br/>
Test  -- MCD: 5.070 dB; BAP: 0.238 dB; F0:- RMSE: 12.051 Hz; CORR: 0.752; VUV: 5.732%

