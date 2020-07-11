# Simulating ideal two-pole pulses

For this task we aim to learn an analytical two-pole function using a neural network. The input of this network will be various paramters such as amplitude and time constants, and the network should output a corresponding time trace that is given by the two-pole function with the input parameters.

This task is a stepping stone towards building a full DMC neural network.

## Dataset 
See the ```data``` folder

## Scoring

Performance is ranked by ```1-sqrt(MSE)``` over the **entire** dataset (not just val or test):
```python
score = 1-np.sqrt(np.mean(np.square(traces-predicted_traces)))
```

## Submission

You should save your model as a Keras model using ```keras.models.save()```. Tarballs or ```.keras``` files are both accepted. Please submit a pull request if you have a model that performs better than the top model in the current ranking. For models that contain custom loss functions/layers, the ```compile=False``` option may be required when loading the model.


| Model Name | Score (%) |
| --- | --- |
| DenseNet-2pole | 99.28 |
