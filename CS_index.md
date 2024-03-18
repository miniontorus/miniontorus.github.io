---
layout: default
---

# CS Notes Compilation

A compilation of very terrible CS notes. 

## Machine Learning

Some key fragments of code worth noting down

### General Model Stuff
```python
# Define a random forest model and measuring mean absolute error
# Source: https://www.kaggle.com/code/mangominion/machine-learning-competitions
rf_model = RandomForestRegressor(random_state=1)
rf_model.fit(train_X, train_y)
rf_val_predictions = rf_model.predict(val_X)
rf_val_mae = mean_absolute_error(rf_val_predictions, val_y)
```

### Kaggle Specific
```python
# Outputing to proper format
output = pd.DataFrame({'Id': test_data.Id,
                       'SalePrice': test_preds})
output.to_csv('submission.csv', index=False)
```