## WHAT IS IT?

This model simulates an ecosystem containing two species: **fish** and **sharks**. Fish consume food (represented by yellow patches) to maintain their energy, while sharks hunt fish. The goal is to observe the population dynamics of these species as they interact with each other while various variables are in effect [fish-count, shark-count, food-count, fish-default-energy, shark-default-energy, food-spawn-chance, fish-spawn-chance, shark-spawn-chance, target-ticks].

---

## HOW IT WORKS

### Fish
- **Movement**: Fish move randomly around the environment, losing 1 energy unit per step.
- **Eating**: Fish eat food (yellow patches) to regain energy.
- **Reproduction**: Fish can reproduce (spawn offspring) if their energy is above a certain threshold and a random chance is met.
- **Death**: if Fish enegry reach 0.

### Sharks
- **Movement**: Sharks move randomly,each step cost 1 energy.
- **Eating**: To regain energy Sharks eat fish.
- **Reproduction**: Can reproduce based on shark-spawn-chance variable and current energy level.
- **Death**: if energy reach 0.

### Food
- **Initial Setup**: Random distribution of Food (yellow patches)
- **Regeneration**: Based on food-spawn-chance food can regenerate randomly

### Energy
- Fish and Sharks have energy that decreases with movement and increases when they eat
- requirement for the turtles to survive.

### Stopping Conditions
- The simulation stops when there are no more turtles (fish or sharks) left in the environment or target tick was met.

---

## HOW TO USE IT

### Sliders
- **Fish Count**: Initial Fish number.
- **Shark Count**:Initial Shark number
- **Food Count**: Initial number of food patches (yellow patches).
- **Target Ticks**: Max number of ticks before simulation halts.
- **Fish Default Energy**: Initial energy of the fish.
- **Shark Default Energy**: Initial energy of the sharks.
- **Food Spawn Chance**: likelyhood of food regenerating each tick. ;proba based on an event
- **Fish Spawn Chance**: Probability of fish reproducing. ; backed by concrete  math
- **Shark Spawn Chance**:Probability of sharks reproducing. 

### Switches
- **Indefinite**: If set to "on" simulation will continue until either Fish or Shark extinct else limit to set tick.

---

## THINGS TO NOTICE

- **Population Dynamics**: Watch how the populations of fish, sharks, and food change over time. Does one species dominate the other, or do their numbers fluctuate and how does population affect each oganism?
- **Energy Balance**:How energy affects survival, do fish and sharks have enough energy to reproduce or survive for long periods?
- **Reproduction**: Pay attention to how the spawn chances influence the growth of populations. Do both fish and sharks reproduce enough to maintain their numbers?
- **Food Availability**: How does the regeneration of food impact the survival of the fish?

---

## THINGS TO TRY

- **Vary Population Ratios**: Increase or decrease the number of fish and sharks. What happens when you have more sharks than fish, or more fish than sharks? -- Tested through various scenario
- **Adjust Energy Levels**: Try modifying the initial energy values for both fish and sharks. How does this affect the survival rate and population size?
- **Control Food Regeneration**: Change the food spawn chance to see how it affects the fish population. What happens when there’s more food or less food available?
- **Run with Indefinite Mode**: Set the **Indefinite** to "on" and observe how the ecosystem change -- Tested through various scenario.

---

## EXTENDING THE MODEL

- **Multiple Predators**: Add new predator or prey species and see how they affect the ecosystem.
- **Prey/Predator Mechanism**: Add a new behavior for both species, such as defense mechanism for preys and predator behaviours
- **Evolve**: Add a way for preys to psuedo fight back, when a prey reach X energy it will grow and start to eat its own, until it reach a point it will be the new predator

---

## NETLOGO FEATURES

- **Breed Command**: The model uses `breed` to define two types of agents: **fishes** and **sharks**, each with its own behavior and properties.
- **Agentset Filtering**: Patches are used as the environment, and food is tracked using `patches with [pcolor = yellow]` to identify food locations.
- **Energy-based Reproduction**: The `hatch` command allows agents to reproduce when their energy is sufficient and a random chance is met.
- **Random Movement**: The `right random-float 360` and `fd 1` commands make fish and sharks move randomly, simulating natural movement behaviors.

---

## RELATED MODEL(S)

- **Wolf Sheep Predation**: A classic NetLogo model where wolves prey on sheep, illustrating predator-prey dynamics similar to this model.

---

## CREDITS AND REFERENCES

Created by CA group 1 Grad/Undergrad,De La Salle University Manila, as part of our agent based modeling project in CA class CSC931M G01.

For educational use. No external datasets or libraries were used.

The model's idea was inspired by Wolf Sheep Predation Model and feeding frenzy game, where the user plays as the prey which eats until it can be the predator. 

Created by:

https://github.com/jrcala7 https://github.com/PedGit025 https://github.com/jasgayamo

