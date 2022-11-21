---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Avatron : 3D Face Avatar and Voice Generation from Text



### Anonymous CVPR submission : Paper ID 8800

---------



<video controls style="width: 1200px"   ><source src='./assets/demo_intro.mp4' type='video/mp4'></video>

## Abstract

We propose a novel 3D facial animation model that does not require explicit temporal synchronization between talking faces and speech. Our model presents a solution to a chronic problem that exists in current speech-driven 3D facial animation. Due to time domain differences between videos and speech, most approaches apply downsampling or upsampling to linguistic features from a pre-trained automatic speech recognition (ASR) model, resulting in unnatural facial movements. However, we efficiently utilize intermediate features from a text-to-speech (TTS) model to solve this problem. We upsample the text embedding of a non-autoregressive TTS model to the length of a mel-spectrogram and feed it into an avatar model to be converted to the vertices of a 3D face avatar. Since our proposed model does not require an ASR model, we are able to reduce the number of parameters and computational complexity of the whole solution. GAN-based training is also used to obtain vivid human-like facial movements. Our model demonstrates good effectiveness and performance in terms of normalized vertices mean error, as well as two subjective evaluations, SMOS and MOS.

-----------

------------



## Normalized Vertices Mean Error (NVME)

We compute vertices error between the reference and predicted 3D face mesh. The difference between the 3D mesh from the reference is represented by its color. The bluer the color of the 3D mesh, the smaller the difference, and the red the mesh, the larger the difference. Avatron shows a smaller overall error than FaceFormer. We colorize 3D mesh using an average error of three vertices which consist of each face. 

### Avatron vs. Faceformer

| <video controls style="width: 1200px"><source src='./assets/nvme/01.mp4' type='video/mp4'></video> |
| :----------------------------------------------------------: |
| <video controls style="width: 1200px"><source src='./assets/nvme/02.mp4' type='video/mp4'></video> |
| <video controls style="width: 1200px"><source src='./assets/nvme/03.mp4' type='video/mp4'></video> |
| <video controls style="width: 1200px"><source src='./assets/nvme/04.mp4' type='video/mp4'></video> |

<pre>
  

</pre>

## Similarity Mean Opinion Score (SMOS)

We provide three samples of FaceFormer and Avatron with reference. All samples from FaceFormer move around the mouth only, so they can convey linguistic information, but they do not describe a facial expression. In contrast, Avatron's samples provide not only context but also facial movements, making avatars more natural.

### Avatron vs Faceformer

|                          Reference                           |                          Faceformer                          |                           Avatron                            |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| <video controls style="width: 400px" ><source src='./assets/ava_face/reference/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/faceformer/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/avatron/01.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/ava_face/reference/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/faceformer/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/avatron/02.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/ava_face/reference/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/faceformer/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/avatron/03.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/ava_face/reference/04.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/faceformer/04.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/avatron/04.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/ava_face/reference/05.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/faceformer/05.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_face/avatron/05.mp4' type='video/mp4'></video> |

<pre>



</pre>

## Ablation study: Advantage of TTS

We generate speech samples with modified speaking speeds and their corresponding 3D facial animations. We are able to control the tempo of the sample (slowing or speeding up) by controlling the estimated phoneme duration from the predictor in Avatron. FaceFormer cannot control the avatar tempo because it used the fixed-length speech as input.

|                            Normal                            |                             Fast                             |                             Slow                             |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| <video controls style="width: 400px"   ><source src='./assets/ablation_speed/normal/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ablation_speed/fast/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ablation_speed/slow/01.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/ablation_speed/normal/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ablation_speed/fast/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ablation_speed/slow/02.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/ablation_speed/normal/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ablation_speed/fast/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ablation_speed/slow/03.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/ablation_speed/normal/04.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ablation_speed/fast/04.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ablation_speed/slow/04.mp4' type='video/mp4'></video> |

<pre>
  

</pre>



## Ablation study: Effect of GAN-based training crietrion

The GAN-based training method helps the model generate facial movements that are more similar to the reference in terms of facial expressions.

|                          Reference                           |                       Avatron w/o GAN                        |                           Avatron                            |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| <video controls style="width: 400px"   ><source src='./assets/ava_nogan/reference/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_nogan/avatron_nogan/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_nogan/avatron/01.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/ava_nogan/reference/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_nogan/avatron_nogan/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/ava_nogan/avatron/02.mp4' type='video/mp4'></video> |

<pre>

</pre>



## Mean Opinion Score (MOS)

We provide two samples of FaceFormer and Avatron with reference. Unlike SMOS samples, MOS samples are generated from duration predictor of TTS. Because of one-to-many mapping problem, reference and others have different durations. Avatron's performance does not lag behind even though it contains only 48.5% of the parameters compared to FaceFormer. 

|                          Reference                           |                          Faceformer                          |                           Avatron                            |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| <video controls style="width: 400px"   ><source src='./assets/mos/ref_select/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/mos/ff_select/01.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/mos/ava_select/01.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/mos/ref_select/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/mos/ff_select/02.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/mos/ava_select/02.mp4' type='video/mp4'></video> |
| <video controls style="width: 400px"   ><source src='./assets/mos/ref_select/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/mos/ff_select/03.mp4' type='video/mp4'></video> | <video controls style="width: 400px"   ><source src='./assets/mos/ava_select/03.mp4' type='video/mp4'></video> |



