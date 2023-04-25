# GPT-Macbeth
A custom finetune of GPT-2 trained on a custom dataset of victorian literature

## Information
The goal of this finetune is to output high-quality victorian literature, while being customizable with Author's Note and being light to run (aka not being a GPT-Neo or GPT-Jax finetune, for now at least).


## Download
You can download it from [Hugging face](https://huggingface.co/Philipuss/GPT-Macbeth) or [Google Drive](https://drive.google.com/file/d/1QuErX7w0C4M-Z4wjm5Z5hXEDTazwKR4y/view?usp=sharing).


## Authors Note
Author's Note was added to the dataset manually

The format of it is [ Author: George Eliot; Genre: Horror, fantasy, novel; Tags: scary, magical, victorian ]
Some words will work well, some won't. Please make sure to have spaces before each ][ .

Most popular victorian authors should work, but keep in mind that some authors (e.g. Mark Twain) will result in a somewhat weird behavior due to a quirk in the dataset that will be addressed in the next version of the finetune.

When it comes to the genres, "novel", "fiction", "horror" and "romance" work best, but from playing around with it, I've noticed that most other genres work pretty well too.

The tags are a bit complicated. Adding "normal" will result in a story without anything special (like no magic or fantasy element) and tends to be pretty low-pace. Using "real-life" will push the AI towards a historical/biographical path. Almost all tags should work. Using "man" or "woman" is supposed to semi-determine what gender the main character is, but it heavily depends on the chosen author.

### Notes
Please use a very low temperature/randomness when using it, if you want to get anything out of it. Pumping the repetition penalty up helps a lot too.

The model was specifically converted to PyTorch so that most front-end GUI's should run it. It has been only tested on KoboldAI, but should theoretically work on others too.

You may sometimes get roman numerals on random occasions, this shouldn't happen often, but if it does, it's again something that will be (manually, unfortunately) addressed in the next version of the finetune.

### CreditsHuggingFace for their tokenizer and everything they've done to make everything easier and of course OpenAI for making GPT-2.
