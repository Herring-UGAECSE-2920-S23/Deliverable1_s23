# Class-Instructions
Instructions for each checkpoint/module in this class, as well as helpful setup/configuration instructions as well as some rules for the class


## Project Specifications
FIRST: MAKE SURE YOU REFERENCE DOCUMENTS ON ELC WHICH DESCRIBE THE OUTLINE OF THE COURSEWORK AND HOW YOU CAN EXPECT TO BE ASSESSED.

Your objective this semester is to complete the design as described in the project design document on ELC.



In order to accomplish this you'll be using Python to program your Raspberry PI and hardware provided to you for the project.

Our objective is to keep your cost to a minimum. However, any additional components that  your team may need that are not supplied to you is your responsibility, and if your team “cooks” a key component (see list), your team must replace the component or receive an incomplete for the course. So pay attention to the resources, best practices, and hints mentioned on this GitHub as well as in class.

There are three key objectives in this class which will be represented by grade-level checkpoint deliverables throughout the semester. Each of which will be graded based on a rubric which will be provided to you. 

You should strive to make this work as closely to a finished product as possible, meaning doing sufficient bug testing, and making the product easy to setup/use. A part of this process is making sure your code runs on startup for the Raspberry Pi. A small writeup for how to do this can be [found here](Deliverables/setup/launch-on-startup.md).


### Documentation Expectations

Your project will have two required documents: 

For both documents, go to ELC and refer to the Assessments for specific requirements and for the rubric(scoring) metrics for each of the User Manual and the Technical Description of the Design.

1. A User’s Manual
    
    - Write a complete step-by-step document instructing a novice user how to use your design. Think about your design as a product bought by the user. The manual will instruct the user on all of the functions of your design. 
    - From your own experience, pictures, drawings, diagrams, etc… make a user’s manual much more beneficial. 
    - Don’t forget to think about a section on errors or what might go wrong, faqs, clarification, etc. 
    - User Manuals also contain safety information for the user.

2. A full Technical Description of the Design

    - Write a complete technical design guide for your design. It should describe every facet of the design (hardware and software). It should allow a person skilled in the art to recreate your design. It should provide appropriate technical reasoning for design decisions including simulation, circuit schematics and design tradeoffs.
    - Multisim, photos of oscilloscope simulations, photos of circuits, Logic.ly simulation, Code examples for key parts of algorithms (the full code will be uploaded on GitHub), and paper worked out notes are all examples. Some of these can also be part of and come from the project management document (see below).
    - At a minimum, each progress deliverable and design deliverable should be ***WELL*** documented and occupy a chapter in the document.
    - Because every group will have different approaches to the solution, we can not give a complete requirement that every document must contain. In short, if there is something that makes your plotter work, you must document it.
    - What if your group did not design it? One example is the mechanical structure of a component. In this case, like in any technical document, you must reference the source. You should also describe the function but do not need to get into the design details.
    - What about your software? Each primary function probably has code written for it. Therefore, your document should include a chapter on the structure of your software.  Think about this as the table of contents and flow control for your software. Each of the design's features/functions that includes software and hardware is most likely a progress or design deliverable and will have a chapter in the document. Use the deliverable chapter to more fully describe the software and hardware.  
    - If you used pre-written libraries, you must reference them and briefly describe the function. Any code that you wrote from scratch should be well documented (and commented in the code).
    - Neatest, precision, and completeness will be assessed. Professionalism in content and in the presentation will also be assessed.
    
### Submitting Work

- When submitting work for this class, it will go in the deliverable assignment folder for that week. This includes any work needed for **P** and **D** deliverables, your Weekly Project Management Report, etc. Any code for your group should remain on your group GitHub repository, and you should make sure to update this with your latest work before deliverables are due.

- When submitting pictures or videos as part of your deliverable, be sure to have your subject in focus and easily seen. Make your videos short and to the point, and make sure you don't have shaky hands while you're filming.

- When submitting writing of any kind, make sure it's clear, concise, and overall decent to read. When formatting is necessary, you can assume 1.15 line spacing, and 12 pt Times New Roman or Calibri font.

