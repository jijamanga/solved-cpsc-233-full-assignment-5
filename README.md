Download Link: https://assignmentchef.com/product/solved-cpsc-233-full-assignment-5
<br>
New concepts to be applied for this assignment<strong>:</strong>

<ul>

 <li><h3><span style="font-weight: 400;">Dynamic (singly linked) lists</span></h3></li>

</ul>

<h3><span style="font-weight: 400;">File input and output is not necessary for this assignment. The data for the lists will be manually entered by the user at run time. The program won’t save the list contents to file.</span></h3>

<h3>Description:</h3>

For this assignment you are to write a program that allows a person to manage their movie collection. The full version will perform some common list management functions such as: adding, displaying, removing or searching. There should not be a limit on the number of movies that can be added.Each movie will be described by four fields:

<ol>

 <li>Movie name</li>

 <li>The names of the first three cast members</li>

 <li>The genre of the movie</li>

 <li>The number of stars (the rating of the movie)</li>

</ol>

<h4>Description of the fields</h4>

<ol>

 <li><strong>Movie name</strong>This field consists of an alpha (and sometime numeric string e.g., “STAR TREK II” can also be titled as “STAR TREK 2”).</li>

</ol>

<ol>

 <li><strong>Cast</strong>The cast list will consist of the full names of three of the actors from this film. A 1D array of strings can be used to store the cast information e.g.,</li>

</ol>

<ol>

 <li><strong>Genre</strong>The genre field describes the category that the movie falls into. There will be six different categories of movies: action, drama, science fiction, comedy, horror, martial arts or ‘other’. You don’t have worry about checking for instances where a movie falls into multiple genres.</li>

 <li><strong>Rating</strong>This field uses a number of stars to rate each movie according to its entertainment value1. The greater the number of stars, the better the movie:1 star (<em>It sucks</em>): It’s not the type of movie that’s so bad that it’s good, it’s just all bad. Don’t waste your time with this one.2 stars (<em>Poor</em>): Overall there were more things that I disliked than liked with this movie. Unless there’s a ticket sale it’s probably one that you should avoid.3 stars (<em>Average</em>): There were some things that I liked and some things that I disliked. It’s one that you may want to rent/stream rather than buy.4 stars (<em>Good</em>): This movie has some flaws but overall you’ll have a great time watching it.5 stars (<em>A true masterpiece!</em>): I laughed, I cried, it became a part of me. It should definitely be nominated for an Oscar (maybe several).</li>

</ol>

When movies are displayed each field will reside on a separate line and each movie will be separated by a line of stars (but the stars are not an attribute of a movie object).TERMINATOR 2 JUDGMENT DAYArnold SchwarzeneggerLinda HamiltonEdward FurlongAction5************IT’S A WONDERFUL LIFEJames StewartDonna ReedLionel BarrymoreDrama5************ROMEO AND JULIETLeonard WhitingOlivia HusseyJohn McEneryDrama4************&lt;style=”line-height: normal”=””&gt;ONCE UPON A TIME A HERO IN CHINACharine ChanTony Leung Kai FaiPeeking Duck aka James TamMartial Arts3************<sup>1. JT: The number of stars given to the movies in the example was based solely upon my opinion and does not necessarily reflect the opinions of the university so please don’t write angry letters outrage because you thought I didn’t properly rate your favourite flick &#x263a;.</sup>

<h4>Classes</h4>

T<span style="font-weight: 400;">he basic structure is very similar to the Dice/User interface program to be covered in <a href="http://pages.cpsc.ucalgary.ca/~tamj/2016/219W/tutorials/tutorials/jan31_feb6/userInterface">tutorial</a>:</span>

<ul>

 <li style="list-style-type: none;">

  <ul>

   <li><span style="font-weight: 400;">Driver: contains the main method which kicks things off by calling a ‘start’ method of class UserInterface.</span></li>

  </ul></li>

</ul>

