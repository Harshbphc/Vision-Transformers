# Vision-Transformers

My project on Vision Transformer research paper. I have run the various experiments given in the research paper. Although I could not completely mimic those experiments because of hardware constraints such as RAM.

I have run various experiments given in the research paper and evaluated performance for each model separately by graphing model train accuracy, validation accuracy and then evaluated on the test set.

Link to the notebook- "link"

Link to the 5th experiment - "link2"

## Experiment 1

Running it with Adam optimizer, beta1=0.9, beta2 = 0.999 and Adam optimizer, learning rate = learning_rate = 0.001, weight_decay = 0.0001


![image](https://user-images.githubusercontent.com/92864931/217338713-aa27eb5f-bb1e-4757-85d8-b9a37d22b624.png)

Train set - loss: 0.7220 - accuracy: 0.7809 - top-5-accuracy: 0.9650 - val_loss: 1.9957 - val_accuracy: 0.5374 - val_top-5-accuracy: 0.8042

Test set - loss: 1.9615 - accuracy: 0.5401 - top-5-accuracy: 0.8062

This is a normal experiment with adam optimizer 

## Experiment 2

Running it with Adam optimizer, beta1=0.9, beta2 = 0.999 and Adam optimizer, learning rate = 0.02, weight_decay = 0.1, batch size = 256

![image](https://user-images.githubusercontent.com/92864931/217511736-74f01e67-15c5-4b47-aad1-d7a4c0a08828.png)


Train set - loss: 4.2087 - accuracy: 0.0536 - top-5-accuracy: 0.2033 - val_loss: 4.1920 - val_accuracy: 0.0620 - val_top-5-accuracy: 0.2152

Test set - loss: 4.1913 - accuracy: 0.0564 - top-5-accuracy: 0.2166

This experiment failed badly beacuse according to the paper I had to use a batch size of 4096 ideally but could not allocate a batch size of more than 256 due to hardware  constraints, and as the weight decay is high it didn't train properly.

## Experiment 3

Running it with SGD optimizer, learning rate = 0.01 and momentum = 0.9, batch size = 256

![image](https://user-images.githubusercontent.com/92864931/217513460-37bd67c1-eb0d-4804-b201-36a2f1245019.png)

Train set - loss: 1.0580 - accuracy: 0.6835 - top-5-accuracy: 0.9334 - val_loss: 1.7799 - val_accuracy: 0.5440 - val_top-5-accuracy: 0.8220

Test set - loss: 1.7567 - accuracy: 0.5474 - top-5-accuracy: 0.8191

The graph does not plateau and reached the said accuracy smoothly. It does not fit the training data that well but has the highest testing accuracy, implying it generalizes well on new data.

Though, according to the research paper adam should work better, the adam optimizer does fit well on the train set, but maybe due to difference in batch size (ideally batch size should have been 512), it did not perform as expected. 

## Experiment 4

Using hyperparameters of Experiment 1 with masking layers in patch encoding

![image](https://user-images.githubusercontent.com/92864931/217514008-49582432-1c91-4674-9c82-5753609004a0.png)

Train set - loss: 0.7439 - accuracy: 0.7748 - top-5-accuracy: 0.9629 - val_loss: 2.0098 - val_accuracy: 0.5418 - val_top-5-accuracy: 0.8054

Test set - loss: 2.0026 - accuracy: 0.5387 - top-5-accuracy: 0.8059

This architecture fits the train model better than the one in Exp 1 without masking by a small margin and the test results are almost similar




