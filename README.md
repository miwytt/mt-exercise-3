# Description of changes, used commands 

For the most part I used the commands that were provided by the assignment description. The changes that I made were solely to adapt path names to use a new data set, which was in my cas Edgar Allan Poe's _Collected Works Volume I_, and the adaptation of the different dropout hyperparameters. Unfortunately, I noticed after training each of the five models, that I did not change the save path for the new models such that I overwrote all but the last model witha a dropout of 0.8. For the generation of model text samples I trained the model with the best results again and saved it this time as model_0.3.pt. 

# Best model sample

The text sample generated with my best model and the generate.sh/py scripts looks as follows:

". <eos> “ We cannot understand , however , not that when there could be immense thing — at least
arrival of Dubourg — for the cavities were satisfied near the bodily of this extraordinary volcanic Roule , however as
secret of its more letters , a still moderate <unk> in blackness . <eos> “ These experience being sitting on
the passage of the daughter , a <unk> <unk> currency . <eos> But , be as the elopement showed me
to be in question , I drew impossible to remember that the original ear of whose building , there came"

I think the output dies resemble the language used by Poe, however, it is highly ungrammatical and does not adhere to simple written language structure rules such as sentence boundaries.


# MT Exercise 3: Pytorch RNN Language Models

This repo shows how to train neural language models using [Pytorch example code](https://github.com/pytorch/examples/tree/master/word_language_model).

# Requirements

- This only works on a Unix-like system, with bash.
- Python 3 must be installed on your system, i.e. the command `python3` must be available
- Make sure virtualenv is installed on your system. To install, e.g.

    `pip install virtualenv`

# Steps

Clone this repository in the desired place:

    git clone https://github.com/emmavdbold/mt-exercise-3
    cd mt-exercise-3

Create a new virtualenv that uses Python 3. Please make sure to run this command outside of any virtual Python environment:

    ./scripts/make_virtualenv.sh

**Important**: Then activate the env by executing the `source` command that is output by the shell script above.

Download and install required software:

    ./scripts/install_packages.sh

Download and preprocess data:

    ./scripts/download_data.sh

Train a model:

    ./scripts/train.sh

The training process can be interrupted at any time, and the best checkpoint will always be saved.

Generate (sample) some text from a trained model with:

    ./scripts/generate.sh
