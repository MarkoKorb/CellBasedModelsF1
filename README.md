# Initial notes
The package did not seem to work with the newest version (1.11) of Julia because there were dependency issues. With Julia version 1.9 it can be installed and used.


# Examples
## Patterning
![Patterning Gif](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/patterning_example.gif)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| Defining complex functions and their many parameters can be daunting at first |  |

## ICM development
![ICM Development1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/icm_development_example.png)
![ICM Development2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/icm_development_proportions.png)
![ICM Development3](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/icm_development_statistics.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| @step: Fitting the model - Upload experimental data the authors want to read a csv file with data but it is not provided to the reader as far as I can tell. I can't continue implementing the example |  |

## Particle aggregation
![Particle Aggregation1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/particle_aggregation_repulsion_agents_example.png)
![Particle Aggregation2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/particle_aggregation_repulsion_boundaries_example.png)
![Particle Aggregation3](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/particle_aggregation_repulsion_diffusion_example.png)
![Particle Aggregation4](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/particle_aggregation_repulsion_statistics.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| The second last code block leads to a “nested task error: BoundsError” | Fix: Using a smaller SimBox (e.g. simBox = S.*[-5. 5; -5 5]) |

## Bacterial colony growth
![Growth1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/bacterial_colony_growth_two_bacterias_example.png)
![Growth2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/bacterial_colony_growth_growth_example.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| Can't initialize the community because there are errors with the (not) defined platform | Fix: I had to use CPU instead of GPU as platform |

## Bacterial chemotaxis
![Chemotaxis1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/bacterial_chemotaxis_example.png)
![Chemotaxis2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/bacterial_chemotaxis_statistics.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| Can't plot because the function "plotRods2D" is not defined, but shows up in the CellBasedModels documentation | Fix: Copy the code from the API and use it do define "plotRods2D" in your code |

---
---

# Discussion with group members
## Member 1


## Member 2


## Member 3


## Member 4
...
