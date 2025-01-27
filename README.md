# Tienso - Segunda parte

La primera parte del proyecto constó en averiguar qué temáticas de contenido genera @tienso_ok para youtube y en función de la performance de cada una de ellas, sugerir al creador una temática a seguir para poder hacer crecer su canal de la manera más rápida posible.

En cambio, para la segunda parte del proyecto opté por hacer de cuenta que Youtube pierde el control de su plataforma y debe re-categorizar todos los videos de @tienso_ok como video regular o reel/short en función de la cantidad de likes y visitas de cada video. El objetivo no tiene nada que ver con la primera parte del proyecto, sin embargo, me permite seguir trabajando con el mismo dataset.

Para ello, elegí evaluar dos modelos de clasificación: KNeighbors y árboles de decisión.

A ambos los sometí a un método de validación cruzada para tener una primera idea de cuál podría funcionar mejor. Si hubiese evaluado más modelos, esto me hubiese permitido seleccionar sólo dos modelos para avanzar con el proceso de optimización de hiperparámetros.

Luego, optimicé los hiperparámetros de ambos modelos utilizando grid search. Los mejores hiperparámetros para ambos modelos fueron:
Para KNN: {'metric': 'manhattan', 'n_neighbors': 3, 'weights': 'uniform'}
Para Árbol de decisión: {'criterion': 'entropy', 'max_depth': 2, 'min_samples_split': 2}

Por último, obtuvimos la precisión y el F1 de cada modelo optimizado, siendo éstas:
Precisión KNN: 0.83
Precisión Árbol de decisión: 0.86
F1-Score KNN: 0.83
F1-Score Árbol de decisión: 0.87

Y pudimos concluir que el modelo de árboles de decisión es el que mejor se ajusta al dataset trabajado.


