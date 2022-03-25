## Using Bayesian Models for Inductive Generalization of Moral Concepts
### Independent Research Project (Advisor: Dr. Alan Jern)
*August 2021 - February 2022*

All materials for this project can be found at the following GitHub link: https://github.com/jernlab/moral-character-inference 

### Motivation for Research
This research project is centered on 2 main ideas: a new hierarchical model of moral concepts which describes how people make inferences about morals [1] and using a Bayesian model to evaluate the accuracy of an inference model [2]. Specifically, I studied how people answer questions such as the following: if Joe cuts in line at a grocery store (one type of moral violation), how likely would he be to also ban people he didn’t like on a Discord server (another type of moral violation)?

The purpose of this study is to evaluate whether the ways in which people make inferences about both moral and non-moral concepts is similar. Specifically, I test the question: Is the way that people reason or make inferences similar for both moral and nonmoral concepts?

In this project, I adapt the Bayesian model from [2] such that it applies to moral concepts and test this adapted model in a new online behavioral experiment. 

### Detailed Project Description
In [1], Landy and Bartels explored how people make inferences about moral situations and proposed a hierarchical model that describes the way people reason about moral concepts. They studied people’s responses to questions such as: if Joe cuts in line at a grocery store (one type of moral violation), how likely would he be to also ban people he didn’t like on a Discord server (another type of moral violation)? However, the authors did not make quantitative predictions about the strength of the inferences made, because they were not testing a computational model. 

Sanjana and Tenenbaum [2] use a Bayesian computational model to describe the way that people make inferences about non-moral situations, which assumes that these inferences are made mostly according to probability theory. For instance, if you learn that a disease has infected three different monkeys, you would be less likely to think it can infect horses than if you learn that it has only infected one monkey. I am interested in exploring whether people reason the same way about moral concepts as they do about questions like these; for example, if someone commits the same type of moral violation many times (like lying), are people less likely to think that person will commit other violations (like stealing) than if the person had only lied once because they believe the subject is specifically a liar and not a thief?

In this project, I replicated the animal experiment from [2] but with questions regarding different categories of moral violations instead of animals, using the moral categories proposed in [1]. I hope to be able to answer the following questions: Do people make inferences in similar ways regardless of the situation, when given only limited information? Or do people judge moral concepts to be a different class of problem than other concepts, meaning that modeling people’s reasoning process the same way for all concepts would not make sense? If people do reason about moral concepts differently, where do these differences lie, and what causes them?

This project builds upon work started in the 2020-21 academic year by another Rose-Hulman student, who conducted an initial pilot study to show that this is a promising question for further investigation. However, that work reached only a preliminary stage, and the research question remained open; during my research project, I worked to complete this research effort. 

## Publication, Presentations & Awards
I was awarded a $532 grant from the Rose-Hulman Independent Project/Research Opportunities Program (IP/ROP) to conduct this research. Specifically, these funds were used to compensate 200 randomly selected survey participants for completing the survey used for data collection. 

I intend to present this work at a cognitive science conference in 2022. This project was also presented during the Winter quarter at a student work showcase at Rose-Hulman. 

### References
[1] Landy, Justin F., and Daniel M. Bartels. An Empirically-Derived Taxonomy of Moral Concepts. 19 Mar. 2018.
[2] Sanjana, Neville E., and Joshua B. Tenenbaum. Bayesian Models of Inductive Generalization.

### Tools and Methods Used
Formr – I used the Formr survey platform to conduct all experiments and perform data collection. 
Python – I used Python to write a script for generating an arbitrary number of Formr surveys, which will be randomly selected then shown to the users. This script handles complex randomization which is needed to ensure the fairness and accuracy of the results. 
