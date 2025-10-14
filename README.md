# Driving scenario generation and evaluation using a structured layer representation and foundational models.
----

## Abstract
Rare and challenging driving scenarios are critical for autonomous vehicle development. Since they are difficult to encounter, simulating or generating them using generative models is a popular approach. Following previous efforts of structuring driving scenario representations in a layer model, we propose a structured five-layer model to improve evaluation and generation of rare scenarios. We use this model alongside large foundational models to generate new driving scenarios using a data augmentation strategy. Unlike previous representations, our structure introduces subclasses and characteristics for every agent of the scenario, allowing us to compare them using an embedding in our layer-model space. We study and adapt two metrics to evaluate the relevance of a synthetic dataset in the context of a structured representation: the diversity score estimates how different the scenarios of a dataset are from one another, while the originality score calculates how similar a synthetic dataset is from a real reference set. This paper showcase both metrics in different generation setup, as well as a qualitative evaluation of synthetic videos generated from structured scenario descriptions.

## Video generation example with Veo3

Real reference scene from the nuScenes-mini dataset:
[![Watch the video](https://raw.githubusercontent.com/Valgiz/5LM_Scene_gen/main/thumbnails/n008-2018-08-01-15-16-36-0400__CAM_FRONT__1533151603512404.jpg)](https://raw.githubusercontent.com/Valgiz/5LM_Scene_gen/main/videos/real_scene.avi)


## Experimental results



|                   | Metric |  L1  |  L2  |  L3  |  L4  |  L5  |
| ------            |     ------   |   ------   | ------     |   ------   |    ------  |    ------  |
| Generated  Scenes |   CO   | 0.93 | 0.59 | n/a  | 0.85 | 0.81 |
|                   |   CD   | 0.68 | 0.18 | n/a  | 0.63 | 0.50 |
|                   |        |      |      |      |      |      |
| Reference Scenes  |   CD   | 0.54 | 0.64 | n/a  | 0.91 | 0.52 |
