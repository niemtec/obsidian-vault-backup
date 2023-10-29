---
tags:
  - computer-science/artificial-intelligence
see also:
  - "[[Neural Networks]]"
source: https://techcrunch.com/2023/08/17/what-is-a-liquid-neural-network-really/?guccounter=1
---
* Liquid neural networks can stay adaptable, even after training based on the incoming inputs they receive.
* The "liquid" refers to the adaptability and flexibility of the networks.
* They tend to be significantly smaller than "solid" neural networks because they contain fewer but richer nodes.
	* They are less computationally expensive which means they can run on cheaper, and smaller, devices rather than depending on external devices.

> "A differential equation describes each node of that system. With the closed-form solution, if you replace it inside this network, it would give you the exact behaviour, as it’s a good approximation of the actual dynamics of the system. They can thus solve the problem with an even lower number of neurons, which means it would be faster and less computationally expensive."

- The natural application of this technology is in robotics control based on continuous-time observation, liquid neural networks can help improve the "reasoning" of robots.
- Another benefit is the [[Neural Network Black Box Question]] because smaller networks are much easier to understand.
	- Biases are a big factor in machine-learning applications because garbage input results in garbage output.
	- More transparency in the network plays an important role in identifying causalities.
- The big **downside** is that liquid systems require "time series" data as they don't extract necessary information from static images instead requiring a dataset that involves sequential data like video.
	> "The real world is all about sequences. Even our perception — you're not perceiving images, you're perceiving sequences of images. So time series data actually create our reality."