# Why does time flow in one direction?
The direction of flow of time is determined by the Second Law of Thermodynamics which says change in Entropy is always a positive number or zero but never negative. That is how we know time is actually moving when we see ice melting or a coffee getting colder when left alone, both are the example of increasing entropy. 

Well what is entropy?

Consider you want to go to some city to meet your friend far away from your place, and in your universe, there is only one mode of travel, say by teleportation (or train whichever you want to imagine). Now your friend will know exactly how you reached there because he/she knows there is only one option right.


Now let's complicate things for your friend. Suppose there are two possible routes you can take to reach to your friend (for example there are two different trains which go to your friend's city or whatever). Now your friend is not sure anymore. He/She is divided into a fifty-fifty probability. And if there are more travel modes: Flight, Road, Boat, Teleportation etc., with different routes each you can see how quickly your friend will get extremely confused and start loosing more and more information about your actual mode of travel. 


Well, what is happening here?

If you see from this example you will notice that the more the options you have to choose from, the lesser is the probability to choose the correct one or in other words lesser is the information about the true path. Examples like this are very general in nature, they are true in every field and every sense. 



Let's take a physics example now. A bunch of molecules in a closed container (Gas in a box) and you want to know the temperature of the gas/system. Temperature is nothing but like a number stamp which tells us about how fast those molecules are moving on average (it is actually related to average kinetic energy but let's take the simpler assumption for the sake of argument). So the devil is in the details, a single average speed of the molecules can be achieved by any number of combinations of the individual speeds of the different molecules.

Let me be more specific, consider you have three molecules, and the average speed of the system is one unit, and the molecules only have three choices of speed (1,2 or 3) units. An average speed of one unit can be achieved by two unique ways; either all three have a speed of one unit, then the average = (1+1+1)/3 = 1 unit or one of them has a speed of 3 units and rest two have a speed of zero units, then the average = (3+0+0)/3 = 1. Note that I am not counting the (0,3,0) or (0,0,3) as a separate combination from (3,0,0) because gas molecules are indistinguishable from each other, so it doesn't matter who comes first and who comes last.



The point of the matter is that this is a similar kind of situation as your friend. Now we don't know which combination the molecules are in because both combinations give the same result. And as you may have already noticed, these number of equally likely combinations increase if I increase the number of choices the molecules have in terms of the speed they can have. Similar to the number of routes your friend could take. Now, this measure of missing information or the measure of the number of combinations you have that represent the same outcome is called ENTROPY. That's right Entropy is nothing but the measure of how many unique combinations your system can take to describe the same physical state. 


In technical language, these number of unique combinations are called Microstates, and the physical state they are representing (the average value in our case) is called the Macrostate of those Microstates. Now I know the language is not perfect and very confusing, but it is what it is.

Also, notice that if the average speed is zero, then there exists one and only one unique combination to achieve that; all molecules go to zero so only one microstate. Mathematically Entropy(S) is defined as the Log of the number of microstates

Entropy = Log(microstates)

The system switches between microstates indiscremenately or more precisely randomly. We can simulate this switching by utilizing the random number generator with the help of Qiskit's QASM simulator which simulate the inherent randomness present in the quantum systems.

The basis idea is to create a superposition of multiple using a bunch of Hadamard gates which makes it equally likely to have any combination of the qbit states and thus we have a pure random number generation when we measure the state and the wavefunction collapses to one of the combination.

![image](https://user-images.githubusercontent.com/51285582/200149103-1e8885fc-6fc0-46b5-a0a8-13b5d7183c51.png)

Now if we let the system switch between mictostates randomly with by utlizing the output of the above circuit and measure the entropy every time we will find that with enough meadurement that the state with highest number of microstates, i.e., with the higheest entropy has the highest probability of happening. The following figure show the distribition of entropy of a system after 800 random switches which start out in a zero entropy state

![image](https://user-images.githubusercontent.com/51285582/200149258-02b59a20-9606-41cb-b8a0-f68f45ab1aa4.png)
 
It is clear that the state with highest entropy has the highest probability and thus we observe a higher entropy state in every system with time because of purely statistical nature just like the if you have more 1 million black balls in a bag and 5 red balls and 2 blue balls and you choose randomly you will most likely to choose a black ball than any of the other and that is not due to some magical law say that nature prefer black color its just statistical similar to entropy where a state with higher entropy has higher probability and thus more likely than not we find systems favoring a higher entropy state.

