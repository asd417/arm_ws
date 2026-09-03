**Pick and Place**

![Metrics](./try2/setup.png)

The setup for the second trial applies the needed changes from the first attempt. The over-arching is now positioned so that the arm no longer occludes the object position like before.

The training however was still unsuccessful despite two different hyperparameter settings. The first setup uses learning rate of 1e-4 while the second uses 1e-5. The loss turned out to be lower for the higher learning rate, indicating that the low learning rate of 1e-5 quickly found the local minima. 

![Metrics1](./try2/metrics1.png)

![Metrics2](./try2/metrics2.png)


With the limited resource (a single laptop with RTX 3080), it is challenging to train optimally. To combat this, the next trial will simplify the task to picking up 1 object.

There was also a problem with the dataset as well. I was recording the dataset so each episode would include the 'return to idle position' action at the end of the episode however some reading showed that it is better to hold the final position of the robot for 2-3 seconds after the successful demonstration. I will address this issue in the next trial.