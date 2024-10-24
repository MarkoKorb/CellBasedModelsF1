# Initial notes
The package did not seem to work with the newest version (1.11) of Julia because there were dependency issues. With Julia version 1.9 it can be installed and used.


# Examples
## Patterning
![Patterning Gif](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/patterning_example.gif)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| Defining complex functions and their many parameters can be daunting at first |  |
| It is quite hard to play around with the parameters as it is not easy to tell which parameter is what based on their names | Fix (kind of): Give ChatGPT the link to the example and ask it what the parameters in the code mean |
| Even after playing around with the parameters it is hard to tell what exactly a parameter does |  |

## ICM development
![ICM Development1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/icm_development_example.png)
![ICM Development2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/icm_development_proportions.png)
![ICM Development3](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/icm_development_statistics.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| @step: Fitting the model - Upload experimental data the authors want to read a csv file with data but it is not provided to the reader as far as I can tell. I can't continue implementing the example |  |
| Here it was hard to tell what parameter does what too. However some parameters were more easy to "decipher" than others. Some parameters were explained in the example code | Fix (kind of): Give ChatGPT the link to the example and ask it what the parameters in the code mean |

## Particle aggregation
![Particle Aggregation1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/particle_aggregation_repulsion_agents_example.png)
![Particle Aggregation2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/particle_aggregation_repulsion_boundaries_example.png)
![Particle Aggregation3](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/particle_aggregation_repulsion_diffusion_example.png)
![Particle Aggregation4](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/particle_aggregation_repulsion_statistics.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| The second last code block leads to a “nested task error: BoundsError” | Fix: Using a smaller SimBox (e.g. simBox = S.*[-5. 5; -5 5]) |

## Bacterial colony growth
![Growth1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/bacterial_colony_growth_two_bacterias_example.png)
![Growth2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/bacterial_colony_growth_growth_example.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| Can't initialize the community because there are errors with the (not) defined platform | Fix: I had to use CPU instead of GPU as platform |

## Bacterial chemotaxis
![Chemotaxis1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/bacterial_chemotaxis_example.png)
![Chemotaxis2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/bacterial_chemotaxis_statistics.png)

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