## Project Rules/Best Practices
- Below is a set of rules to follow while working on this project in addition to any established on the syllabus. These are generally best practices for keeping your project organized and on track.

### Breadboard Wiring

When wiring up components with a breadboard it is crucial that your wires stay organized and distinguishable. If you don’t follow these practices, you’re likely to screw up the wiring for your audio car often, which not only leads to frustration and wasted time, but could also be fatal for your more sensitive components such as the H-Bridge chip or the Raspberry Pi. If you follow these steps, you will be well on your way to avoiding the most common pitfalls:

1. ### Use Clean Wiring
![wires](/Resources/WIREEX.png)
- Keep your wiring clean. Avoid excessively long wires which make it impossible to trace if there is a problem and are more prone to pull out. You can either purchase wires that are pre-cut to different lengths or make them yourself. 



2. ### Use Color Coding
![colorcode](/Resources/GPS.png)
- Another tip is to organize your wires so that the color matches the circuit's electrical property. This will help you identify what types of wires are which when troubleshooting your breadboard circuits. The most common wire color coding is that all POWER wires should be RED, and all GROUND wires should be BLACK.

- As you get more advanced, you can have different colors representing different voltage levels and functions. For example you can add a separate color for digital signals with 5V logic, and another for 3.3V.

- For analog circuits, you may want to have a specific color for an amplifier input or output, and yet another color to identify an ADC input.

- Besides organization, this will really help you spot mis-wirings before you apply power and potentially damage your hardware. Keep a careful lookout for RED and BLACK wires connecting to the same terminal strip, as this could indicate a short.

3. ### Final areas of "neatness"
- Use labels to identify signals.
- Clean up wiring with zipties or glue or shorter wires.
- If functions are completed and stable, consider soldering to proto/zip boards


### Maintaining your Group Github Repository

In order to encourage you to learn the useful skill of managing and using a Git/Github repository, we ask to keep your group repository up to date, follow the [Github Flow](https://guides.github.com/introduction/flow/) and to use Git/Github features like [issues](https://guides.github.com/features/issues/) to your advantage! More information on Git/Github and how to learn it will be provided in the deliverable instructions.

### Code Style/Conventions

- Your code should follow the commonly accepted code style conventions outlined in [PEP 8](https://www.python.org/dev/peps/pep-0008/) on the official Python website. In addition to the practices outlined in PEP 8, you should follow [Object-Oriented Programming](https://en.wikipedia.org/wiki/Object-oriented_programming) principles when necessary (we'll generally let you know if something needs to be a class) and avoid creating [monolithic](https://en.wikipedia.org/wiki/Monolithic_application) software; instead opt to break your software into smaller, more manageable and maintainable pieces.

- While mildly outlined in the PEP 8 document above, we'd like to reiterate that commenting your code is crucial to both the development and grading process. A good rule of thumb to follow is that a comment should *only* be added to answer a question that the code can't. In essence, if you follow the PEP 8 naming conventions and give your variables/objects meaningful names, it won't take very long to understand most code; in some ways, the code *becomes* the documentation. However, if you use a little optimization trick here, or implement a complicated operation/algorithm there, you should add a comment explaining your implementation or methodology.

### Power
- You may only power the PI with the USB-PI power adapter.
- Don’t use the PI as a power bus. It can drive digital related signals, but nothing that requires a lot of current.  In this case, use your power generated from the DC adapter provided to you and that you've designed for the appropriate voltage/current.
- Raspberry PI GPIOs must be carefully programmed prior to using them.  Be careful.
- Be careful not to short the power pins of the pi to other power pins or ground. That’ll kill em. 
 

### Class Discussion

To facilitate class discussions, we will be using this repository’s **Issues** page to post comments or questions. This is a great place to ask general questions pertaining to the course and project. You are encouraged to join the discussion but just remember to abide by the “Collaboration Policy” detailed in the course syllabus. 

To post a question or comment, see the Issues link at the top of the repository or follow this [link](https://github.com/Herring-UGAECSE-2920-S22/Class-Instructions/issues). The submission process is self explanatory. 
