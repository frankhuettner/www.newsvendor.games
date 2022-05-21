---
layout: page
permalink: /play/
title: 🎮 play
description: Setup takes about 10 min (mostly unattendet) for installing Julia, Pluto, and some packages. It requires about 1 GB disk space.
nav: true
---


 

1. Download Julia **[from the official website](https://julialang.org/downloads/)** and install it with the standard settings.
2. Copy the code below. 
```
begin
  # Download the notebook into a temporary directory
  nb = download("https://raw.githubusercontent.com/frankhuettner/newsvendor/main/game/newsvendorgame.jl", joinpath(mktempdir(), "newsvendorsimulation.jl"))
  # Install Pluto
  import Pkg;	Pkg.add("Pluto")
  # Start Pluto and load the notebook
  import Pluto; Pluto.run(notebook=nb)
end
 ```
3. Start Julia (e.g. in the Windows Start Menu). The Julia REPL will appear: 
   
   <img src="https://aws1.discourse-cdn.com/business5/uploads/julialang/original/3X/b/2/b210ef1688d324908e9217b8d413d54cdb5d8ded.png" alt="Julia REPL" width="400"/>
4. Rightclick into the Julia REPL window. This will paste the code that you copied above. Hit the <kbd>Enter</kbd> key to execute the code.
5. Now wait for 10 minutes. Julia will install Pluto and download the simulation. After about 5 minutes, it opens your browser and you see fragments of the simulation. It will install further packages and is finished once the animations stop. Get a ☕ or 🍵 or use your computer for something else while waiting (*do **not** close the Julia window*).
6. Close of Julia and the browser window when you're done.
