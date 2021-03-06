---
title: 2021 Exercises
layout: rlos_page
body_class: rlos
permalink: rlos/2021/code_exercises.html
---

# RL Open Source Fest Application Exercises

See [here](/rlos/2020/code_exercises.html) for last year's exercises.

## C++ Exercise
If your project involves C++, complete the following exercise:

VowpalWabbit (VW) has an input text format allows examples to have a tag associated with each example. A tag is a string that carries no specific meaning but can be used to identify examples later, or be used to signal some behavior. Given this example:
```
1 foo_tag| feat_1 feat_2
```
The string `foo_tag` is the tag.

### Task
Add a command line option (`--ignore_tag <value>`) to VW that makes it ignore examples with a specific tag `value`.

To test it, use the following test file (`input.txt`):
```
0.5 foo| a c
0.5 bar| a
0.5 ignore| b
1 ignore| a b
0 | c
```

Invoking vw with `./vw input.txt --ignore_tag ignore` should give the same result as using the following input:
```
0.5 foo| a c
0.5 bar| a
0 | c
```

Submit a diff file through `git --diff` for this exercise or a link to the commit in your fork for your application.

### Links
- [vowpal_wabbit repo](https://github.com/VowpalWabbit/vowpal_wabbit)
- [Build instructions](https://github.com/VowpalWabbit/vowpal_wabbit/wiki/Dependencies)

## Python / Data Science Exercise
If your project involves Python or data science, complete the following exercise:

For this exercise we'll look into how non-stationarity affects different Contextual Bandit algorithms.

First, get yourself familiarized with the [Simulating Content Personalization with Contextual Bandits](https://vowpalwabbit.org/tutorials/cb_simulation.html)
Vowpal Wabbit tutorial and in particular the second scenario, which shows the effects of non-stationarity.

### Task
Modify the second scenario in the following ways:

- Add multiple changes to the reward distribution over time
- Introduce varying noise in the reward distribution

Run this new simulator with different exploration algorithms and vizualize and compare their performance.

Submit a Jupyter notebook showcasing the above in a GitHub repo for your application.
### Links
- [Contextual Bandits Tutorial](https://vowpalwabbit.org/tutorials/contextual_bandits.html)
- [Exploration Algorithms](https://github.com/VowpalWabbit/vowpal_wabbit/wiki/Contextual-Bandit-algorithms#changing-action-set-or-featurized-actions)
