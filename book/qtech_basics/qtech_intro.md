# Tutorial 1 - Basic concepts of quantum technologies
In today's world, the word “quantum” evokes similar dreams, hopes and reactions like the words “blockchain” or “artificial intelligence”. Enthusiasts focus exclusively on the disruptive potential while the greater public sees it mostly as a big hype which is impossible to understand for normal people. This hipster role is rather new to the quantum sector which has largely evolved under the radar to the greater public for the last one hundred years. In this tutorial series, we will summarize some basic concepts of quantum physics and then  discuss the four pillars of quantum technologies:

1. **Quantum metrology**, where we use quantum physics for precise measurements.
2. **Quantum cryptography**, where we improve security through quantum physics.
3. **Quantum simulation**, where we solve specific problems that are hard for normal computers with quantum systems.
4. **Quantum computing**, where we build a new computational framework with quantum mechanics.

## The esoteric beginnings of quantum physics in the 1920s

Theoretical physicists like Planck, Einstein, Schrödinger or Heisenberg (before he was reborn as a drug kingpin in a TV series) founded quantum physics in the 1920s. They tried to explain rather esoteric physical effects like black body radiation or the photoelectric effect. This work proved to have major implications to our understanding of physics and became integral to the description of our world. 
The mathematical framework behind quantum mechanics is sufficiently advanced to go well beyond high school physics, so we will skip it here. But if you have the feeling that you would like to have a deeper understanding, here are some ways of doing this:

- We wrote a university lecture on the cooking recipes for quantum mechanics with plenty of references. It is a one hour summary that might get you started if you are familiar with most of the maths.
- If you would like to get a marvelous introduction into some basic principles of quantum mechanics we recommend the absolutely outstanding Feynman lectures. 
- The books by Cohen Tannoudji give an extensive and clean introduction into quantum mechanics with discussions of numerous problems.

## Two rules, no math

In this tutorial series, we discuss quantum mechanics based on two rules with no math. This beautiful description was given by Chris Monroe in a short youtube video that we highly recommend before you continue. 

We will just call the rules from the video **quantum rules one and two** throughout the tutorial series.

- **Quantum rule 1**: Quantum objects can be in several states at the same time. 
- **Quantum rule 2**: Rule number one only works when you are not looking.

We will see these two rules in action in every single quantum technology, but here we will visualize them directly by the famous Schrödinger cat.

## Schrödingers cat

Erwin Schrödinger, one of the founders of quantum mechanics, illustrated the rules of quantum mechanics through the following thought experiment. 

It is a thought experiment of a cat that is trapped in a box together with a closed bottle of toxic gas. A very thin filament that might snap at any time keeps a hammer above the bottle from falling. And when the hammer hits the bottle the unfortunate cat dies of poisoning. The final ingredient is that we cannot see or hear anything of what is happening within the box without opening it. So if we look at this problem through the rules of quantum mechanics two options are imaginable:

- Option A: The filament holds, the bottle remains intact and the **cat stays alive**.
- Option B: The filament snaps, the bottle breaks and the **cat is dead**.

**If we can apply the rules of quantum mechanics** we know from quantum rule 1 the cat will therefore be in both states at the same time, it is dead and alive as long as the box is closed. We will often use the terms **superposition** to describe a situation where a system is in multiple states at the same time. But as soon as we open the box, we will only see it as being dead or alive according to quantum rule 2. 

The art of quantum technologies is then to build up systems that follow these rules in a very controlled manner. Physicists developed increasingly refined approaches over the last one hundred years. The technologies have lead to different quantum hardware platforms based on atoms, electrons or even light.  We have a whole series of tutorials on quantum hardware if you would like to know more about it. Over the years, physicists have learned to master these systems to an increasingly high degree. And it has now even been possible to realize Schrödinger's thought experiment. See for example here for a realization with atoms.

## The two quantum rules in the different quantum technologies

To end this tutorial, we now discuss how we use the two rules as essential ingredients in all quantum technology stacks. We leave the much more detailed discussion  to the next parts of the series.

1. In **quantum metrology** we put the measurement system into a superposition in the first step (quantum rule 1). We can think of it like a coin that is tossed and rotates at a speed that might depend on gravity. We then measure the result after some time and as for any coin, we will always get heads or tails. 
2. In **quantum cryptography** we put a pair of photons into a superposition. Then, we send them to the partners that would like to communicate.  If someone tries to listen to the discussion he will measure the system and destroy the superposition. Smart protocols use this to secure the communication.
3. In **quantum simulation** physicists design a system to solve a very specific problem efficiently by testing multiple solutions in parallel. The measurement in the end allows the observers the solution to the problem.
4. In **quantum computing** we put we computational units into superpositions. Then, smartly designed algorithms can solve certain problems more efficiently than classical computers. The final measurement is then telling the user the result of the computation.

## Summary

In this tutorial we discussed basic concepts of quantum technologies. We saw that the key challenge is to implement systems that follow the two quantum rules. The designer chooses then the technologies that solve the problem at hand in the most efficient way. We will focus on quantum metrology in our next tutorial before we move on to the other pillars.