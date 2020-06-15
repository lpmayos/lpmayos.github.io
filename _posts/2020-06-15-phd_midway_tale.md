---
layout: post
title: "The path to PhD. A midway tale"
date: 2020-06-15
---

After almost three years of work on my still-work-in-process PhD, I think it is time to share some things I learned along the way. I am going to write about how I work, which by all means may be totally wrong for you or anybody else. 


### Clarifying the big picture

PhDs are long projects, and of course they evolve in time. The goal will change. Even the topic may change. If you have a bad memory, as is my case, you may wonder at some point how you got here, looking puzzle at your thesis proposal and asking yourself what happened. 
 
It is important for me to be able to see the big picture at all times, and thus I need to keep track of what I do (and why). I keep a folder on the cloud where I **organize all the information related to my PhD**. I have some documents and schemas describing the general ideas of my PhD, how it evolves on time, some future work/crazy ideas list, etc. Then, I have a folder for each PhD year, where I store specific information about things I did that year: experiments, paper submissions, paper reviews, etc. It helps. A lot.

### Designing bombproof experiments

I have a software development background, which means I jump into code waaaay too early every single time. Don't do this. **Think first**. Then, think some more. Then draw an schema of your experiment. Write down your research question and hypothesis. Outline the steps that you will follow for the concrete experiment. Then, discuss it with your supervisor and other colleagues. Make sure everybody has the same picture in their minds, that everybody understands the goal and the procedure that you'll follow to pursue it. Make sure that there is a **single picture**, and everybody is visualizing it. Then, and only then, it is (finally!) time to code.  

### Getting your hands dirty

Great. The big picture is clear, and hangs there as a shared vision to be fulfilled. It is finally time to code, and you are getting excited, a familiar tingling on your fingertips. Pay attention, this is important: **START SLOW**. Start small and manageable. Prepare some toy datasets that you can use to make sure your code runs and does (apparently) what you want it to do. Oh! By small, I mean something you can run on your 10-year-old laptop at home within a few minutes. 

Are your toy examples running? Do they look good? Great! Time to burn those GPUs. It should be easy to duplicate your toy-examples execution scripts to run the real experiments; ideally you'll be changing the path to your real datasets, the resources needed (memory, GPUs, etc) and the output folder. That should be (more or less) it. If porting your experiments to an HPC and running the real thing was complex, it is probably time to stop and redesign your code. You'll thank me later. For real.

While they run, invest some time in **documenting what you do**. Remember that big picture? It is time to start filling the gaps. Write down which experiments are you running, how to execute them, how long does it take to run them, information about the datasets you are using, etc. Do it now, because these details should be in the final paper (yay! extra points for reproducibility) and you don't want to be digging for them 5 hours to the submission deadline.

Great, results are generated. Hopefully, you did it the smart way and generated a bunch of json files with the results of the different experiments and runs (no? oh oh). Time to write some scripts to compile them and generate some data that you can easily visualize and explore. Hear me now. Do not take any manual step. Automatize the scripts compilation and visualization in (ideally) a one click process. You may need to repeat executions, to add new experiments, etc and you don't want to reproduce complex manual steps each time: "yeah, after merging the json files then I remove these empty values here ... and then I crop the results of that experiments that saved extra steps for some reason ... oh, and I have to rename that key value that I changed for the new experiments ... and ...". You get the idea. **Automatize**. It is waaaay funnier to write code than to edit json files.


### Writing, a process 

Yay! Results are looking good, and your hypothesis was right. There is a tale to be told. Time to write! 

Just to set my mind in writing mode, I start by writing a **draft abstract**. This forces me to think of how to clearly present the context, the problem I am tackling, why am I doing it, how, and what can I conclude. All in about 20 lines: a skeleton of the tale you are about to compile. This is important: you are telling a story for your readers, make it interesting!

Then, I **prepare the structure**. I do this directly on LaTeX, on overleaf.com. I like to have a main .tex file in which I import a .tex file for each section, stored in a 'content' folder. I also store my images in a separate 'images' folder. There has been [some criticism on using different .tex files](https://twitter.com/thamar_solorio/status/1262833400609677314) instead of a single file, but I personally hate the idea of having everything in a single file, Spaghetti code style.  

As you may know, I work in NLP. The field is fast-paced, which implies that for example your related work section is going to grow while you work in your reserach. Eevery two days new related papers will appear on arXiv.org, and keeping track of all of it can be a little overwhelming. Here is what (kind of) works for me. I keep a simple GDocs text file with titles, summaries, bib tex references and tags with all related work. Once it is time to work on it, I draw (with pen and paper) an schema of the different topics covered, i.e. 'linguistic features', 'BERT', 'semantics', 'optimization' ... This way, it becomes easier to relate the different papers and **build a solid related work section**.

Writing the related work section usually takes different iterations (and it is hard!), so in parallel I start writing two other sections. First, I detail my **experimental setup**: base model, framework, tasks and datasets. The notes you took while conducting your experiments will come handy now! Then, I present **the experiments** I did, along with a description of the results, with plots and images. 

Once I have my experiments written down, I work on the **analysis and conclusions**. This is one of the most interesting parts for the reader, so put some love in there. You did not work this hard just to write a weak and non-convincing end to your tale. What is your punch? Time to make it shine!

Almost there. The work is pretty much done, all there is left is to **round the tale with a nice introduction**. Make sure you present a solid context, in which the rest of the topics covered along the paper make sense. And don't forget to review the abstract you wrote! What do you do when you get a new paper in your hands? If the abstract gets your attention, then you'll scan the sections and read the conclusions; if the conclusions are interesting, you may consider reading the rest of the paper. **Add some extra love in your abstract and conclusions!**


### And afterwards, what?

Nothing. Seriously. You probably did not get much sleep on the last week, and spend too many night hours fixing code. Time to reset your mind and pay back the attention debt to your loved ones, including yourself. Go get a shower. Get a couple of days off (at least). **Eat ice-cream**. Have fun!  