<ul>

 <li>UserInterface: handles user input and output, the start method will likely contain the main program loop that only ends when the user quits the program. To actually change or view the list the user interface class will invoke methods of class Manager. These operations must not be directly implemented in the user interface.</li>

</ul>

<ul>

 <li>Manager: handles all list operations such as adding, removing etc.</li>

</ul>

<ul>

 <li>MovieNode: A linked list node whose data attribute is a movie.</li>

</ul>

<ul>

 <li>Movie: Stores data associated with an individual movie (instances contains the 4 attributes associated with a movie such as name, cast etc.)</li>

</ul>

<h4>Program features</h4>

<table width="100%">

 <tbody>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>Displays an introduction to the program (describes how it works) each time that it’s run.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>Displays a sign off exit message to indicate to the user that the program has ended.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>Defines class ‘Movie’ with the 4 attributes described above.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>Defines class ‘MovieNode’ (analogous to ‘BookNode’ from my notes on linked lists) which is a class with two fields: a) ‘Data’ which is of type ‘Movie’ b) ‘Next’ which is a reference to aMovieNode (next node in the list or null for the end of the list).</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>Defines a ‘Manager’ class which will include methods for all the major list operations e.g., add, remove, search, display. Your first step is to define this class with empty methods. Later you can fill in the method bodies for the major list operations (feature #11, 14, 15, 16, 17) and the ‘helper’ methods for feature #10 (helper methods are features #12, 13).</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>Declares a head reference/pointer of type ‘MovieNode’ which is initialized to null. The head reference is an attribute of the Manager class.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>Defines a ‘UserInterface’ class which is responsible for all interactions with the user (displaying program options, getting user input). This class does not implement the same operations as the manager class! The user interface class is responsible for displaying a menu of features available (#8 below), getting the user’s selection, checking the validity of the input and determining the option selected. This class should not include the actual code for changing/displaying the list itself. Once the appropriate menu option has been determined (e.g., ‘a’) then the user interface class will tell class manager to run the appropriate method (e.g., ‘addNode()’). In tutorial the TA’s covered an example program that approximately mimics how the UserInterface class and the Managerclass interact. In that example the ‘GameInterface’ class will be analogous to the ‘UserInterface’ class and the ‘Dice’ class will be roughly analogous to the ‘Manager’ class. To get credit for the UserInterface class definition (feature #7) you simply have to outline the empty methods and attributes. Credit for implementing those methods are part of feature #8, 9 and several methods associated with #10.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Class UserInterface method): Displays a menu listing the features available. (The menu options don’t have to be functional yet, to get credit for this the feature the menu just has to be displayed).</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Class UserInterface method): The program repeats until the user quits. Each time that the program repeats the main menu (above) is displayed. The <strong>(Q)uit</strong> menu option has been implemented.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Other methods of class UserInterface): Checks that the user’s menu selection was valid and if so it determines what option was selected (likely through branching).</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Class Manager method)<strong> (A)dd a movie to the collection:</strong> You are to implement one of two versions. (You only get credit for one version or the other). In both cases the program will prompt the user to enter each field one-at-a-time. Although the program doesn’t have to check for duplicate movies it should error check the genre and the rating when new movies are added. (See the next two features). The add feature must be implemented before you can get credit for any of the other features that follow it.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td width="3%"></td>

   <td width="93%">

    <ol>

     <li>The simple version will insert new movies at the end of the list.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td width="3%"></td>

   <td width="93%">

    <ol>

     <li>The advanced version will insert movies in ascending order of name (in-order insertion). You can use the String method ‘compareToIgnoreCase()’ (i.e., case insensitive) to determine ordering. Note: an in-order insertion is NOT the same as sorting the list! For this feature you need to find the insertion point and then add the node at that point and NOT change ordering of the other elements.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Class Manager method – to be executed when the add feature is invoked): The genre should only be one of the types listed above. If not the program should continue prompting the user for a value until either a valid genre is entered, or the person signals that they wish to cancel adding a new movie (by just hitting enter – blank genre – during the error handling loop).</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Class Manager method – to be executed when the add feature is invoked): The program should check that the rating is a value between one and five. If not then the program should continue prompting the person for the number of stars until either a legitimate value is entered or the person enters a negative value (to signify that they wish to cancel this option).</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Class Manager method)<strong> (D)isplay </strong>implemented: Each movie will be separated onscreen by a line of stars.  When the list of movies is long, to prevent the output from scrolling off the screen your program should ‘pause’ the display of movies every 4th movie while it waits for the user to ‘Hit enter to continue’.  The output must be displayed in a neat and legible format.  (See the above example). The program should display an appropriate status message if the list is empty (e.g., “List is empty: nothing to display”). (<em>JT’s hint: you should implement this feature soon after you complete the add feature because it’s essential for testing the other features</em>).</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Class Manager method)<strong> (S)earch</strong>: The user types in the name of the movie (case insensitive) to see full information about that movie.  If the list is empty then the program should inform the user of this fact and no search should be performed.  If the movie is not in the list, then your program should indicate that the movie could not be found under that name.  If the movie is in the list, then your program will display additional details about that movie (all the fields of that movie will be displayed onscreen).</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="97%">

    <ol>

     <li>(Class Manager method)<strong> (R)emove a movie from the list</strong>: You can implement one of two versions of this feature (you only get credit for one). In both cases the program should produce some sort of error message if the list is already empty when this feature is invoked.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td width="3%"></td>

   <td width="93%">

    <ol>

     <li>The simple version will just remove the last node from the list.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td width="3%"></td>

   <td width="93%">

    <ol>

     <li>The advanced version will prompt the user for the name of the movie to remove. The program will then search for and remove the first instance of that movie (case insensitive search). Similar to the search, an appropriate status message should be displayed if no matches were found.</li>

    </ol></td>

  </tr>

  <tr>

   <td width="2%"></td>

   <td colspan="2" width="96%">

    <ol>

     <li>(Class Manager method) <strong>(O)pposite order display: </strong>Invoking this method will recursively display the list in reverse order (last movie display first, second last movie displayed second…the first movie is displayed last). This method should only display the list in reverse order but it should NOT change the actual order of the nodes in the list (i.e., after calling this method the movie that was first in the list should still be first in the list etc.) (<em>JT’s hint: some of you may find that this last feature is significantly harder than the other features so you might want to work on this one last.</em>)  An appropriate status message should be displayed if the list is empty.</li>

    </ol></td>

  </tr>

 </tbody>

