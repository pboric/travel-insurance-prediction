# Travel Insurance Prediction

Which customers buy travel insurance? Exploratory analysis, hypothesis tests and classification models on data
about 1,987 customers of a travel company (age, employment, income, family size, chronic diseases and travel
history).

## Results

Test set of 398 customers (35 % buyers). The models use the two features most clearly linked to buying insurance,
annual income and whether the customer has travelled abroad:

| Model | Accuracy | Recall for buyers | Precision for buyers |
|---|---:|---:|---:|
| **Random Forest** | **0.79** | 0.45 | 0.93 |
| SVM | 0.78 | 0.47 | 0.86 |
| Logistic regression | 0.69 | 0.56 | 0.57 |

Random Forest has the best accuracy, but it finds fewer than half of the buyers; logistic regression finds more of
them at the cost of many false positives. The right choice depends on whether missing a buyer or contacting a
non-buyer is more costly.

## Key findings

- Customers with higher annual income, frequent flyers and those who have travelled abroad are much more likely to
  buy travel insurance.
- Hypothesis tests show that age and income are significantly related to buying; family size is not.

## Repository

| File | Content |
|---|---|
| [`Travel_Insurance_Prediction.ipynb`](Travel_Insurance_Prediction.ipynb) | EDA, hypothesis tests, model training with grid search and evaluation |
| `TravelInsurancePrediction.csv` | The dataset |

## Run it

```bash
pip install -r requirements.txt
jupyter notebook Travel_Insurance_Prediction.ipynb
```

## Limitations

Using only two features keeps the model simple and explainable, but it leaves out information (such as employment
type and frequent-flyer status) that could improve recall.

## License

MIT
