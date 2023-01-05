---
layout: project
title: 'Augmented Reality Network Observatory Project'
date:        1 June 2022
caption: I created a functional bunny NPC character to be used in virtual reality to guide players
description: >
   Created from scratch an interactable bunny NPC character with dialogue tree, several different animations,
object highlighting abilities, random movements within bounds, and other functionalities. Click the links above the image to see my repo or a demo of my NPC bunny in action.
 
image: 
  path: /assets/img/projects/hydejack-site.jpg
  srcset: 
    1920w: /assets/img/projects/bunny.jpg
    960w:  /assets/img/projects/bunny@0,5x.jpg
    480w:  /assets/img/projects/bunny@0,25x.jpg
links:
  - title: Source
    url: https://github.com/danielmilton22/ComputerVisionProject
sitemap: false
---


# Mr. Rabbit NPC Character

This project was created to be implemented into ARNO as a bunny NPC character with certain functionalities to help players navigate the world, pull up tutorials on a browser widget, and have dialogue with the player. The following documentation will briefly go over how everything works and guides to customizing the bunny NPC to your needs. The bunny character is based on the fictional character Mr. Rabbit from the book Rainbows End.


## Features

- Custom Dialogue System that can easily be implemented with custom dialogue
- NPC manager system that gives bunny random patrols within bounds and interaction capabilities
- Bunny model + animations
- Custom system to highlight in game objects from the dialogue with bunny
- Browser widget that can be pulled up from dialogue



## How to Create Custom Dialogue

![Imgur Image](https://imgur.com/MKqdrKN.jpg)

Creating custom dialogue is simple with this system. Follow these steps

1. Create a new behavior tree (Keep this in the dialogue system folder under bunny_AI)
2. Give it a blackboard asset of dialoguebackboard
3. Once this is done you can start. To make things easier copy paste the dialogue from dialoguetree1
4. You can customize the speech patterns by utilizing sequence and selector nodes
5. Sequence nodes follows one thing after another left to right while selector nodes lets you choose from a list of options (This is why a selector node always follows a reply node)
6. Use speak node for the bunny to speak and reply for the player to choose from an array of options
7. From the selector node you can see reply1, reply2, and reply3 blackboard keys attached to nodes. This is important because you need these blackboard keys to have a key value that matches with the corresponding choice in the array of replies.
8. Use an exit node to exit the dialogue and have the bunny resume its routine
9. To have this new behavior tree custom dialogue work for a new NPC character, implement a dialogue component interface into the character and set its dialogue tree to the tree that you have just created.



## How to Highlight Objects

To highlight objects is a few step process:

![Imgur Image](https://imgur.com/RLSlwSu.jpg)

1. Implement interface BPI_HighlightObject into desired object to be highlighted
2. Scroll to the bottom of the objects settings and set its tag to a unique identifier


![Imgur Image](https://imgur.com/Xt1uExW.jpg)

3. In the corresponding reply node in the dialogue system, add tags and given it values that match the tag on the object
4. Your object should now highlight when prompted

## Creating a Random Patrol within a Bounding Box

The creator of the NPC Manager plugin that was used for the random patrol within a bounding box is called Coqui Games. The creator has created many tutorials on all the functionalities his plugin offers but for this specific task, use this tutorial.

- link: https://youtu.be/u8RmPLYV5Q4


## Other Notes

Some other things to note are:

- In the unreal project, everything that you need to find that I have created can be found under the Bunny_AI folder
- In the repo, the folder Bunny_Model contains all of the original bunny 3D models as well as additional animations to the ones I've used. These include animations for running, jumping, and eating.
- You can easily change the aesthetic of the dialogue box by using a different .jpg image and replacing it under the dialog widget blueprint
- Press key F to interact with bunny
- Press tab to change from 3rd person to 1st person POV

## Demo

https://www.youtube.com/watch?v=-HFDkOb5J4k


## Screenshots

![Imgur Image](https://imgur.com/EL2IzaC.jpg)
![Imgur Image](https://imgur.com/INuXy8r.jpg)
![Imgur Image](https://imgur.com/Jxb7IsT.jpg)


## Mr. Rabbit Quotes and Actions from Rainbows End

## Actions:

- Sips tea
- Shrugs
- Implausible mannerisms
- Shakes and wiggles ears a lot
- Grins
- Arrogant in speech


## Quotes:

- “Have I got a deal for you!”—hopped on table and tipped its too hop
- “Hmph.”—sits down and pours itself a cup of tea
- “Im all ears”--wiggled two long ears
- “Of course I am highly recommended. For any problems, political, military, scienctific, artistic, or amorous-meet my terms, and I will deliver.”
- “Well,well,well”—rabbit sits back(shows thinking)
- “Whatever. You’ve come to the right fellow”—nose quivers
- “Well then. I will hop right on it.”
- “Talk to you soon”— Bunny laughs and hops off table
- “Of course I share your charitable motives”
- "Really?" Rabbit was literally bug-eyed with curiosity. "How is that?" 
- The critter took a chomp out of its carrot and waggled an ear. "What's it to ya, Doc?" 
- "Heh," it said, giving a little carroty salute.
- "What did I tell you, Doc! We're in. We're in!" Rabbit danced a merry jig around the caisson
- "Hey, no problem." Rabbit waved magnanimously. 

## Authors

- [@danielmilton22](https://www.github.com/danielmilton22)

