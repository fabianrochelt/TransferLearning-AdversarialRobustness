# TransferLearning-AdversarialRobustness
Wie beeinflusst Transfer Learning die Adversarial Robustness von neuronalen Netzen

## Genrelle Informationen
Sämtliche Files in diesem Reopsitory stehen als Jupyter Notebook Dateien .ipynb zur Verfügung. Für die Implementierung wurde Python 3.8.5 verwendet welches durch die Anaconda3 Distribution bereitgestellt wird.
## Installation
Anaconda und Environment nach dieser [Anleitung](https://phoenixnap.com/kb/how-to-install-anaconda-ubuntu-18-04-or-20-04) einrichten.
### Tensorflow (Version 2.4.1) und Tensorflow Datasets (Version 3.1.0)
```python
conda install tf
```
### Activate Tensorflow für dedizierte Verwendung der GPU
```python
conda create -n tf-gpu tensorflow-gpu
conda activate tf-gpu
```
### Tensorflow Datasets (Version 3.1.0)
```python
conda install tensorflow-datasets==3.1.0
```
### Skicit-Learn (Version 0.24.2)
```python
conda install scikit-learn
```
### Eagerpy (Version 0.29.0)
```python
conda install eagerpy
```
### Matplotlib (Version 3.4.1)
```python
conda install matplotlib
```
### Foolbox (Version 3.3.1)
```python
conda install foolbox
```
### Pandas (Version 1.2.4)
```python
conda install pandas
```
## Verwendung
In jedem Ordner gibt es zwei Jupyter Notebook Files eines für das Modell ohne Transfer Learning und eines für das Modell mit Transfer Learning.
Wenn alle Pakete mit der korrekten Version installiert wurden, lassen sich die einzelnen Zellen nacheinander ausführen.

Ablauf ohne Transfer Learning:
- Laden des Datensatzes
- Erstellung der CNN Architektur
- Training und Speicherung von 10 Modellen mit 10-Fold Cross Validation
- Evaluierung der Modelle
- Foolbox Angriff auf eines der 10 Modelle
- Ausgabe der Ergebnisse in Jupyter Notebook und Excel

Ablauf mit Transfer Learning:
- Laden der Datensätze
- Erstellung der CNN Architektur
- Trainings des Modells in einem Durchlauf und 50 Epochen
- Evaluierung des Modells und Speicherung
- Transfer Learning und Speicherung von 10 Modellen mit 10-Fold Cross Validation mit Hilfe Basismodell
- Evaluierung der 10 Modelle
- Fine Tuning eines der 10 Modelle
- Foolbox Angriff auf eines der 10 Modelle
- Ausgabe der Ergebnisse in Jupyter Notebook und Excel

## Mitwirkung
Pull requests sind willkommen. FÜr größere Änderungen bitte zuerst einen Issue erstellen um die Anpassungen zu diskutieren.
