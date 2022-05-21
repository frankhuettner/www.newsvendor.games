---
layout: page
permalink: /teacher/
title: 🧑‍🏫 teacher
description: suggested teaching plan
nav: true
---
**Use this for your class if...**
- you are somewhat familiar with **[Julia and Pluto](https://www.youtube.com/watch?v=OOjKEgbt8AI)** (no coding is needed but you should know how to open a notebook)
- your students are capable of and have the time for **[installing Julia and Pluto and run the simulation](../play)**
- you do not rely on customer service (**[feel free to ask questions anytime](https://github.com/frankhuettner/newsvendor/issues)**)

**Otherwise**, let me recommend the excellent service by **[fathomd.com](https://www.fathomd.com/nvg)**.

#### What you get
The following is available:
- A notebook that contains the **[mini cases and preparatory questions](https://github.com/frankhuettner/newsvendor/blob/main/preparation/student_preparation.jl)**
- A notebook that contains **[the game](https://github.com/frankhuettner/newsvendor/blob/main/game/newsvendorgame.jl)** 
- A notebook that allows you to **[analyze the game results](https://github.com/frankhuettner/newsvendor/blob/main/debrief/game_results.jl)**. Here is a [DEMO](https://debrief.newsvendor.games/game_results.html) (class or player selection might not work or might be very slow; **[download the repo from GitHub](https://github.com/frankhuettner/newsvendor)** and try it locally to get a better impression.)
- A notebook that demonstrates how to **[solve the newsvendor problem](https://github.com/frankhuettner/newsvendor/blob/main/debrief/newsvendor_solution.jl)** Here is a [DEMO](https://debrief.newsvendor.games/newsvendor_solution.html) (be patient with the demo server; it's much faster if you run it yourself).

#### How I'd teach it

##### Homework prior to class
1. Ask the students to read the mini case and answer preparatory questions.
2. Let them play part I of the game.
3. Request them to download their results and submit them to you (each student will submit a TOML-file).
Note that the students can reset their play and repeat as often as they want. Hence, it might be less useful to give them grades for the performance of their play -- after all, you might want to demonstrate some flaws in their behaviour (you might however promise small rewards to the top 5). Points could be given for their answer to the preparatory questions instead. 

##### Make your slides
**Get the game results:** 
1. Save the notebook for watching the game results on your disk (if you simply open it in Pluto from the web, then make sure to save it at a location that you can find on your computer; consider reloading the notebook after saving). **[Here](https://github.com/frankhuettner/newsvendor/tree/main/debrief/data)** you find some example data.
2. Open the notebook in Pluto. 
3. At the beginning, it tells you the location for where to store the TOML-files submitted by your students.
4. Click on the ``Reload`` button. You can now select your class.
5. In order to download a figure as a PNG file, use the camera button in the menue of the figure. For a better resolution, make a screenshots with your computer.

**Solution:** 
Open the notebook containing the solution. It offers useful graphs for your explanation.

##### Homework after class
Ask the students to complete the remaining parts II, III, and IV of the game. In particular, they should be capable of correctly answering part III.