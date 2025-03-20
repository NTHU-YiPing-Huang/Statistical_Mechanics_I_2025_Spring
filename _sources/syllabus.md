# Syllabus for Statistical Mechanics (I) -- (2025)PHYS521000

> 盡信書不如無書。				--孟子 
>
> 道可道，非常道。				--老子
> 
> *Keep throwing out the inessential until the problem becomes trivial. Then go back one step. -- Sam Edwards*

The quotes above are very elegant descriptions about the attitude of learning. If one completely believe what a book says, it is better not to read any books. Any books should not become an obstacles for thinking. The second quote says: if a principle can be explicitly described by words, such a principle will not be the eternal principle. Somehow they describe how our understanding evolves as a function of time.

## Basic information
* Time: Thursday 13:20-16:20
	* 13:20-14:10 (lecture, 50min)
	* 14:10-14:20 (break)
	* 14:20-15:30 (lecture, 70min)
	* 15:30-16:00 (Quiz/review the lecture with TAs, 30min. The roll call is not part of the final scores, just used for me to check if this helps the learning.)
* Classroom: Physics building, Room 124 
* Instructor: Yi-Ping Huang
* Office hours: 11:00 am on Thursday or by appointment (Online or at Room 517)
* Teaching assistant: **Hao-Yang Yen**, **Ren-Hao Lee**, and **Ping-Cheng Lu**
* TA Office hours: 
  Monday, 18:00~19:00 Room 620
  Tuesday, 13:00~14:00 Room 706
  Friday, 14:00~15:00 Room 706
* **Midterm exam date: April 10th**
* **Final exam date: June 5th**
* The course will be offered in English.
	* We encourage everyone to interact in English. If some conceptual questions are difficult to be described in English, one can ask the question in Mandarin, and I will translate that into English. If I forgot to do that, please remind me to do so.
* Teaching method: Lectures with live video streaming. 
	* link for the video streaming: please contact the instructor.
	* Course-related information(*e.g.*, homework) will be posted in the eeclass platform of NTHU.

## Evaluation:

Homework (0%), Midterm (50%), Final (50%).

### How to do the exercise 

* Bring your pen, blank paper, and the assignment. Find a place where you can think. Start working on the assignment. Think about the meaning of the problem. If you don't know what to do, that's fine. Propose possible ways to yourself first. Develop the logic to solve the problem first, ignore the details of the calculation. Focus on the strategy of your approach. 
* Then, start to carry out your strategy. If you get stuck, found you are confused about some concept. Check the note and see if you can figure out what's going on. 
* If you still cannot figure it out, try to describe your confusion to yourself. Try to narrow down the concept that you don't feel you understand. Construct specific examples to show why it is confusing to you. Then you can bring your confusion to discuss with your classmates or TAs. 
	```{admonition} Example (A possible workflow of doing homework)
	:class: tip
	**Assignment**: Calculate the specific heat of model X:
	
	1. What is the physical meaning of specific heat? Did we learn how to calculate specific heat during the course? Thermodynamic quantities are usually related to thermodynamic potential. Can we calculate the free energy of the system and get specific heat from there?
	2. What is model X? What is the energy spectrum of model X? How knowing the energy spectrum helps me to construct the expression of thermodynamic potential?
	3. If I find a way to derive the thermodynamic potential and if I understand how to calculate specific heat from thermodynamic potential. Then I should be able to solve this problem. So I should understand how to construct thermodynamic potential from scratch and how the thermodynamic potential is related to the specific heat.
	4. Carry out the detail of the calculation.
	```
## Textbook

1. *Statistical Mechanics in a Nutshell*, Luca Peliti {cite:p}`peliti2011statistical`-- Formal approach, might be a little bit boring.
2. *Statistical Mechanics: Volume 5, Landau and Lifshitz* -- The classic theoretical physics collection. It's unfortunate that we cannot discuss with Landau anymore, but his way of thinking is left in the classic textbook series forever. It's the textbook  we used when I was a graduate student at CU Boulder.
3. *(2nd Edition)Statistical Mechanics: Entropy, Order Parameters, and Complexity: Second Edition (Oxford Master Series in Physics)*, James P. Sethna {cite:p}`sethna2021statistical`-- More applications of statistical mechanics. When you have the question: why should we study statistical mechanics? You can find various interesting assignments at the end of each chapter.

