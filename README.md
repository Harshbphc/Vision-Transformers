# Vision-Transformers

My project on Vision Transformer research paper. I have run the various experiments given in the research paper. Although I could not completely mimic those experiments because of hardware constraints such as RAM.

I have run various experiments given in the research paper and evaluated performance for each model separately by graphing model train accuracy, validation accuracy and then evaluated on the test set.

## Experiment 1

Running it on beta1=0.9, beta2 = 0.999 and Adam optimizer.


![image](https://user-images.githubusercontent.com/92864931/217338713-aa27eb5f-bb1e-4757-85d8-b9a37d22b624.png)

Train set - loss: 0.7220 - accuracy: 0.7809 - top-5-accuracy: 0.9650 - val_loss: 1.9957 - val_accuracy: 0.5374 - val_top-5-accuracy: 0.8042

Test set - loss: 1.9615 - accuracy: 0.5401 - top-5-accuracy: 0.8062



