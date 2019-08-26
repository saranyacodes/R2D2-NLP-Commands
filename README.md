# R2D2-NLP-Commands
Control an R2D2 Robot using natural language commands. 

This project is compatible with R2D2 and R2-Q5 robots by Sphero, which can be found here: https://www.amazon.com/Sphero-R201ROW-R2-D2-App-Enabled-Droid/dp/B07D9TZHRW/

Here is a video demonstration of how the R2D2 works: https://youtu.be/a7nyfv4dxa4 

This project is a delve into the Natural Language Processing topic of CIS521: Artificial Intelligence. Multiple different commands can be interpreted to mean the same thing. For example, if we want R2D2 to make some noise, we may say “start singing” or “play some music” or “make a noise”. Although these are all worded differently, they can be interpreted to mean the same command. Through using word embeddings given by the GloVe word vectors (https://nlp.stanford.edu/projects/glove/),we can begin to give R2D2 natural language commands like so. 

Some instructions on set up as as follows. 

First, the following repository must be pulled onto one’s device: https://github.com/josephcappadona/sphero-project

There are terminal instructions given in that ReadMe. In sphero-project —> src, we are going to add another file. We are going to add the r2d2_final.py and the glove.6B.300d.magnitude files. Make sure to download the .magnitude file from the pymagnitude website (https://github.com/plasticityai/magnitude). 

Once all the necessary modules are installed (nltk, sklearn, pymagnitude, etc), then we can proceed with setting up the r2d2 Command Center! In the python environment from terminal, type in the following commands: 
```
from client import DroidClient
droid = DroidClient()
droid.scan() # Scan for droids.
droid.connect_to_droid('D2-33C3') # droid ID here
```

Now we have connected to the robot… this is where our r2d2_final.py script comes into play. Type in the following commands:
```
from r2d2_final import CommandCenter
command = CommandCenter(droid)
command.run_commands()
```

Feel free to play with the robot now!
