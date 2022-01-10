# Competition3 Reverse-Image-Caption

We have 2 model versions about this homework that deal quite good performance. Depend on your requirement, you can select one of them to improve your performance.

    1. DL_comp3_Team123_model_without_BERT:
    
    - DCGAN (4 layers)
    - TextEncoder (1 caption)
    - Generator Dropout (0.5)
    - WGAN-GP Loss
    - 4x Data Augmentation
    - Normalization (127.5)

    2. DL_comp3_Team123_model_with_BERT:

    - DCGAN (3 layers)
    - BERT Encoder (10 captions)
    - Without Generator Dropout (0.5)
    - WGAN-GP Loss
    - No Data Augmentation
    - Normalization (127.5)
