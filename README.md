# Datasets for M1: Programming and Machine Learning

Teaching copies of the data used in the module's notebooks. Each notebook reads its file straight from this
repository, for example:

```python
data_url = "https://raw.githubusercontent.com/martynharris-lab/datasets/refs/heads/main/penguins.csv"
penguins = pd.read_csv(data_url)
```

## Unit 2

| File | Source | Licence |
|---|---|---|
| `airbnb_*.csv` | Inside Airbnb, Geneva (and Zurich reviews), https://insideairbnb.com/get-the-data/ | CC BY 4.0 |

## Unit 3

| File | Notebook | Source | Licence |
|---|---|---|---|
| `pulsars.csv` | 01_classifier-pulsars | HTRU2 survey: Lyon, R.J., Stappers, B.W., Cooper, S., Brooke, J.M. and Knowles, J.D. (2016) 'Fifty years of pulsar candidate selection', *Monthly Notices of the Royal Astronomical Society*, 459(1), pp. 1104-1123. UCI Machine Learning Repository, dataset 372. **Changed:** columns renamed, values rounded to three places. | CC BY 4.0 |
| `gapminder.csv` | 02_regression-gapminder | Gapminder (www.gapminder.org), via the `gapminder` package extract by Jennifer Bryan (https://github.com/jennybc/gapminder). 142 countries, every five years from 1952 to 2007. **Changed:** columns renamed; life expectancy rounded to 0.1 years and income to whole dollars. | CC0 (extract); Gapminder data CC BY 4.0 |
| `federalist_papers.csv` | 03_clusters-federalist | Counts of eight small words per 1,000 words in each of the 85 Federalist Papers (1787-88), made from Project Gutenberg eBook #1404. Method after Mosteller, F. and Wallace, D.L. (1963) 'Inference in an authorship problem', *JASA*, 58(302), pp. 275-309. | Public domain (source text) |
| `penguins.csv` | 04_resampling-and-pipelines-penguins | Horst, A.M., Hill, A.P. and Gorman, K.B. (2020) *palmerpenguins*. Original study: Gorman, K.B., Williams, T.D. and Fraser, W.R. (2014) *PLoS ONE*, 9(3), e90081. **Changed:** the two birds with no body measurements dropped; missing sex recorded as "unknown". | CC0 1.0 |

## Unit 4

| File | Notebook | Source | Licence |
|---|---|---|---|
| `har_signals.csv.gz` | 01_network-components-har, 02_architectures-har | Anguita, D., Ghio, A., Oneto, L., Parra, X. and Reyes-Ortiz, J.L. (2013) 'A public domain dataset for human activity recognition using smartphones', *ESANN 2013*, pp. 437-442. UCI Machine Learning Repository, dataset 240 (Human Activity Recognition Using Smartphones). 30 people, a phone at the waist, six activities, 50 readings a second. One row per reading: `person`, `window`, `group` (the original train or test set), `activity`, `time` (seconds into that person's recording) and nine channels: `acc_x/y/z` (acceleration with gravity), `body_acc_x/y/z` (without gravity), `gyro_x/y/z` (rotation). **Changed:** the original 2.56-second windows overlap by half; only every other window in each unbroken stretch of one activity is kept (5,351 of 10,299), so each person's rows read as one recording; sorted by person and time; signals rounded to 5 places; gzipped (pandas reads it as it is). Made by `prep/prepare_har.py` in the Unit 4 folder. | CC BY 4.0 |
| `har_features.csv.gz` | 01_network-components-har, 02_architectures-har | The same source: the 561 features the authors computed from each window, for the same 5,351 windows, with `person`, `window`, `group` and `activity`. **Changed:** rounded to 4 places; duplicated feature names get their feature number added. Made by the same script. | CC BY 4.0 |
| `sms_spam.csv` | earlier SMS version of the Unit 4 notebooks (archived) | SMS Spam Collection: Almeida, T.A., Gómez Hidalgo, J.M. and Yamakami, A. (2011) 'Contributions to the study of SMS spam filtering: new collection and results', *Proceedings of the 11th ACM Symposium on Document Engineering*, pp. 259-262. UCI Machine Learning Repository, dataset 228. 5,574 messages, 747 spam. **Changed:** the tab-separated file saved as CSV with columns `label` (ham or spam) and `text`; no rows dropped, no text edited. Made by `prep/prepare_sms_spam.py` in the Unit 4 folder. | CC BY 4.0 |
