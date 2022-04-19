Good and bad controls
================
Emilio Berti
April 2022

# What are good and bad controls?

Good controls are variable that, when included into a statistical model,
help finding the true association among other variables. These are also
called *deconfounders*. Bad controls are variable that, when included
into a statistical model, introduce bias in the true association among
other variables. These are also called *confounders*. Good and bad
controls can be identified visually using causal diagrams, also called
directed acyclic graphs (DAGs).

# DAGs

DAGs represent the scientific model of the phenomenon of interest. They
are composed of nodes (e.g.,
![\\{X, Z, W, ..., Y\\}](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;%5C%7BX%2C%20Z%2C%20W%2C%20...%2C%20Y%5C%7D "\{X, Z, W, ..., Y\}"))
and edges (e.g.,
![\\{ X \\rightarrow Z, Z \\rightarrow W, ..., W \\rightarrow Y \\}](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;%5C%7B%20X%20%5Crightarrow%20Z%2C%20Z%20%5Crightarrow%20W%2C%20...%2C%20W%20%5Crightarrow%20Y%20%5C%7D "\{ X \rightarrow Z, Z \rightarrow W, ..., W \rightarrow Y \}")),
where the arrow
![\\{ X \\rightarrow Z\\}](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;%5C%7B%20X%20%5Crightarrow%20Z%5C%7D "\{ X \rightarrow Z\}")
denotes a (possible) direct causal relationship.

DAGs have three main motifs:

-   Mediators or **chains**:
    ![\\{ X \\rightarrow Z \\rightarrow Y \\}](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;%5C%7B%20X%20%5Crightarrow%20Z%20%5Crightarrow%20Y%20%5C%7D "\{ X \rightarrow Z \rightarrow Y \}").
-   Common causes or **forks**:
    ![\\{ X \\leftarrow Z \\rightarrow Y \\}](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;%5C%7B%20X%20%5Cleftarrow%20Z%20%5Crightarrow%20Y%20%5C%7D "\{ X \leftarrow Z \rightarrow Y \}").
-   Common effects or **colliders**:
    ![\\{ X \\rightarrow Z \\leftarrow Y \\}](https://latex.codecogs.com/png.image?%5Cdpi%7B110%7D&space;%5Cbg_white&space;%5C%7B%20X%20%5Crightarrow%20Z%20%5Cleftarrow%20Y%20%5C%7D "\{ X \rightarrow Z \leftarrow Y \}").
