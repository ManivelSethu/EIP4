
/* Assignment 02 */ 

1. Model.evaluate output
[0.019846547819019178, 0.9946] 

2. Strategy /action
     * (removed bias in every convolution layer. ran the model and checked the output it was giving the similar output (~99.4) )
     * Channel size reduction: 
     For reducing the params less than 15K - targetted the layer before 1x1x10x32. (which is 26x3x3x32) because in 1x1x10 convolution 
     layer the mixing is going to happen after which the max pooling happening. experimented what is sufficient channel size - arrived \
     at - 26x3x3x 16 instead of 26x3x3x32. (param 4640 - 2304 = 2336 reduction) - reached around 13994 total param. 
     
     * to acheive exactly 99.4x - used 16 instead of 32. When used 20 instead of 32 the accuracy went more than 99.5x easily.
     
 3. EPOCHs
 Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 12s 195us/step - loss: 0.1206 - acc: 0.9494 - val_loss: 0.0363 - val_acc: 0.9894
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 8s 133us/step - loss: 0.1079 - acc: 0.9522 - val_loss: 0.0337 - val_acc: 0.9895
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 8s 132us/step - loss: 0.1006 - acc: 0.9538 - val_loss: 0.0236 - val_acc: 0.9922
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 8s 136us/step - loss: 0.0960 - acc: 0.9563 - val_loss: 0.0301 - val_acc: 0.9922
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 8s 134us/step - loss: 0.0932 - acc: 0.9571 - val_loss: 0.0284 - val_acc: 0.9922
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0934 - acc: 0.9551 - val_loss: 0.0267 - val_acc: 0.9920
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 8s 130us/step - loss: 0.0890 - acc: 0.9571 - val_loss: 0.0233 - val_acc: 0.9936
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 8s 131us/step - loss: 0.0882 - acc: 0.9580 - val_loss: 0.0236 - val_acc: 0.9935
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0895 - acc: 0.9564 - val_loss: 0.0242 - val_acc: 0.9933
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0876 - acc: 0.9568 - val_loss: 0.0207 - val_acc: 0.9936
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 8s 134us/step - loss: 0.0857 - acc: 0.9570 - val_loss: 0.0195 - val_acc: 0.9944
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0841 - acc: 0.9581 - val_loss: 0.0209 - val_acc: 0.9946
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0843 - acc: 0.9579 - val_loss: 0.0199 - val_acc: 0.9946
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 8s 134us/step - loss: 0.0812 - acc: 0.9599 - val_loss: 0.0202 - val_acc: 0.9944
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0825 - acc: 0.9578 - val_loss: 0.0216 - val_acc: 0.9934
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0822 - acc: 0.9592 - val_loss: 0.0202 - val_acc: 0.9938
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0813 - acc: 0.9579 - val_loss: 0.0225 - val_acc: 0.9937
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0829 - acc: 0.9580 - val_loss: 0.0235 - val_acc: 0.9932
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0820 - acc: 0.9584 - val_loss: 0.0206 - val_acc: 0.9945
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0786 - acc: 0.9596 - val_loss: 0.0198 - val_acc: 0.9946

<keras.callbacks.History at 0x7f8375c045c0>
