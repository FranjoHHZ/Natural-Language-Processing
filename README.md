# Natural-Language-Processing

In dieser Übungsaufgabe verwenden wir eine Pipeline, um Yelp Reviews zu analysieren und automatisch in zwei Kategorien zu klassifizieren: 1-Sterne- und 5-Sterne-Bewertungen. Dabei nutzen wir die Textinhalte der Bewertungen, um zu lernen, wie man zwischen guten und schlechten Bewertungen unterscheiden kann. Wir nutzen Yelp Review Daten von Kaggle.
 
Jede Beobachtung in dem Datensatz ist eine bestimmte Bewertung eines bestimmten Geschäfts durch einen bestimmten Nutzer.

Die "stars" Spalte beinhaltet die Anzahl der Sterne (1 bis 5) die der Bewerter dem Geschäft verliehen hat. In anderne Worten: Die Bewertung des Geschäfts durch den Autor.

Die "cool" Spalte beinhaltet die Anzahl der "Cool"-Votes der Bewertung durch andere Nutzer.

Alle Bewertungen starten mit 0 "Cool"-Votes und es gibt nach oben kein Limit. Je mehr Leute die Bewertung "Cool" finden und sie so voten, desto höhere die Anzahl.

Für die "useful" (dt. nützlich) und "funny" (dt. witzig) Spalten gilt das gleiche.

# Ausführung
Um dieses Jupyter Notebook erfolgreich auszuführen, öffnen Sie den untenstehenden Binder Bagde Link. Folgen Sie den Anweisungen innerhalb des Notebooks, um die Daten zu laden, vorzuverarbeiten, die Modelle zu trainieren und die Ergebnisse zu evaluieren.
Die Pipeline besteht aus den folgenden Schritten:
1. **CountVectorizer**: Wandelt den Text in eine numerische Darstellung um, indem es die Häufigkeit jedes Wortes zählt.
2. **TfidfTransformer**: Verfeinert die numerische Darstellung, indem es häufige Wörter herunterstuft und seltene Wörter aufwertet.
3. **Multinomial Naive Bayes Classifier**: Führt die eigentliche Klassifikation durch, basierend auf den vorherigen Transformationen.

Um die Übungsaufgabe auszuführen:
1. Führen Sie zuerst die Pipeline mit den Trainingsdaten "X_train" und "y_train" durch, um das Modell zu trainieren. 
2. Verwenden Sie das trainierte Modell, um Vorhersagen für die Testdaten "X_test" zu treffen.
3. Bewerten Sie die Vorhersagen, indem Sie eine Confusion Matrix und einen Classification Report erstellen.

# Erwartete Ergbnisse

Nach dem Ausführen der Vorhersagen und der Evaluierung sollten Sie eine Confusion Matrix und einen Classification Report erhalten, die die Modellleistung anzeigen. In diesem Fall zeigt das Ergebnis, dass das Modell Schwierigkeiten hat, die 1-Sterne-Bewertungen korrekt zu klassifizieren, da alle 1-Sterne-Bewertungen falsch als 5-Sterne-Bewertungen eingestuft wurden. Die Precision, Recall und F1-Score für die 5-Sterne-Kategorie sind jedoch hoch (0,81 bis 1,00).

Das Ergebnis zeigt auch, dass die Verwendung von TF-IDF (Term Frequency-Inverse Document Frequency) möglicherweise die Ergebnisse verschlechtert hat, da die Unterscheidungskraft zwischen den beiden Kategorien verringert wurde. Weitere Versuche könnten beinhalten, die Pipeline-Anpassungen wie die Verwendung eines anderen Analyzers oder Modells auszuprobieren.

# Binder Badge
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FranjoHHZ/Natural-Language-Processing/HEAD?labpath=3-Nlp_Projekt-Loesung.ipynb)
