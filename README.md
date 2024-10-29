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

### Parameters
| Parameter | Explanation (ChatGPT) |
| :-------- | :-------------------- |
| λ (lambda) | Dispersion rate or decay factor for the morphogen gradient |
| a0 | Initial concentration or starting value of the morphogen substance |
| a1 | Could signify a normalization or distribution of a certain property in the system |
| τ (tau) | This is a time constant describing the rate of a reaction or change |
| l | Seems to be a characteristic length or distance |
| D | Diffusion coefficient for the morphogen gradient |
| S0 | May represent an initial or maximum value for a morphogen source or sink |
| τg (tau_g) | Time constant for gradient decay |
| L | System length that defines the size of the space |
| N | Number of discrete points or cells |

---

## ICM development
![ICM Development1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/icm_development_example.png)
![ICM Development2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/icm_development_proportions.png)
![ICM Development3](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/icm_development_statistics.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| @step: Fitting the model - Upload experimental data the authors want to read a csv file with data but it is not provided to the reader as far as I can tell. I can't continue implementing the example |  |
| Here it was hard to tell what parameter does what too. However some parameters were more easy to "decipher" than others. Some parameters were explained in the example code | Fix (kind of): Give ChatGPT the link to the example and ask it what the parameters in the code mean |

### Parameters
| Parameter | Explanation (ChatGPT) |
| :-------- | :-------------------- |
| α | Possibly a growth rate or a coefficient related to interaction strength between cells |
| K | Likely refers to a carrying capacity, the maximum population size that the environment can sustain |
| nn | Could represent the [Hill coefficient](https://en.wikipedia.org/wiki/Hill_equation_(biochemistry)) or the degree of interaction or cooperativity |
| mm | Could be another coefficient affecting the interaction term or steepness of a response curve |
| fRange | Likely defines a range for a function or a parameter that affects the extent of variability in some feature, possibly related to fitness or force range |
| mi | Possibly related to mass or initial cell size |
| ri | Could be a radius parameter, likely representing the initial size or distance in the model |
| b | Could represent a baseline birth rate or a background parameter in the model |
| k0 | Could be a rate constant, possibly for reactions or transitions within the model |
| fAdh | Likely an adhesion force parameter, representing the strength of the adhesive interactions between cells |
| μ | Likely a viscosity or friction coefficient |
| τDiv | Division time parameter |
| σDiv | Likely the standard deviation or noise in the division time |
| c0 | Initial concentration or density of a substance |
| σc | The standard deviation of the concentration |
| nCirc | Likely the number of cells in a circular configuration or arrangement |
| σNCirc | The standard deviation for nCirc |
| fMin | A minimum fitness or force threshold |
| fMax |  A maximum fitness or force threshold |
| fPrE | The proportion or fraction, possibly of a precursor or progenitor cell type |
| fEPI | The fraction or proportion of epithelial cells |
| τCirc | Possibly the time for a circular configuration or cycle to complete |
| στCirc | The standard deviation for the circular time |
| rESC | Radius or size of embryonic stem cells |
| f0 | Likely an initial force matrix or a parameter representing initial conditions for forces or interactions |

---

## Particle aggregation
![Particle Aggregation1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/particle_aggregation_repulsion_agents_example.png)
![Particle Aggregation2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/particle_aggregation_repulsion_boundaries_example.png)
![Particle Aggregation3](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/particle_aggregation_repulsion_diffusion_example.png)
![Particle Aggregation4](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/particle_aggregation_repulsion_statistics.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| The second last code block leads to a “nested task error: BoundsError” | Fix: Using a smaller SimBox (e.g. simBox = S.*[-5. 5; -5 5]) |
| It is quite hard to play around with the parameters as it is not easy to tell which parameter is what based on their names | Fix (kind of): Give ChatGPT the link to the example and ask it what the parameters in the code mean |

### Parameters
| Parameter | Explanation (ChatGPT) |
| :-------- | :-------------------- |
| rRep | The repulsion radius |
| fRep | The strength of repulsion |
| rAtr | The attraction radius |
| fAtr | The strength of attraction |
| αT | The "thermal" or randomness parameter, responsible for random movement |
| x | Specifies the x coordinates of the particles |
| y | Specifies the y coordinates of the particles |
| N | Number of particles |
| D | Diffusion coefficient |

---

## Bacterial colony growth
![Growth1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/bacterial_colony_growth_two_bacterias_example.png)
![Growth2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/bacterial_colony_growth_growth_example.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| Can't initialize the community because there are errors with the (not) defined platform | Fix: I had to use CPU instead of GPU as platform |
| It is quite hard to play around with the parameters as it is not easy to tell which parameter is what based on their names | Fix (kind of): Give ChatGPT the link to the example and ask it what the parameters in the code mean |

### Parameters
| Parameter | Explanation (ChatGPT) |
| :-------- | :-------------------- |
| m | A mass scaling factor, potentially representing the mass of the bacteria |
| g | A growth scaling factor, likely setting a reference growth rate for the bacteria |
| d | Could represent a diffusion or density characteristic |
| kn | Nutrient concentration or diffusion coefficient, calculated based on the interaction between mass, growth, and density |
| γn | A nutrient transport parameter, affecting how nutrients move or diffuse relative to bacterial growth |
| γt | Transport rate, likely controlling the rate at which other molecules, besides nutrients, are transported or diffuse within the environment |
| μcc | The cell-cell interaction rate |
| μcw | The cell-wall interaction rate |
| β | A growth control factor, influencing the overall growth rate or replication frequency of bacterial cells |
| βω | A similar growth control factor, possibly focused on a specific aspect of bacterial growth, like wall expansion or replication |
| growth | The effective growth rate, which scales bacterial growth according to the product of growth, diffusion, and a set multiplication factor |
| lMax | The maximum allowable cell length |
| σlTarget | The standard deviation for cell length |
| α | An interaction strength parameter, which could determine the degree of response bacteria have toward environmental or cellular interactions |
| d | Diffusion rate or density factor for individual cells, possibly varying per cell in the simulation to add heterogeneity |
| l | The cell length of a bacterium |
| lTarget | The target length for each cell |
| x | X Coordinate for each bacterium's position |
| y | Y Coordinate for each bacterium's position |
| theta | Orientation of each bacterium |

---

## Bacterial chemotaxis
![Chemotaxis1](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/bacterial_chemotaxis_example.png)
![Chemotaxis2](https://github.com/MarkoKorb/CellBasedModelsF1/blob/master/results/examples/bacterial_chemotaxis_statistics.png)

### Notes
| Difficulties | Tricks |
| :----------- | :----- |
| Can't plot because the function "plotRods2D" is not defined, but shows up in the CellBasedModels documentation | Fix: Copy the code from the API and use it do define "plotRods2D" in your code |
| It is quite hard to play around with the parameters as it is not easy to tell which parameter is what based on their names | Fix (kind of): Give ChatGPT the link to the example and ask it what the parameters in the code mean |
| Changing the parameters does not seem to have any impact on the results? |  |

### Parameters
| Parameter | Explanation (ChatGPT) |
| :-------- | :-------------------- |
| m | A mass scaling factor, potentially representing the mass of the bacteria |
| g | A growth scaling factor, likely setting a reference growth rate for the bacteria |
| d | Could represent a diffusion or density characteristic |
| kn | Nutrient concentration or diffusion coefficient, calculated based on the interaction between mass, growth, and density |
| γn | A nutrient transport parameter, affecting how nutrients move or diffuse relative to bacterial growth |
| γt | Transport rate, likely controlling the rate at which other molecules, besides nutrients, are transported or diffuse within the environment |
| μcc | The cell-cell interaction rate |
| μcw | The cell-wall interaction rate |
| β | A growth control factor, influencing the overall growth rate or replication frequency of bacterial cells |
| βω | A similar growth control factor, possibly focused on a specific aspect of bacterial growth, like wall expansion or replication |
| fChem | Chemotaxis strength, potentially governing the cells’ directional response to the chemical gradient |
| τTumble | Average time a cell maintains a movement direction before tumbling |
| τTumbleMin | Minimum time before tumbling occurs |
| ωTumble | Frequency of tumbling |
| ωMedium | Response frequency of cells to the medium |
| DMedium | Diffusion coefficient for the medium |
| l | The cell length of a bacterium |
| x | X Coordinate for each bacterium's position |
| y | Y Coordinate for each bacterium's position |
| theta | Orientation of each bacterium |

---

## General difficulties and tricks
If you have no idea about agent-based models and their implementation in code, it might be difficult to use the package, as many things are not self-explanatory.

---
---

# Discussion with group members
## Member 1


## Member 2


## Member 3


## Member 4
...