</table>

<h4><strong>Using pre-written Java code</strong></h4>

Aside from common sense operators and operations such as those for input/output, unless you are told otherwise, you will need to write your own code and cannot use other pre-written Java classes or operators. Obviously you should not use Java classes that implement a linked list but you can use interfaces that specify a design if you wish.

<h3>Marking</h3>

To help you ensure that you haven’t missed anything here is a [<a href="http://pages.cpsc.ucalgary.ca/~tamj/2016/219W/assignments/assignment5/marking.htm">marking checklist</a>]

<h3>Points to keep in mind:</h3>

<ol>

 <li><strong>Due time:</strong> All assignments are due at <strong>4 PM</strong> on the <a href="http://pages.cpsc.ucalgary.ca/~tamj/2016/219W/index.html">due dates</a> listed on the course web page.  Late assignments or components of assignments will not be accepted for marking without approval for an extension beforehand. What you have submitted in D2L as of the due date is what will be marked.</li>

 <li><strong>Extensions</strong> may be granted for reasonable cases by the course instructor with the receipt of the appropriate documentation (e.g., a doctor’s note). Typical examples of reasonable cases for an extension include: illness or a death in the family. Cases where extensions will not be granted include situations that are typical of student life: having multiple due dates, work commitments etc. Tutorial instructors (TA’s) will not be able to provide extension on their own and must receive permission from the course instructor first. (Note: Forgetting to hand your assignment or a component of your assignment in does not constitute a sufficient reason for handing your assignment late).</li>

 <li><strong>Method of submission: </strong>You are to submit your assignment using D2L [<a href="https://d2l.ucalgary.ca/shared/LE_Basics_Videos/index.htm">help link</a>]. Make sure that you [<a href="http://pages.cpsc.ucalgary.ca/~tamj/2016/219W/tutorials/verifying.pdf">check the contents of your submitted files</a>] (e.g., is the file okay or was it corrupted, is it the correct version etc.). It’s your responsibility to do this! (Make sure that your submit your assignment with enough time before it comes due for you to do a check).</li>

 <li><strong>Identifying information</strong>: All assignments should include contact information (full name and student ID number) at the very top of your program in the class where the ‘main()’ function/method resides.</li>

 <li><strong>Collaboration</strong>: <a href="http://pages.cpsc.ucalgary.ca/~tamj/2016/219W/assignments/misconduct.html#Assignments_must_reflect_individual_work">Assignments must reflect individual work</a>, group work is not allowed in this class nor can you copy the work of others.  For more detailed information as to what constitutes academic misconduct (i.e., cheating) for this course please read the following [<a href="http://pages.cpsc.ucalgary.ca/~tamj/2016/219W/assignments/misconduct.html">link</a>].</li>

 <li><strong>Execution</strong>: programs must run on the computer science network.  If you write you code in the lab and work remotely using a remote login program such as Putty or SSH. If you choose to install Java on your own computer then it is your responsibility to ensure that your program will run properly here. It’s not recommended that you use an IDE for writing your programs but if you use one then make sure that you submit your program in the form of individual text “.java” files (one for each class that you define).</li>

 <li><strong>Source code</strong>: in order to get any credit for your work you must submit all relevant dot-java files for the assignment (e.g., Driver.java). If you only submit your byte code files (e.g. Driver.class) then you will not be awarded any credit.</li>

