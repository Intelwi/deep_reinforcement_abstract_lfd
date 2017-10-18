# Deep Reinforcement Leanring of Abstract Reasoning from Demonstrations
Madison Clark-Turner

deep_reinforcement_abstract_lfd

The following repository contains a Deep Recurrent Q-Network (DRQN) architecture for use in high-level Learning from Demonstration (LfD) of human interactions. We specifically designed this network for use with an Applied Behavioral Analysis (ABA) social greeting behavioral intervention.



Usage
=============

In order to train the network you must list the directory containing traing files in the form of TFRecords in: X

While training the network our system will generate a checkpoint file every 10,000 iterations. You can train the model by executing:

  python model_trainer.py

Evaluation of a model can be performed by running 
  
  python evaluator.py
  
The live system can be run after a checkpoint file has been generated by executing:
  
  roslaunch nao_full_py.launch
  roslaunch dqn.launch
  
Dependencies
=============
The following libraries are used by this application:
- [Tensorflow 1.3.0](https://www.tensorflow.org/) - Deep network library
- [NumPy 1.13.3](http://www.numpy.org/), [SciPy 0.19.1](http://www.scipy.org/) - Python numerical libraries
- [OpenCV2 2.4.8](https://opencv.org/) - Open Source image processing library
- [Librosa 0.5.1](https://librosa.github.io/librosa/index.html) - Music and audio analysis library
- [ROS Indigo](http://wiki.ros.org/) - (Robot Operating System) Robotics library

Acknowledgents
=============

We borrowed code from several sources for this project:

- Spectral Subtraction: https://github.com/tracek/Ornithokrites.git
- Inception Network: https://github.com/tensorflow/models.git
