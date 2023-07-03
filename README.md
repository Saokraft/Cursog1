# Cursog1 

```python
import tensorflow as tf

# Definir la estructura de la red neuronal
model = tf.keras.models.Sequential([
    tf.keras.layers.Dense(64, activation='relu', input_shape=(input_size,)),
    tf.keras.layers.Dense(64, activation='relu'),
    tf.keras.layers.Dense(num_classes, activation='softmax')
])

# Compilar el modelo
model.compile(optimizer='adam',
              loss=tf.keras.losses.SparseCategoricalCrossentropy(from_logits=True),
              metrics=['accuracy'])

# Entrenar el modelo
model.fit(x_train, y_train, epochs=10, validation_data=(x_val, y_val))

# Evaluar el modelo
test_loss, test_acc = model.evaluate(x_test, y_test)
print('Precisión en los datos de prueba:', test_acc)
```