</ol>

<h3>D2L configuration for this course</h3>

<ul>

 <li>You can (and really should) submit work as many times as you wish before the due date</li>

 <li>D2L will only retain whatever files that you submitted the last time that you uploaded to D2L, previous files will not be retained (e.g. if you submit files: A.java, B.java, C.jpg the first time and then you submit A.java the second time then D2L will only have one file stored: A.java. That means that you should submit every file associated with the assignment each time that you want to submit something regardless of how many of those files were actually changed since the last submission.</li>

</ul>

5/5 - (6 votes)

<table width="453">

 <tbody>

  <tr>

   <td width="28"><strong>0]</strong></td>

   <td width="29">H</td>

   <td width="29">e</td>

   <td width="29">a</td>

   <td width="29">t</td>

   <td width="29">h</td>

   <td width="29">e</td>

   <td width="29">r</td>

   <td width="29"></td>

   <td width="29">M</td>

   <td width="29">o</td>

   <td width="29">r</td>

   <td width="29">r</td>

   <td width="29">i</td>

   <td width="29">s</td>

   <td width="29"></td>

   <td width="30"></td>

  </tr>

  <tr>

   <td width="28"><strong>[1]</strong></td>

   <td width="29">R</td>

   <td width="29">i</td>

   <td width="29">c</td>

   <td width="29">h</td>

   <td width="29">a</td>

   <td width="29">r</td>

   <td width="29">d</td>

   <td width="29"></td>

   <td width="29">G</td>

   <td width="29">r</td>

   <td width="29">o</td>

   <td width="29">s</td>

   <td width="29">s</td>

   <td width="29">e</td>

   <td width="29"></td>

   <td width="30"></td>

  </tr>

  <tr>

   <td width="28"><strong>[2]</strong></td>

   <td width="29">D</td>

   <td width="29">o</td>

   <td width="29">n</td>

   <td width="29">n</td>

   <td width="29">a</td>

   <td width="29"></td>

   <td width="29">B</td>

   <td width="29">u</td>

   <td width="29">r</td>

   <td width="29">k</td>

   <td width="29">e</td>

   <td width="29"></td>

   <td width="29"></td>

   <td width="29"></td>

   <td width="29"></td>

   <td width="30"></td>

  </tr>

 </tbody>