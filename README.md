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

Using the Statistics 157 Questionnaire data that we will access using the Google API, we will be visualizing a relationship between the data from the responses of our peers.  With the columns "What type of Learning Style?" and the following four columns, we are going to how we work in group settings.  How we are seen and how we see ourselves in groups.  The spectrum varies across Administrators, Producers, Entrepreneurs, & Integrators with options of Always, Sometimes, Often, & Not Often in taking on these roles.  Understanding this relationship will emphasize if the VARK Scores are at all accurate to the positioning in groups we take on ourselves.
Any questions we may have can be found [here](https://github.com/stat157/questionnaire/issues).

**Parameters**

-	Types of VARK Scores: Aural, Visual, Read/Write, Kinesthetic
-	Group Roles: Administrator, Producer, Entrepreneur, Integrator
-	Responses: Always, Sometimes, Often, Not Often

_Data from the Questionnaire can be found at: http://goo.gl/Cplm9O_

**To Begin, Preliminary Setup**

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

Navigate through your VM to find the directory containing this repository (**homework-02**). Launch iPython through this special command:

    ipython notebook --no-browser --ip=0.0.0.0 --script --pylab=inline

In your local OS, open your browser of choice and open your iPython notebook by going to (by default) _127.0.0.1:7777_
    
To produce the set of data, we can curate the data by reading the Google Spreadsheet, and presenting all of the subjects who submitted well-behaved responses (they gave exactly four proper VARK scores for their learning styles).  Within a Python Dictionary, each of our four roles corresponds to the person's degree of affinity.  With the four learning styles corresponding to their VARK scores (positive integers from 0 to 14), we've understood quantitatively what we are trying to represent.


In analyzing the data, we are developing the average learning style affinity scores for all subjects who identified with different roles at varying degrees. Within the three-level dictionary, we are looking at the role keys and dictionary values.  These dictionaries have learning style keys and dictionary values. Each dictionary represents the affinity degree keys and average learning scores are as the value.
 
Producing graphs allows us to understand how visuals representation emphasize and improve our understanding of different affinities of playing different roles help individual learn differently.

Our Final Project: [Repository](https://github.com/lauraccunningham/homework-02) & [Notebook Viewer](http://nbviewer.ipython.org/urls/raw.github.com/lauraccunningham/homework-02/master/data.ipynb)

==========

[Final Projects & Presentations](https://github.com/stat157/questionnaire/wiki/How-To-Submit-Your-Homework)
==========

Hints For Success
-----------------
To be successful you will need to collaborate within your horizontal (11 person) AND vertical (4 person) groups.

You have a better chance of succeeding with this assignment by running `git commit` frequently on your local system and by running `git push` often. If you're not sure what this means or have any questions, use resources such as GitHub Help, StackOverflow, IRC, and other resources that we configured in the first weeks of the class.

Keep notes about your process. If you are not able to make your process reproducible by the deadline then you should be able to provide notes about the errors, confusions, and other roadblocks that you encountered.

Also, keep track of those "Aha!" moments and share those with others in the class.
