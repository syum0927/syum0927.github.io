---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Avatron : 3D Face Avatar and Voice Generation from Text



### Anonymous CVPR submission : Paper ID 8800

---------



## Abstract

We propose a novel 3D facial animation model that does not require explicit temporal synchronization between talking faces and speech. Our model presents a solution to a chronic problem that exists in current speech-driven 3D facial animation. Due to time domain differences between videos and speech, most approaches apply downsampling or upsampling to linguistic features from a pre-trained automatic speech recognition (ASR) model, resulting in unnatural facial movements. However, we efficiently utilize intermediate features from a text-to-speech (TTS) model to solve this problem. We upsample the text embedding of a non-autoregressive TTS model to the length of a mel-spectrogram and feed it into an avatar model to be converted to the vertices of a 3D face avatar. Since our proposed model does not require an ASR model, we are able to reduce the number of parameters and computational complexity of the whole solution. GAN-based training is also used to obtain vivid human-like facial movements. Our model demonstrates good effectiveness and performance in terms of normalized vertices mean error, as well as two subjective evaluations, SMOS and MOS.

-----------

------------



## LVME

LVME is ~~. 

#### Avatron vs. Avatron-FC

| <video controls style="width: 1200px" loop=True ><source src='./assets/lvme_01/sample_01.mp4' type='video/mp4'></video> |
| :----------------------------------------------------------: |
|                                                              |
|                                                              |



#### Avatron vs. Faceformer

video sample

|      |
| ---- |
|      |
|      |



## SMOS

Description ~~. 

#### Avatron vs Faceformer

|                          Reference                           |                          Faceformer                          |                           Avatron                            |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/reference/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/faceformer/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/avatron/01.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/reference/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/faceformer/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/avatron/02.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/reference/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/faceformer/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/avatron/03.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/reference/04.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/faceformer/04.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/avatron/04.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/reference/05.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/faceformer/05.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/avatron/05.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/reference/06.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/faceformer/06.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_face/avatron/06.mp4' type='video/mp4'></video> |

---------



#### Avatron vs Avatron-noGAN

|                          Reference                           |                        Avatron-noGAN                         |                           Avatron                            |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/reference/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/avatron_nogan/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/avatron/01.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/reference/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/avatron_nogan/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/avatron/02.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/reference/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/avatron_nogan/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ava_nogan/avatron/03.mp4' type='video/mp4'></video> |



#### Speed Control

|                            Normal                            |                             Fast                             |                             Slow                             |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/normal/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/fast/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/slow/01.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/normal/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/fast/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/slow/02.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/normal/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/fast/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/slow/03.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/normal/04.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/fast/04.mp4' type='video/mp4'></video> | <video controls style="width: 400px" loop=True ><source src='./assets/ablation_speed/slow/04.mp4' type='video/mp4'></video> |

