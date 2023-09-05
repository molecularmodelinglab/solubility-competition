# The MML solubility prediction onboarding competition

## Introduction

Welcome the the Molecular Modelling lab! The competition is meant to be a fun way to get a sense of what the lab does, as well as get setup with all the python libraries we use here.

The goal of this competition is to create the best model for predicting aqueous solubility. Solubility is an example of an important molecule property we want to predict. It may seem simple, but it's actually super important, and far from a solved problem. Chemists working on new drug candidates often discover that their latest molecule is completely insoluble -- which makes it pretty useless. If we can accurately predict this (and convince the chemists to use our models...), chemists will know beforehand not to synthesize those insoluble bricks.

Your mission, should you choose to accept it, is to create a solubility model that can generalize to new types of molecules. We are using the [AqSolDB dataset](https://www.nature.com/articles/s41597-019-0151-1), split into train/valid/test clusters according to scaffold splits. (That is, two very similar molecules should be in the same split).

You will extend the code in `competition.py` with whatever models you want (random forests, neural networks, you name it). This script will train your model (currently, just a linear regressor) and test it on the validation set. You will be judged according to your model's final performance on the test split. The winner will receive a prize (details TBA).

You may work alone or in teams of up to 3 people.

## Rules

1. When developing your model, you may only check the performance of your current model on the validation set. You may not try your model on the test split until you are ready to submit. You must submit your final performance once you try it out on the test split, regardless of how you feel about the result.
2. When you are ready to submit, change the `split_name` variable from `valid` to `test` in `competition.py`. Run the code and copy full output of the script. Send this output to @mixarcid, along with your team name.
3. The deadline for submissions is *Friday, Oct 6 at 11:59 ET*.
4. The winner will be the team with the highest R2 (or, equivalently, the lowest MSE).
5. Have fun.

## Getting started

In order to get started, make sure you have [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [conda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html). [Fork this repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo) onto your computer. If you're on a team, make sure only one person forks the repository and shares it with the rest of the team!

If you have never used conda before, check out [this tutorial](https://conda.io/projects/conda/en/latest/user-guide/getting-started.html#managing-python). You'll want to create a new conda environment with Python 3.11 installed. Then open up a terminal in your environment (this can be done easily from the Conda GUI on Windows). `cd` to the directory where you cloned this repository, and run `pip install -r requirements.txt` to install all the required packages.

Now you _should_ be all set up. Try running `python competition.py` and see what happens. If you don't see any errors, you're good to go! If you see an error that confuses you, please reach out on slack! Ping @mixarcid for any questions.

## Tips

1. Slack Michael (@mixarcid) if you have any questions
2. Check out the literature on solubility prediction models! A little domain knowledge goes a long way.
