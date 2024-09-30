# How to use the Model
1) First load the model using
loaded_model = load_model("Drug_Model.keras")
2) Replace age, sex, bp, cholesterol, na_to_k with your actual input values (Using the Classes Given in ClassMapping)
single_input = np.array([[age, sex, bp, cholesterol, na_to_k]])
preprocessed_input = scaler.transform(single_input)  # Assuming you used a scaler to scale your data during training

# Use the loaded model to make predictions.

predictions = loaded_model.predict(preprocessed_input)
# Since you have a multi-class classification model, you may want to get the class with the highest probability
predicted_class = np.argmax(predictions)
# Print the predicted class
print("Predicted class:", predicted_class)

Model Accuracy:
Test Loss: 0.11488501727581024
Test Accuracy: 0.9750000238418579
