# Model-SkinSavvy


Dataset for skinsavvy model machine learning : https://drive.google.com/drive/u/1/folders/1Yf9PHAZm8HMfIMK6kDbzh1z8lQYJ2nnL 

base_model = ResNet50(weights='imagenet', include_top=False, input_shape=(image_height, image_width, 3))

layers :
    base_model,
    GlobalAveragePooling2D(),
    Dense(256, activation='relu'),
    BatchNormalization(),
    Dropout(0.5),  # Dropout untuk mengurangi overfitting
    Dense(num_classes, activation='softmax')

optimizer='adam', 
loss='categorical_crossentropy',