# Who we are?
* We are FRC Team 3481, and FTC Team 4602, 4008, and 6976.
* Our repositories are free to use for any team to use as inspiration or code snippets!

# Team Repos
* FRC Team 3481 - [FRC2024](https://github.com/BroncBotz3481/FRC2024)  
[![Open in Github Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=594465053)
* FTC Team 4008 - [FTC2024-4008](https://github.com/BroncBotz3481/FTC2024-4008)
* FTC Team 4602 - [FTC2024-4602](https://github.com/BroncBotz3481/FTC2024-4602) 
* FTC Team 6976 - [FTC2024-6976](https://github.com/BroncBotz3481/FTC2024-6976)

# Mentor Example Code
* Our mentors have created example code to serve as a guide and show implementations within our rules.
* The [repository](https://github.com/BroncBotz3481/FRC2022-MENTOR) is available in codespaces for live testing and development within the browser too! 
* Remember to **DELETE** your codespace after you **PUSH** changes to your own repository that way you can make the most out of the 60hrs free per month!  
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=567809275)

<details><summary>Bronc Botz Command Based Programming</summary>  

* Our organization follows the coding paradigm within the new CommandBased programming framework for FRC based off of ["The Art of Unix Programming"](https://www.catb.org/~esr/writings/taoup/html/ch01s06.html) rules.  
* Our interpretation is as follows:
  * Subsystems = Interface  
  * Commands = Engines  
  * Policy = Policy  

</details>
<details><summary>Basic Architecture</summary>  

* All Subsystems **MUST** have a "Policy Class" which contains static variables that may be userful to access about that subsystem without having to fetch the object itself. 
  * Policy classes **MUST** be used for **ANY** algorithmic operation affecting a subsytem (if/then's).  
* All algorithmic operations must be done via static functions within the "Policy Class".
  * This is done to ensure subsystem classes are exclusively operation oriented and do not stray into algorithmic operations causing the time to comprehend a class to rise significantly.  
* Subsystems are programmatic representations of physical systems, psuedo-subsystems may exist for the sole purpose of providing and interpreting abstracted sensor feedback (like vision processing).  
* All subsytems must have a default command which returns them to a "normal" state.  
* Sometimes default commands must change between autonomous and teleop modes.  
* Commands are simple actions and must be seperated as such, if a complex action needs to occur it should be within a ParallelCommandGroup or similar unless there is a ligitimate reason that it cannot be done that way.  
* The subsystems commands folder contain only packages representing each subsystem OR subsystem grouping.  
* All utility classes must be in their own package seperate from the commands and subsystems folder.  
* All functions serve one purpose.  
  * For example if a motor controller needs configured there should be a single function which configures that motor controller.  

</details>
<details><summary>The Rules</summary>  

1. Rule of Modularity  
> Write simple parts connected by clean interfaces.  
2. Rule of Clarity  
> Clarity is better than cleverness.  
3. Rule of Composition  
> Design programs to be connected to other programs.  
4. Rule of Separation  
> Separate policy from mechanism; separate interfaces from engines.  
5. Rule of Simplicity  
> Design for simplicity; add complexity only where you must.  
6. Rule of Parsimony  
> Write a big program only when it is clear by demonstration that nothing else will do.  
7. Rule of Transparency  
> Design for visibility to make inspection and debugging easier.  
8. Rule of Robustness  
> Robustness is the child of transparency and simplicity.  
9. Rule of Representation  
> Fold knowledge into data so program logic can be stupid and robust.  
10. Rule of Least Surprise  
> In interface design, always do the least surprising thing.  
11. Rule of Silence  
> When a program has nothing surprising to say, it should say nothing.  
12. Rule of Repair  
> When you must fail, fail noisily and as soon as possible.  
13. Rule of Economy  
> Programmer time is expensive; conserve it in preference to machine time.  
14. Rule of Generation  
> Avoid hand-hacking; write programs to write programs when you can.  
15. Rule of Optimization  
> Prototype before polishing. Get it working before you optimize it.  
16. Rule of Diversity  
> Distrust all claims for “one true way”.  
17. Rule of Extensibility  
> Design for the future, because it will be here sooner than you think.  

</details>

<details><summary>Bronc Botz Student Onboarding</summary>
 
# Student Tasks
1. Install WPILib, FRC Game Tools, REV Hardware Client, and CTRE Pheonix Tuner.
2. Create a robot project and include the REVLib and CTRE libraries.
3. Design a Command Based robot following our paradigm with the following mechanisms (assume all motors are `CANSparkMax`'s):  
  Arm  
  Differential Drive (4 motor drive train)  
  Climber  
  Shooter (Attached to arm)  
4. Prove the design follows our paradigm by submitting it for mentor validation.
5. Fill in 3 of the subsystems.
6. Create corresponding commands.
7. Setup the default commands for every subsystem.
8. Connect corresponding commands to a controller input.
9. Submit for mentor validation.
 
</details>
