# 2 — The Technology Behind Autonomous Driving

> Source: "Autonomy" by Lawrence D. Burns and Christopher Shulgan

## The Sensor Stack

Autonomous vehicles use a combination of sensors that work together to create a complete picture of the environment. Each sensor compensates for the weaknesses of others.

> **Case: The LiDAR Breakthrough** (Chapter on Sensors): "LiDAR — Light Detection and Ranging — creates a 3D point cloud of the world around the vehicle by firing laser pulses and measuring their return time. Early LiDAR units cost $75,000 and were the size of a coffee can. Today's solid-state LiDAR costs a few hundred dollars and fits in the palm of your hand." Burns explains the key enabling technology.
> **Key takeaway**: The cost reduction of LiDAR is one of the most important technology trends in the autonomous vehicle industry. The exponential curve — from $75,000 to hundreds of dollars in 15 years — is what makes autonomous vehicles economically viable.

> **Case: The Sensor Fusion Problem** (Chapter on AI): "Each sensor has strengths and weaknesses. LiDAR works in the dark but struggles in rain. Cameras give color and texture but don't provide depth. Radar sees through fog but has low resolution. The AI system must fuse all these inputs into a single, coherent model of the world. This sensor fusion problem is one of the hardest in computer science." Burns describes the integration challenge.
> **Key takeaway**: No single sensor is sufficient. The magic of autonomous driving is not any one technology but the integration of all of them — and the AI system that makes sense of the combined data. This is why the problem is so hard.
