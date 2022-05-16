Я добавила код в свой train.py от прошлого модуля

X_test_in = pd.read_csv("data/test.csv")

y_predicted = pipeline.predict(X_test_in)

pd.DataFrame({"Id": X_test_in["Id"], "Cover_Type": y_predicted}).set_index(["Id"]).to_csv("data/submission.csv")


А вызывала:

poetry run train --ml-model 2 --n-estimators 1000 --use-feature-selection 2
