1 Introduction

Motivation

Unternehmen sind zunehmend daran interessiert, die Kundenzufriedenheit in Echtzeit zu erfassen. Klassische Methoden wie Umfragen sind aufwendig und bieten kein unmittelbares Feedback. Durch die automatisierte Analyse von Gesichtsausdrücken mithilfe von Machine Learning kann ein System entwickelt werden, das die Stimmung von Kunden erkennt und so wertvolle Erkenntnisse über das Kundenerlebnis liefert.

Define your research question

Kann ein Machine-Learning-Modell automatisiert anhand von Gesichtsausdrücken erkennen, ob ein Kunde zufrieden oder unzufrieden ist?

How is this document structured

Zunächst wird verwandte Arbeit diskutiert. Anschließend folgen die Beschreibung der Methodik, der verwendeten Daten, die Modellierung und die Evaluation. Danach werden die Ergebnisse dargestellt und abschließend diskutiert.

2 Related Work

Emotionserkennung durch Gesichtsausdrücke ist ein aktives Forschungsfeld. Das FER2013-Datenset wurde in zahlreichen Arbeiten zur Gesichtsanalyse verwendet. CNN-Architekturen wie VGGNet oder ResNet haben in der Vergangenheit hohe Genauigkeiten bei der Klassifikation von Gesichtsausdrücken erreicht. Ein Beispiel ist die Arbeit von Mollahosseini et al. (2017), die ein Deep Neural Network mit dem AffectNet-Datensatz trainierten.

3 Methodology

3.1 General Methodology

Auswahl eines geeigneten Datensatzes (FER2013)

Vorverarbeitung der Bilder (Normalisierung, Augmentierung)

Modellwahl (Convolutional Neural Network)

Training und Evaluierung des Modells

Anwendung des Modells auf unbekannte Bilder

3.2 Data Understanding and Preparation

Datensatz: FER2013 (Kaggle)

Enthält ca. 35.000 Bilder (48x48 Pixel, Graustufen)

Emotionen: "Angry", "Disgust", "Fear", "Happy", "Sad", "Surprise", "Neutral"

Vorbereitung: One-hot-Encoding der Labels, Normalisierung der Pixelwerte, Datenaugmentation zur Erhöhung der Vielfalt

3.3 Modeling and Evaluation

Modell: Einfaches CNN mit 3 Convolutional-Blöcken und Dense-Layern

Trainingsverfahren: Adam-Optimizer, Cross-Entropy Loss

Metriken: Accuracy, Confusion Matrix, Precision, Recall, F1-Score

4 Results

Implementierung eines funktionierenden Modells in Python mit TensorFlow/Keras

Modell erreicht auf dem Validierungsset eine Genauigkeit von ca. 65%

Beispielhafte Anwendung auf neuen Bildern zeigt plausible Ergebnisse

Verwendung von Streamlit zur Erstellung einer einfachen Web-App zur Emotionserkennung auf hochgeladenen Bildern

5 Discussion

Limitierungen: Der FER2013-Datensatz ist relativ klein und enthält nur Graustufenbilder. Bestimmte Emotionen wie "Disgust" sind unterrepräsentiert.

Ethische Überlegungen: Die automatische Emotionserkennung kann als Eingriff in die Privatsphäre empfunden werden. Zudem kann ein nicht-diverser Trainingsdatensatz zu diskriminierenden Modellergebnissen führen.

Transparenz: Es ist wichtig, dem Nutzer gegenüber transparent mit der Fehlerwahrscheinlichkeit und dem Einsatzzweck des Modells umzugehen.

Gesellschaftliche Auswirkungen: Positiv ist das Potenzial zur Verbesserung des Kundenerlebnisses; negativ die Gefahr des Missbrauchs zur Überwachung.

Weiterführende Forschung: Kombination von Gesichtsausdrücken mit Tonanalyse für multimodale Emotionserkennung, Anwendung auf Videos in Echtzeit, Erweiterung auf weitere Emotionen.


https://www.kaggle.com/datasets/msambare/fer2013
polars/pandas
