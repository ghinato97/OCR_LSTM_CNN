This project aims to develop an OCR usign Deep Learnign models. Specifically we create a model that combine CNN ( Convolutionale Neural Networks ) and LSTM ( Long Short Term Memory).
As dataset, black and white alphanumeric images were used.(28 x 28 pixels)

# Model Description
| Layer (type)                  | Output Shape       | Param #     |
|-------------------------------|--------------------|-------------|
| conv2d (Conv2D)               | (None, 28, 28, 32) | 320         |
| max_pooling2d (MaxPooling2D)  | (None, 13, 13, 32) | 0           |
| conv2d_1 (Conv2D)             | (None, 13, 13, 64) | 18,496      |
| max_pooling2d_1 (MaxPooling2D)| (None, 6, 6, 64)   | 0           |
| batch_normalization (BatchNormalization) | (None, 6, 6, 64) | 256  |
| reshape (Reshape)             | (None, 1, 2304)    | 0           |
| bidirectional (Bidirectional) | (None, 1, 256)     | 2,491,392   |
| bidirectional_1 (Bidirectional)| (None, 1, 256)    | 394,240     |
| flatten (Flatten)             | (None, 256)        | 0           |
| dense (Dense)                 | (None, 128)        | 32,896      |
| dense_1 (Dense)               | (None, 47)         | 6,063       |

 Total params: 2,943,663

