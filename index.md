# <center> FastSVC: Fast Cross-Domain Singing Voice Conversion with Feature-wise Linear Modulation</center>

<center> Anonymous </center>  

## Abstract
This paper presents FastSVC, a light-weight cross-domain sing voice conversion (SVC) system, which is able to achieve high conversion performance, with inference speed 4x faster than real time on CPUs. FastSVC uses Conformer based phoneme recognizer to extract singer-agnostic linguistic features from singing signals. A feature-wise linear modulation based generator is used to synthesize waveform directly from linguistic features, leveraging information from sine-excitation signals and loudness features. The waveform generator can be trained conveniently using a multi-resolution spectral loss and an adversarial loss. Experimental results show that the proposed FastSVC system, compared with a computationally heavy baseline system, can achieve comparable conversion performance in some scenarios and significantly better conversion performance in other scenarios. Moreover, the proposed FastSVC system achieves desirable cross-lingual singing conversion performance. Inference speed of the FastSVC system is 30x and 70x faster than the baseline system on GPUs and CPUs, respectively.

## Brief introduction
- Singing voice conversion (SVC): convert the voice of one singer to that of other singers without changing the underlying content and melody.
- Cross-domain training: models are trained with speech dataset while conversion is conducted in the singing domain.
- Faster than real time: able to conduct inference with a real-time factor (RTF) < 1.0 on modern CPUs.
- Any-to-many conversion: convert an arbitrary voice into a target singer’s voice within the finite singer set during training process.
- Cross-lingual conversion: convert singing voice in a language which is unseen during the training process.

## Compared systems
- UCD-SVC: unsupervised cross-domain singing voice conversion system, Adam Polyak et al.
- FastSVC (Ours)

## Any-to-One Cross-domain (A2O-CD) singing voice conversion
### Target speech reference samples from LJ-Speech.

| LJ002-0271 | LJ010-0295 | LJ028-0335 | LJ031-0224 | 
| :--- | :--- | :--- | :--- |
| <audio src="wavs/A2O-CD/LJ-refs/LJ002-0271.wav" controls preload></audio> | <audio src="wavs/A2O-CD/LJ-refs/LJ010-0295.wav" controls preload></audio> | <audio src="wavs/A2O-CD/LJ-refs/LJ028-0335.wav" controls preload></audio> | <audio src="wavs/A2O-CD/LJ-refs/LJ031-0224.wav" controls preload></audio> |
| --- | --- | --- | --- |

| Source | UCD-SVC | FastSVC (Ours) |
| :--- | :--- | :--- |
| <audio src="wavs/NUS-refs/ADIZ_18.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/ADIZ.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/ADIZ.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/NUS-refs/JLEE_11.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/JLEE.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/JLEE.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/NUS-refs/JTAN_07.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/JTAN.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/JTAN.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/NUS-refs/KENN_10.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/KENN.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/KENN.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/NUS-refs/MCUR_17.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/MCUR.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/MCUR.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/NUS-refs/MPOL_20.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/MPOL.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/MPOL.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/NUS-refs/MPUR_02.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/MPUR.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/MPUR.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/NUS-refs/NJAT_16.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/NJAT.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/NJAT.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/NUS-refs/PAMR_15.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/PAMR.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/PAMR.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/NUS-refs/SAMF_13.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/SAMF.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/SAMF.wav" controls preload></audio> |
| --- | --- | --- |
| <audio src="wavs/NUS-refs/VKOW_11.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/VKOW.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/VKOW.wav" controls preload></audio> | 
| --- | --- | --- |
| <audio src="wavs/NUS-refs/ZHIY_03.wav" controls preload></audio> | <audio src="wavs/A2O-CD/UCD-SVC/ZHIY.wav" controls preload></audio> | <audio src="wavs/A2O-CD/FastSVC/ZHIY.wav" controls preload></audio> | 
| --- | --- | --- |


## Any-to-Many Cross-domain (A2M-CD) singing voice conversion

## Any-to-Many In-domain (A2M-ID) singing voice conversion

## Cross-lingual (CL) singing voice conversion

| <audio src="wavs/NUS-refs/ADIZ_18.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/JLEE_11.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/JTAN_07.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/KENN_10.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/MCUR_17.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/MPOL_20.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/MPUR_02.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/NJAT_16.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/PAMR_15.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/SAMF_13.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/VKOW_11.wav" controls preload></audio> |
| <audio src="wavs/NUS-refs/ZHIY_03.wav" controls preload></audio> |
