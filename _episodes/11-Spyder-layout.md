---
title: "Spyder Layout, navigating the IDE, project setup"
teaching: 5
exercises: 0
questions:
- "How is Spyder laid out?"
- "How do we create a project and why is it important?"
objectives:
- "Be familiar with the panes contained within Spyder"
- "Be confident creating a new project and new script files"  
keypoints:
- "Python and Spyder are not the same thing. Spyder is an IDE that provides you with a convenient way to manage Python projects and Python is the underlying language that enables Spyder."
- "You will not learn everything about Python or Spyder in a day, there are a huge number of tools available to you in Spyder. The more time you commit to exploring and practicing the more you will achieve."
- "Project management is a vital part of ensuring that you are producing maintainable, sharable, and robust software."
---

## Starting a new project:
>Let us start by exploring the major features we will use for this course in Spyder. Our first aim is to become more familiar with the interface.  
>Start by generate a new project (name it **‘my_first_python_project’**).   
>  
>**Instructions**  
>* From the main menu select **‘File’ > ‘new project’ > ‘new directory’ > ‘new project’**.   
>* You will be prompted for a directory name for your project and a file path where you want to create the project.   
>* Name your project “OneZoo_PythonIntro" and choose the folder you previously created as part of your set-up worksheet.
>* Save the script file (name it **'my_first_python_script’**).  

{% include figure.html max-width="100%" file="/fig/spyderIDE.png" 
alt="Spyder pane layout on first initialisation" caption="Figure 1: Spyder layout you should expect to see (OS and version dependant)" %}

>## Top
>* **Menu Bar:**  
>The Menu bar controls some of the major actions available in Spyder. The most common are creating, saving and loading projects and scripts. If you look through the drop-down menus you will notice that many procedures have shortcuts allocated. The more familiar you get with Spyder the more you will start to take advantage of these shortcuts and possibly create or remap your own shortcuts. 
{: .callout}

>## Bottom right
>* **Console pane:**  
>This is the console pane. The console is your primary interface with the Python programming language. You will use it often for inputting prompts and displaying outputs.  
{: .callout}

>## Middle Left
>* **Script pane:**  
>You should see the script pane in this location. It provides a powerful and user-friendly environment for writing, editing, and managing Python code and other documents. You can run scripts using the green arrow run button.
{: .callout}

> ## Question: Why do we need the console and the script pane when they do similar things?
> Although there is some overlap between the two, when we look closer, we will find there are different capabilities of both
> panes. To clarify the situation using a kitchen analogy; imagine the console is your kitchen worktop, you could try out 
>different techniques, or perform specific tasks. Your script pane is akin to a recipe book, a place to create a collection of 
>work that you want to perform time and time again.  
{: .challenge }

### How these two panes influence your workflow options: 
Much of your initial learning time in Python will be spent in the Python interactive console. This is where you can test out lines of code and it can be a useful environment to try out ideas. This way of working is successful when conducting small task and initially starting off. It can quickly become inefficient for large tasks with more complex structure. Writing scripts will allow you to better manage the workflow of more complicated projects. Storing your code in scripts allows for easier maintenance, collaboration, and code clarity.

>## Top Right
>* **Variable pane:**  
>The Variable pane provides a convenient way to inspect, manage, and interact with the variables in your Python environment. This view will also help by giving you an insight to your data and allow you to interact with it more efficiently.
>* **Plots pane:**  
>The plots pane in Spyder is used to interact with graphical output from your Python code. You can visualize, explore, manage, and export data plots.
>* **Help pane:**  
>The help pane serves as a valuable resource for learning about Python programming, exploring package functionality, troubleshooting issues, and finding answers to your questions. 
>* **Files pane:**  
>The files pane in Spyder provides a straightforward way to navigate and manage files and directories within your project. 
{: .callout}

>## Far Left 
>* **Files pane:**  
>The files pane in Spyder provides a straightforward way to navigate and manage files and directories within your project. 
{: .callout}

>## Important to explore and practice
>Clearly there are many more features to Spyder we have not covered in this brief introduction. If you spend time researching and practicing using Python and Spyder you will start to collect tools that you will find useful for your research goals. Don't be afraid to try and fail. 
{: .challenge }

### Project management

### Question: We have created a project in Spyder but what can go wrong if we don’t? 
Typical problems caused by poor project management. 

1. ***Poor maintainability*** – You may remember the ad-hoc system you used for naming and organising files and folders but when you come back to a project a week, a month, or a year later will you still remember? If someone is collaborating with you will it make any sense to them? 

2. ***Data corruption*** – Defensive steps (e.g., naming convention, back-ups, read only files) will protect your data. It can be very easy to accidently modify data that should be static. Losing/corrupting data can be catastrophic for projects.


### Question: What practices should we apply when it comes to project management?
There is no ‘best’ way to manage a project, there are general principles that will make your project easier to manage. We will touch on many aspects of this during the course however a full account of these areas is outside of the scope of this session.

1. ***Segment files sensibly:*** Create clearly labelled folders/sub-folders to group similar files. This will make finding and identifying files easier.  

2. ***Read only data:*** Any original data should be read-only so it cannot be accidently modified.  

3. ***Separate functions:*** Separating the project specific code from more generic code that could be reused in other projects will improve your efficiency when starting new projects.  

4. ***Version control:*** Version control systems (VCS) are a tool that facilitate multiple users collaborating on the same project. They have a wide set of tools but are commonly used to manage reverting files to previous states, comparing changes, and managing versions. Git is the most widely used version control system. 

5. ***Backup:*** Ensuring your data and your project is backed up is vital. Consider a minimum of one local-backup and one online-backup.     

