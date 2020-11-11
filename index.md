# <center> FastSVC: Fast Cross-Domain Singing Voice Conversion with Feature-wise Linear Modulation</center>

## Abstract
This paper presents FastSVC, a light-weight cross-domain sing voice conversion (SVC) system, which is able to achieve high conversion performance, with inference speed 4x faster than real time on CPUs. FastSVC uses Conformer based phoneme recognizer to extract singer-agnostic linguistic features from singing signals. A feature-wise linear modulation based generator is used to synthesize waveform directly from linguistic features, leveraging information from sine-excitation signals and loudness features. The waveform generator can be trained conveniently using a multi-resolution spectral loss and an adversarial loss. Experimental results show that the proposed FastSVC system, compared with a computationally heavy baseline system, can achieve comparable conversion performance in some scenarios and significantly better conversion performance in other scenarios. Moreover, the proposed FastSVC system achieves desirable cross-lingual singing conversion performance. Inference speed of the FastSVC system is 30x and 70x faster than the baseline system on GPUs and CPUs, respectively.

## Brief introduction
- Singing voice conversion (SVC): convert the voice of one singer to that of other singers without changing the underlying content and melody.
- Cross-domain training: models are trained with speech dataset while conversion is conducted in the singing domain.
- Faster than real-time: able to conduct inference with a real-time factor (RTF) < 1.0 on modern CPUs.
- Any-to-many conversion: convert an arbitrary voice into a target singer’s voice within the finite singer set during training process.
- Cross-lingual conversion: convert singing voice in a language which is unseen during the training process.