## Course Description
This course will introduce students to one of the pillars of theoretical physics: Statistical Mechanics. 
Statistical mechanics provides a framework to understand and describe all macroscopic systems, from a 
cooling cup of coffee, boiling water to electrons in metals, semiconductors, superconductors, magnets, black 
holes, ... just to name a few. Statistical mechanics is a body of knowledge that establishes the relation 
between microscopic properties and macroscopic properties of the system, which is essential from both 
fundamental and application points of view. The course will cover the basic theoretical framework and 
applications(starting from non-interacting systems, classical gas, and quantum gases(fermions and bosons) 
). After the study of non-interacting systems, we will discuss the techniques related to interacting systems. 

## References

1. **Statistical mechanics, R. K. Pathria and P. D. Beale** -- A relatively formal but solid textbook.
2. **Thermodynamics and an introduction to thermostatistics, H. B. Callen** -- An excellent textbook that discusses the fundamental principles of thermodynamics.
3. **Statistical physics of particles/fields, M. Kardar** -- A pair of modern textbooks about statistical physics with detailed discussion.
4. **Statistical mechanics, Shang-Keng Ma** -- An idiosyncratic textbook that introduces statistical mechanics in the 70's on **this** campus. (Originally written in Mandarin.) The textbook discusses the fundamentals and applications of statistical mechanics and exposes some of the thorny questions in the study of statistical mechanics that are not discussed in standard textbooks.
5. Statistical mechanics, K. Huang [NTU open course](http://ocw.aca.ntu.edu.tw/ntu-ocw/ocw/cou/102S112)

A good reference is the one that you are willing to read.


## Acknowledgement:

* Prof. Christopher Laumann : for allowing us to use the python tutorial scripts.

## Outline of the course

1. Motivation and basic mathematical tools for statistical mechanics.
2. Random walks and universality classes
3. Thermodynamics as a phenomenological theory and the fundamental postulates of thermodynamics.
4. The fundamental postulates of statistical mechanics and connection with thermodynamics.
5. Applications of statistical mechanics on non-interacting systems
	* two-level system
	* ideal gas model
	* non-interacting boson/fermion
6. Interacting systems and mean-field theory

### Course plan (2025-spring)

| Date   | Contents                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :----- | :-------                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 02.20  | (w1) Introduction -- Thermodynamics, statistical mechanics and the concept of emergence. <br /> (**Random walks**, concept of the **scaling invariance**, and the **universality class**.)                                                                                                                                                <br /> *Readings*: {cite}`sethna2021statistical`: Chapter 1, Chapter 2; {cite}`callen1998thermodynamics`: Chapter 21; Online lecture notes: Fundamentals                                                                                                                            |
| 02.27  | (w2) Introduction -- (Continue) Thermodynamics, statistical mechanics and the concept of emergence. <br /> (the **diffusion equation**: microscopic picture and the effective theory, basic probability theory.)  <br /> *Readings*: {cite}`sethna2021statistical`: Chapter 2; Online lecture notes: Random walks and emergent properties. <br /> *Quiz 1*: Random matrix theory                                                                                                                                                                                                                                              |
| 03.06  | (w3) Statistical postulates and review of thermodynamics. <br /> (The ideal gas example and the formal structure of thermodynamics, Key properties of entropy. )  <br /> *Readings*: {cite}`sethna2021statistical`: Chapter 2; Online lecture notes: Random walks and emergent properties. <br /> *Quiz 2*: Taylor series and asymptotic series                                                                                                                                                                                                                                                                               |
| 03.13  | (w4) The fundamental postulates of statistical mechanics <br /> (The idea of phase space, observables, Boltzmann's entropy formula, the idea of Liouville's theorem)                                                                                                                             <br /> *Readings*: {cite}`sethna2021statistical`: Chapter 3; {cite}`peliti2011statistical`: Chapter 2 and Chapter 3, Online lecture notes: Random walks and emergent properties and Thermodynamics and statistical mechanics <br /> *Quiz 3*: Generating random walks and the emergent symmetry                              |
| 03.20  | (w5) The fundamental postulates of statistical mechanics <br /> (Proof of Liouville's theorem, variational principle of the entropy, quantum version of the Boltzmann's postulate, the phase space of ideal gas, the **microcanonical ensemble**. )                                                                           <br /> *Readings*: {cite}`sethna2021statistical`: Chapter 3; {cite}`peliti2011statistical`: Chapter 2 and Chapter 3, Online lecture notes: Thermodynamics and statistical mechanics and Postulates of statistical mechanics <br /> *Quiz 4*: Monte Carlo for $\pi$                              |
| 03.27  | (w6) The fundamental postulates of statistical mechanics <br /> (The **canonical ensemble**, **generalized ensemble**, **Grand canonical ensemble**.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 04.03  | (w7) Holiday                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 04.10  | (w8) **The midterm exam**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 04.17  | (w9) The interacting free systems <br /> (Single mode harmonic oscillator, midterm exam discussion)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 04.24  | (w10) The interacting free systems <br /> (Fermions and bosons, quantum statistics, Hamiltonian and Hilbert space of many-particle systems, partition function and grand partition function for free fermions/bosons.)                                                                                                                                                                                                                                                                                                                                                                                                        |
| 05.01  | (w11) The interacting free systems <br /> (Bose-Einstein and Fermi-Dirac distribution, Bose-Einstein condensate, Fermi gases, second quantization )                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 05.08  | (w12) The interacting free systems <br /> (second quantization, Goldstone theorem, phonon, photon) <br /> Phases and phase transitions <br /> (Motivation of the study of phases and phase transitions.)                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 05.15  | (w13) Phases and phase transitions <br /> (Phases and phase diagram, thermodynamic limit, phase transitions, symmetry and spontaneous symmetry braking (I:Introduction), classical Ising model and the phase diagram )                                                                                                                                                                                                                                                                                                                                                                                                        |
| 05.22  | (w14) Phases and phase transitions <br /> ( The heuristic arguments of the phase diagram of Ising model, spontaneous symmetry breaking(II: Analytic property of free energy for finite and thermodynamic system).)                                                                                                                                                                                                                                                                                                                                                                                                            |
| 05.29  | (w15) Phases and phase transitions <br /> ( Spontaneous symmetry breaking(III: Ergodicity breaking), the one-dimensional Ising model and the transfer matrix method, The Weiss mean field theory and the universality class, comparing Ising model and Van der Waals gas model, symmetry and the Ginsburg-Landau theory. )                                                                                                                                                                                                                                                                                                    |
| 06.05  | (w16) **The final exam**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |


## How to benefit from the course? 

The correct mindset: to pass the course is not difficult; to learn something requires hard work!
* For students who want to work in *theoretical physics*: The bar for theoretical physics is high. It would help if you tried to learn statistical mechanics by self-studying the subject. Try to self-studying the two textbooks and discuss with classmates, TAs, and me during office hours for those important conceptual questions.
* The bar is also high for students who want to work in *experimental physics*: Try to connect statistical mechanics with experimental phenomena that you have learned. I will mention some examples. However, those examples are far from enough to build the physics intuition for an outstanding experimentalist.
* For students who do not belong to above-mentioned categories: The bar is even higher. Try to find out the possible use of statistical mechanics for the subjects that you are interested in. During the lectures, you might have a feeling why statistical mechanics could have a broad range of applications. If you are interested in X, you can try to google "statistical mechanics and X." I believe you can find something interesting.
* The bottom line is: **DO NOT LEARN SUBJECTS BY ATTENDING LECTURES ONLY**. You can become better and better by thinking independently, but not by attending more and more lectures.

## How to use this note?

1. I will have a short summary of the key concepts that I hope you learn in each section. After the lecture or reading the section, a simple question is: do I know the meaning of the statement in summary?
	```{admonition} Summary
	:class: tip
	It is important to understand the summary after your finish reading the section or attending the lecture.
	```
2. There will be some interesting simple questions that are worth thinking about. It will be a good question to discuss with the TAs during the office hours.
	```{admonition} What?
	:class: tip
	Why is the sky blue?
	```
3. There will be problems that are not part of the homework. However, it will be a good exercise to work through it.
	```{admonition} Exercise 
	:class: tip
	Proof $a^2+b^2=c^2$ for a right triangle using dimensional analysis.
	```
4. Some of the material will be in the jupyter notebook format. That means you can download the jupyter notebook and run your own simulation.

5. We can use tabs to understand the conclusion from different scopes. For example, the Pythagorean theorem is

	````{tab} Mathematics
	```math
	A result for right triangle.
	```
	````
	````{tab} Physics
	```phys
	A result for dimensional analysis.
	```
	````



