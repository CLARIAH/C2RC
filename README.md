# C2RC

The goal of the Civil Registry Reconstitutions Cleaner (C2RC) is to help assess the correctness of computed reconstitutions of individuals. 

## Description

C2RC evaluates the quality of the reconstitutions generated by the BurgerLinker tool based on sets of soft and hard rules. For instance, a reconstitution is unlikely when an individual is mentioned in two birth certificates. In this case, the ‘hard rule’ stating that a person can only be born once is broken. A ‘soft rule’ is based on the assumption that consecutive children for example cannot be born more than ten years apart. The rules are inspired by the expected structure of an extended family.

As illustrated in Figure 1, the tool shows the rules broken by a reconstituted individual to assist the user in judging the correctness of a reconstitution. For each reconstitution the tool displays subgroups clustering individuals who appear together more than once. Based on this evidence, a user can decide to merge or exclude subgroups from a reconstitution.

![](Results-2.png)
*Fig 1: Enabling consistency validation*

Computed reconstitutions might not refer to a unique person due to :

- A weak set of discriminating criteria.
- The quality and size of the data.
- Limitations of matching algorithms

C2RC therefore facilitates the identification of false positives and highlights potentially erroneous reconstitutions. The tool can thus evaluate the overall power of the discriminating strategy developed in the LINKS project and re-implemented by the BurgerLinker entity matching tool.


## ⚠️ Soft Rules

1. A person is unlikely to have more than 20 children.
2. A person is unlikely to marry more than 5 times.
3. A person should not have more married children than children.
4. A person should not have divorced more than they got married.
5. Consecutive children are unlikely to be more than 10 years apart.
6. A person should not appear with the same person only once (groundless).
7. The number of grounded reconstituted subgroups - where the reconstituted individual appears with the same person at least twice - should not exceed the number of children plus one.
8. A person should not have more groundless observations than a third of its reconstitution size

## ❌ Hard Rules
1. A person cannot be born more than once.
2. A person's children cannot be born more than once.
3. A woman is very unlikely to marry before the age of 13.
4. A mother is very unlikely to give birth past the age of 50.
5. A person should not break more than two soft rules.
6. A person should have at most one father or mother.
    A person cannot be known and unknown at the same time.
7. The first and last child of a mother are very unlikely to be more than 30 years apart.




