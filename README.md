# GPT-Macbeth
A custom finetune of GPT-2 trained on a custom dataset of victorian literature

## Information
The goal of this finetune is to output high-quality victorian literature, while being customizable with Author's Note and being light to run (aka not being a GPT-Neo or GPT-Jax finetune, for now at least).


## Download
Currently can only be downloaded through Google Drive: https://drive.google.com/file/d/1QuErX7w0C4M-Z4wjm5Z5hXEDTazwKR4y/view?usp=sharing


## Authors Note
Author's Note was added manually, so please appreciate it. :)

The format of it is [ Author: George Eliot; Genre: Horror, fantasy, novel; Tags: scary, magical, victorian ]
Some words will work well, some won't. Please make sure to have spaces before each ][.

Most popular victorian authors should work, but keep in mind that some authors (e.g. Mark Twain) will result in a somewhat weird behavior due to a quirk in the dataset that will be addressed in the next version of the finetune.

When it comes to the genres, "novel", "fiction", "horror" and "romance" work best, but from playing around with it, I've noticed that most other not too specific genres work pretty well too.

The tags are a bit complicated. Adding "normal" will result in a story without anything special (like no magic or fantasy element) and tends to be pretty low-pace. Using "real-life" will push the AI towards a historical/biographical path. Almost all tags should work. Using "man" or "woman" is supposed to semi-determine what gender the main character is, but it heavily depends on the chosen author.

## History
Version 0 - This was the first test version of the finetune, trained on GPT-2-small and with a really small dataset. The name was GPT-Kelini before it was renamed to GPT-Macbeth in V1.

Version 1 - The current version of the finetune. Trained on GPT-2-medium with a much, much bigger dataset compared to V0. Supports Author's Note

### Notes
Please use a very low temperature/randomness when using it, if you want to get anything out of it. Pumping the repetition penalty up helps a lot too.

The model was specifically converted to PyTorch so that most front-end GUI's should run it. It has been only tested on KoboldAI, but should theoretically work on others too.

For some odd reason, my finetune is capable of writing victorian NSFW content, if used the right way. No NSFW was in the dataset and considering the size of the model, it's really odd to see it do so. Perhaps the countless romantic novels in the dataset had something naughty in them, but I highly doubt it.

You may sometimes get roman numerals on random occasions, this shouldn't happen often, but if it does, it's again something that will be (manually, unfortunately) addressed in the next version of the finetune.

If you are wondering why I renamed my finetune to Macbeth, there are a few reasons: First, it sounds much better and smoother than Kelini, second, it's a play by Shakespeare that closely matches the writing style of some of the authors in my dataset, and third, the most important reason, it's was mentioned in Hamilton, so yes, my love with Hamilton is bleeding everywhere and yes, the next version of the dataset will try to have a Hamilton easter egg featuring the Author's Note.

### Credits
I want to thank HuggingFace for their tokenizer and everything they've done to make everything easier. Then is OpenAI for making GPT-2. I also want to thank most active people on the AIM Discord server in the community-projects channel. Thanks to Bran for finding a way to convert checkpoints to a PyTorch model, thanks to Mr. Seeker and Aedial for helping me in cleaning the dataset and to finetune form the NovelAI team for perhaps making my finetune output much better quality by telling me about the magic of the <\|endoftext\|> token.




P.S. If you happen to use it in something commercial or in an online demo or in any other way that is not for personal use, a credit will be greatly appreciated (and if you do something exciting with it, make sure to let me know, I'd be more than happy to see it being used by someone!).
