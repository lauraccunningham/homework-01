homework-02
===========
Due October 07, 2013

**Questionnaire Data Wrangling**
----

Vertical Group, #2
-----
_Role -- Name ( [GitHub Account Homepage](https://github.com) )_
  - Administrator -- Sherry XIA ( [xsherryxia](https://github.com/xsherryxia) )
  - Producer -- Laura CUNNINGHAM ( [lauraccunningham](https://github.com/lauraccunningham) )            
  - Entrepreneur -- Ashley SIA ( [ashleysia](https://github.com/ashleysia) )
  - Integrator -- David LAU ( [davidopluslau](https://github.com/davidopluslau) )

Step-by-step Instructions for Homework-02
-----

**GOAL**

To see if there is a relationship between the VARK Scores and suggested roles as opposed to the projected roles within groups we see ourselves as.  To look at the columns "What type of Learning Style?" and the following four columns, we were able to identify where we are perceived and how we perceive ourselves along the spectrum of group members.

**Parameters**

-	Types of VARK Scores: Aural, Visual, Read/Write, Kinesthetic
-	Group Roles: Administrator, Producer, Entrepreneur, Integrator
-	Responses: Always, Sometimes, Often, Not Often

_Data from the Questionnaire can be found at: http://goo.gl/Cplm9O_

**To Begin**

You will need to first open your Virtual Machine.  Log in, and get it running!  From here type in the following commands as we want to make sure you are able to run iPython Notebook, and the necessary functions for claiming data from the Questionnaire data on the Google Document shared to us via our Professor.

    sudo apt-get install ipython ipython-notebook python-pip
    sudo pip install gspread

From here we will ne cloning the `example.cfg` file from the standard class repository [_Questionnaire_](https://github.com/stat157/Questionnaire).  We want to places these files into our home directory named as `stat157.cfg` like this:

    cp example.cfg ~/stat157.cfg

Use a programming text editor to edit the example config file
`~/stat157.cfg` such as:

    vi ~/stat157.cfg

To edit this way, you will need to understand how to you `vi` and how to change the mode to edit.  We will need to be changing the email and username along with the correct [bConnected key](https://kb.berkeley.edu/campus-shared-services/page.php?id=27226).

**Additional Preliminary Setup**
To acquire all these files, run this command:

    `git clone http://github.com/lauraccunningham/homework-02.git`

Ensure that your `~/stat157.cfg` file is setup as specified above. Then, to import the appropriate libraries used in the analysis, run this command:

    sudo apt-get install python-numpy python-scipy python-matplotlib ipython ipython-notebook python-pandas python-sympy python-nose
    
The environment setups used in this course will normally also need a change of an environment variable to display graphs properly, as done through this command:

    export DISPLAY=localhost:0

Navigate through your VM to find the directory containing this repository (homework-02). Launch iPython through this special command:

    ipython notebook --no-browser --ip=0.0.0.0 --script --pylab=inline

In your local OS, open your browser of choice and open your iPython notebook by going to (by default) _127.0.0.1:7777_
    
**Curation**
Run all the cells specified in the "Curation" section, producing the curated data. At a top-level view, it is the data of all subjects who submitted well-behaved responses (they gave exactly four proper VARK scores for their learning styles). On a low level view, it is a list of Python dictionaries, each of which has four role ("Administrator", "Entrepreneur", "Integrator", "Producer") corresponding to the person's degree of affinity ("Not Often", "Sometimes", "Often", "Always"). There are also four learning styles ("Visual", "Aural", "Read/Write", "Kinesthetic") corresponding to their VARK scores (positive integers from 0 to 14).

**Analysis**
Run all the cells specified in the "Analysis" section, producing the analyzed data. At a top-level view, it shows the average learning style affinity score for all subjects who identified with different roles to different degrees. At a low level, it is a three-level dictionary. The top level is a dictionary with role keys and dictionary values. These dictionaries have learning style keys and dictionary values. These dictionaries have affinity degree keys and average learning score as the value.

**Visualization**
Run all cells specified in the "Visualization" section (i.e. all remaining cells). The graphs allows you to see how people of different affinities to different roles learn differently.

==========

[Final Projects & Presentations](https://github.com/stat157/questionnaire/wiki/How-To-Submit-Your-Homework)
==========

Objective
----
You will use the Stat 157 Questionnaire data that you will access using the Google API. Your primary objective is to visualize data from two columns of the spreadsheet data: 1) the column labeled "What is your learning style?" and 2) any other column of your choosing that you feel helps give us insight into the people in the class.

The data that we have available in the spreadsheet comes from the real world, which means the data is **dirty**. Your job before you visualize the data is to clean it up and transform it into a form that the analyzers and visualizers in your group can use.

Specifically, this is the data that YOU submitted via the Google Form as part of the Questionnaire for this course so we can better understand you, your skills, and where you're headed after you graduate. All identifying data has been redacted from this data!

Any questions regarding the homework can be found [here](https://github.com/stat157/questionnaire/issues).

Hints For Success
-----------------
To be successful you will need to collaborate within your horizontal (11 person) AND vertical (4 person) groups.

You have a better chance of succeeding with this assignment by running `git commit` frequently on your local system and by running `git push` often. If you're not sure what this means or have any questions, use resources such as GitHub Help, StackOverflow, IRC, and other resources that we configured in the first weeks of the class.

Keep notes about your process. If you are not able to make your process reproducible by the deadline then you should be able to provide notes about the errors, confusions, and other roadblocks that you encountered.

Also, keep track of those "Aha!" moments and share those with others in the class.
