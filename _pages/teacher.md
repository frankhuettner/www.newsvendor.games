---
layout: page
permalink: /teacher/
title: 🧑‍🏫 teacher
description: hints for teachers and a suggested teaching plan
nav: true
---
**Use this game for your class if**
- you are somewhat familiar with **[Julia and Pluto](https://www.youtube.com/watch?v=OOjKEgbt8AI)** (no coding is needed but you should know **[how to open a notebook](https://www.youtube.com/watch?v=OOjKEgbt8AI)**)
- you know how to **[download](https://stackoverflow.com/a/6466993)** or **[clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)** repositories from GitHub
- your students are capable of and have the time for **[installing Julia and Pluto and run the simulation](../play)**
- you do not rely on customer service (**[feel free to ask questions anytime](https://github.com/frankhuettner/newsvendor/issues)**)

**Otherwise**, let me recommend the excellent service of **[fathomd.com](https://www.fathomd.com/nvg)**. Their game is all web-based and you do not need any technical knowledge. This also means that students do not need to install any software and you further have the opportunity to let all students play simultaneously with the same random numbers in the classroom.


### What is in the repository?
The following is available at **[https://github.com/frankhuettner/newsvendor](https://github.com/frankhuettner/newsvendor)** for download or cloning:
- A notebook that contains the **[mini cases and preparatory questions](https://github.com/frankhuettner/newsvendor/blob/main/preparation/student_preparation.jl)**. Here is a **[pdf version](https://github.com/frankhuettner/newsvendor/blob/main/preparation/student_preparation-Handout.pdf)**.
- A notebook that contains **[the game](https://github.com/frankhuettner/newsvendor/blob/main/game/newsvendorgame.jl)** 
- A notebook that allows you to **[analyze the game results](https://github.com/frankhuettner/newsvendor/blob/main/debrief/game_results.jl)**. Here is a [DEMO](https://debrief.newsvendor.games/game_results.html) (class or player selection might not work or might be very slow; **[download the repo from GitHub](https://github.com/frankhuettner/newsvendor)** and try it locally to get a better impression.)
- A notebook that demonstrates how to **[solve the newsvendor problem](https://github.com/frankhuettner/newsvendor/blob/main/debrief/newsvendor_solution.jl)**. Here is a [DEMO](https://debrief.newsvendor.games/newsvendor_solution.html) (be patient with the demo server; it's much faster if you run it yourself locally).

### How I'd teach it

**[Download](https://stackoverflow.com/a/6466993)** or **[clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)** the repo from **[https://github.com/frankhuettner/newsvendor](https://github.com/frankhuettner/newsvendor)**

##### Homework prior to class
As part of this simulation, students will download Julia and install some packages on their computers. This means that each student will download about 1 GB of data so that it seems impractical to have this done in class. Hence, the following preparation.
1. Ask your students to read the mini case and answer preparatory questions. To this end, 
    - you can distribute the `newsvendor/preparation/student_preparation-Handout.pdf`, or
    - let them load the corresponding notebook, using the following instructions:
        1. Download Julia **[from the official website](https://julialang.org/downloads/)** and install it with the standard settings.
        2. Copy the code below. 
        ```
        begin
        # Download the notebook into a temporary directory
        nb = download("https://raw.githubusercontent.com/frankhuettner/newsvendor/main/preparation/student_preparation.jl", joinpath(mktempdir(), "student_preparation.jl"))
        # Install Pluto
        import Pkg; Pkg.add("Pluto")
        # Start Pluto and load the notebook
        import Pluto; Pluto.run(notebook=nb)
        end
        ```
        3. Start Julia (e.g. in the Windows Start Menu). The Julia REPL will appear: 
        
        <img src="https://aws1.discourse-cdn.com/business5/uploads/julialang/original/3X/b/2/b210ef1688d324908e9217b8d413d54cdb5d8ded.png" alt="Julia REPL" width="400"/>
        4. Rightclick into the Julia REPL window. This will paste the code that you copied above. Hit the <kbd>Enter</kbd> key to execute the code.
        5. Now wait for 10 minutes. Julia will install Pluto and download the preparation. After about 5 minutes, it opens your browser and you see fragments of the case. It will install further packages and is finished once the animations stop. Get a ☕ or 🍵 or read the case while waiting (*do **not** close the Julia window*).
        6. Close of Julia and the browser window when you're done.


2. Let them play part I of the game. 
    - If they've already installed Julia and Pluto for the preparation, then you can ask them to simply load the notebook from `https://github.com/frankhuettner/newsvendor/blob/main/game/newsvendorgame.jl`, e.g., by running the following instructions in the Julia REPL:
    ```
    begin
    # Download the notebook into a temporary directory
    nb = download("https://raw.githubusercontent.com/frankhuettner/newsvendor/main/game/newsvendorgame.jl", joinpath(mktempdir(), "newsvendorsimulation.jl"))
    # Install Pluto
    import Pkg; Pkg.add("Pluto")
    # Start Pluto and load the notebook
    import Pluto; Pluto.run(notebook=nb)
    end
    ```
    - Otherwise, **[here are the instructions to install Julia, Pluto, and start the game.](https://www.newsvendor.games/play/)** 

3. Request them to download their results ***before*** closing Julia and the browser window, and to submit them the TOML-file to you.
Note that the students can reset their play and repeat as often as they want. Hence, it might be less useful to give them grades for the performance of their play -- after all, you might want to demonstrate some flaws in their behaviour (you might however promise small rewards to the top 5). Points could be given for their answers to the preparatory questions instead. 

##### Make your slides
To assist your preparation for the course, the following resources might be helpful.

**Analyzing the game results** 

In Pluto, open `newsvendor/debrief/game_results.jl`. 

- At the beginning, it tells you the location for where to store the TOML-files submitted by your students. (You might need to click on the <kbd>Reload</kbd> button after adding your own data before you can select your class.)
- Alternatively, you can work with two example data sets, which come with the repository. 

You will now see the results of the play. In order to download a figure as a PNG file for your slides, use the camera button in the menue of the figure. For a better image resolution, make a screenshots with your computer.

**Solution** 

Check out the notebook containing the solution: `newsvendor/debrief/newsvendor_solution.jl`. It offers useful graphs for your explanation. Alternatively, you can ask your students to open the notebook.

##### Exercise or homework
Ask the students to complete the remaining parts II, III, and IV of the game. In particular, they should be capable of correctly answering part III.