## Inhaltsverzeichnis

- [Zielsetzung](#zielsetzung)
- [Cartpole Game](#cartpole-game)
- [Ansatz](#ansatz)
- [Training](#training)
- [Evaluierung](#evaluierung)
- [Optimierung](#optimierung)
- [Verwendete Quellen](#verwendete-quellen)
- [Voraussetzungen](#voraussetzungen)
- [Installation](#installation)
- [Anleitung](#anleitung)



## Zielsetzung

Das Ziel dieses Projekts bestand darin, das CartPole-Spiel mit Hilfe eines Rein-
forcement Learning-Ansatzes zu lösen. Reinforcement Learning ist eine Form des maschinel-
len Lernens, bei der ein Agent in einer Umgebung interagiert, Aktionen ausführt und Feedback
in Form von Belohnungen oder Bestrafungen erhält, um eine optimale Strategie zu erlernen.

## Cartpole Game

Das CartPole-Spiel besteht aus einem Wagen, der sich auf einer horizonta-
len Achse bewegen kann, und einem langen Pendel (Pole), das am Wagen befestigt ist. Ziel
des Spiels ist es, das Pendel so zu balancieren, dass es nicht nach unten fällt, indem der
Agent den Wagen nach links oder rechts bewegt. Das Spiel endet, wenn das Pendel einen
bestimmten Winkel überschreitet oder der Wagen eine bestimmte Position verlässt. Der Agent
erhält positive Belohnungen, solange das Pendel im Gleichgewicht gehalten wird, und negati-
ve Belohnungen, wenn das Spiel vorzeitig endet. Das CartPole-Spiel ist eine der klassischen
Umgebungen, die in OpenAI Gym enthalten sind.

## Ansatz 

Für dieses Projekt wurde bewusst der Q-Learning-Algorithmus gewählt, um den
Agenten zu trainieren. Q-Learning ist ein modellfreier Reinforcement-Learning-Algorithmus,
der sich für die Anwendung besonders eignet, da er die Fähigkeit besitzt, die Q-Funktion
zu nutzen, um die erwarteten Belohnungen für verschiedene Aktionen in einem bestimmten
Zustand zu schätzen. Die Q-Funktion fungiert als Wertfunktion und gibt die erwartete Ge-
samtbelohnung aus einem Zustand und einer bestimmten Aktion an. Diese Methode ist ideal, um das CartPole-Spiel effektiv zu lösen und die besten Aktionen zu erlernen, die das Pendel im Gleichgewicht halten.

## Training
Nachdem die QLearningAgent-Klasse und ihre Funktionen implementiert wurden, konnte der ei-
gentliche Trainings- und Testprozess für den Q-Learning-Agenten in der CartPole-Umgebung durch-
geführt werden. Der Agent wird trainiert, indem er für eine bestimmte Anzahl von Episoden (hier
10.000 Episoden) trainiert wird. Der Agent spielt das Spiel, aktualisiert die Q-Tabelle basierend auf
den erhaltenen Belohnungen und den maximalen erwarteten Belohnungen für die verschiedenen
Zustände und Aktionen. Die Erkundungswahrscheinlichkeit wird nach jeder Episode abgebaut, um
den Fokus auf Ausnutzung (Exploitation) zu lenken. Die trainierte Q-Tabelle des Agenten wird in
eine Datei gespeichert, um sie für zukünftige Verwendung zu behalten. Dies ermöglicht es, den
Agenten zu einem späteren Zeitpunkt zu laden und erneut zu nutzen.

## Evaluierung

Der Agent spielt das Spiel, und die Gesamtbelohnung über die Testepisoden wird aufgezeichnet. Dies wird mehrmals durchgeführt,
und die durchschnittliche Belohnung über die Testepisoden wird berechnet. Die durchschnittliche
Belohnung von 22.493 über 1000 Testepisoden zeigt, dass der Agent im Laufe des Trainings eine
effektive Strategie entwickelt hat, um das CartPole-Spiel erfolgreich zu meistern. Die visualisierte
Lernkurve zeigt, dass die durchschnittliche Belohnung im Verlauf der Testepisoden zunimmt, was
auf eine kontinuierliche Verbesserung der Agentenleistung hinweist.

## Optimierung

Es gibt verschiedene Ansätze und Techniken, die angewendet werden können, um den Q-Learning-
Agenten weiter zu verbessern und seine Leistung im CartPole-Spiel zu optimieren und die gleich-
zeitig über das Hyperparameter-Tuning hinausgehen. Einige mögliche Verbesserungen sind:
- Deep Q-Networks: Statt einer Q-Tabelle kann der Agent ein neuronales Netzwerk verwen-
den, um die Q-Funktion zu approximieren, was die Handhabung komplexer Zustandsräume
ermöglicht.
- Experience Replay: Die Verwendung von Erfahrungs-und Wiederholungspuffern kann den
Trainingsprozess stabilisieren und die Effizienz verbessern.
- Fortgeschrittene Algorithmen: Policy Gradient oder Proximal Policy Optimization können un-
tersucht werden, um möglicherweise effizientere Lernverfahren zu erzielen

## Verwendete Quellen

Während der Entwicklung dieses Projekts wurden folgende Quellen verwendet:

- [Gym Documentation](https://www.gymlibrary.dev/environments/classic_control/cart_pole/) 

- [Tutorial (Repository)](https://github.com/JackFurby/CartPole-v0)
  
- [Medium Article](https://medium.com/analytics-vidhya/q-learning-is-the-most-basic-form-of-reinforcement-learning-which-doesnt-take-advantage-of-any-8944e02570c5)

- [Python Tutorial (Repository)](https://github.com/pythonlessons/CartPole_reinforcement_learning)
  
## Voraussetzungen

- Python 3.6 oder höher
- OpenAI Gym
- Weitere Abhängigkeiten werden in der `requirements.txt`-Datei aufgelistet.

## Installation

1. Klone das Repository auf einen lokalen Computer:

git clone https://github.com/aminaud/CartPoleGame.git

cd cartpole-q-learning

pip install -r requirements.txt

## Anleitung
- Führe die Datei cartpole.ipynb aus, um den Q-Learning-Agenten zu trainieren und das CartPole-Spiel zu spielen.
  









