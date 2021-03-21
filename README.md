# Custom-Image-Manipulation
This repository contains some custom python code that has been used for a robotics project in which the robot had to detect some specific object inside an envirnoment and navigate towards or away from them.

The notebook contains some classe for the following tasks:
- **Image Segmentation** (implemented through K-means segmentation).
- **Blob Detection** (implemented through recursive and iterative exact methods but also an approximate algorithm).
- **Image Pixelation** (decrease an image definition by extracting the median color in a given area).

The code has been then tested with my laptop webcam, taking some colors as input (extracted by the square at the center of the webcam image) and then tracking it.
All the algorithms have been tested with some coloured objects.

## Experiments

### Blob detection and Object tracking

![recursiveAlg](https://user-images.githubusercontent.com/36633875/111853047-9dd37200-8919-11eb-85f6-0a76e11168de.gif)<br>
***Recursive Algorithm**: here the algorithm tracks a blue joystick. Even though this algorithm is quite precise, it requires a lot of computational effort, especially for big images.*

![iterativeAlg](https://user-images.githubusercontent.com/36633875/111853214-57324780-891a-11eb-8442-acd8e76b26f7.gif)<br>
***Iterative Algorithm**: the recognition is noisier (a lot of small boxes appear in the image) but it can be observed a faster execution of the image processing.*

![sectorsAlg](https://user-images.githubusercontent.com/36633875/111853284-9bbde300-891a-11eb-99b1-04b1a334790c.gif)<br>
***Sectorized Algorithm**: in this case the algorithm highlights fixed image cells whenever the ratio of pixels matching the color bounds overcomes a fixed threshold. It is the less accurate method, but it is memory and time efficient.*
