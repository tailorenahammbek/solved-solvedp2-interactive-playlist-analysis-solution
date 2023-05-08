Download Link: https://assignmentchef.com/product/solved-solvedp2-interactive-playlist-analysis-solution
<br>
In this assignment, you will develop an application that manages a user’s songs in a simplified playlist.Objectives

Write a class with a main method (PlayList).Use an existing, custom class (Song).Use classes from the Java standard library.Work with numeric data.Work with standard input and output.Specification

Existing class that you will use: Song.javaClass that you will create: PlayList.javaSong (provided class)

You do not need to modify this class. You will just use it in your PlayList driver class.You are given a class named Song that keeps track of the details about a song. Each song instance will keep track of the following data.Title of the song.The song title must be specified when the song is created.Artist of the song.The song artist must be specified when the song is created.The play time (in seconds) of the song.The play time must be specified when the song is created.The file path of the song.The file path must be specified when the song is created.The play count of the song (e.g. how many times has the song been played).This is set to 0 by default when the song is created.The Song class has the following methods available for you to use:public Song(String title, String artist, int playTime, String filePath) — (The Constructor)public String getTitle()public String getArtist()public int getPlayTime()public String getFilePath()public void play()public void stop()public String toString()To find out what each method does, look at the documentation for the Song class: java docs for Song classPlayList (the driver class)

You will write a class called PlayList. It is the driver class, meaning, it will contain the main method.

In this class, you will gather song information from the user by prompting and reading data from the command line. Then, you will store the song information by creating song objects from the given data. You will use the methods available in the song class to extract data from the song objects, calculate statistics for song play times, and print the information to the user.

Finally, you will use conditional statements to order songs by play time. The ordered “playlist” will be printed to the user.

Your PlayList code should not duplicate any data or functionality that belongs to the Song objects. Make sure that you are accessing data using the Song methods.

Do NOT use a loop or arrays to generate your Songs. We will discuss how to do this later, but please don’t over complicate things now. If you want to do something extra, see the extra credit section below.

User input

Console input should be handled with a Scanner object.

Create a Scanner using the standard input as follows:Scanner in = new Scanner(System.in);You should never make more than one Scanner from System.in in any program. Creating more than one Scanner from System.in crashes the script used to test the program. There is only one keyboard; there should only be one Scanner.Your program will prompt the user for the following values and read the user’s input from the keyboard.

A String for the song title.A String for the song artist.A String for the song play time (converted to an int later).A String for the song file path.Here is a sample input session for one song. Your program must read input in the order below. If it doesn’t, it will fail our tests when grading.

Enter title: Big Jet PlaneEnter artist: Julia StoneEnter play time (mm:ss): 3:54Enter file name: sounds/westernBeat.wav

You can use the nextLine() method of the Scanner class to read each line of input.

Creating Song objects from input

As you read in the values for each song, create a new Song object using the input values.

Use the following process to create each new song.Read the input values from the user into temporary variables.You will need to do some manipulation of the playing time data.The play time will be entered in the format mm:ss, where mm is the number of minutes and ss is the number of seconds. You will need to convert this string value to the total number of seconds before you can store it in your Song object. (Hint: use the String class’s indexOf() method to find the index of the ‘:’ character, then use the substring() method to get the minutes and seconds values.)All other input values are String objects, so you can store them directly in your Song object.Use the Song constructor to instantiate a new song, passing in the variables containing the title, artist, play time, and file path.Because a copy of the values will be stored in your song objects, you can re-use the same temporary variables when reading input for the next song.Before moving to the next step, print your song objects to make sure everything looks correct.To print a song, you may use the provided toString method. Look at the Song documentation for an example of how to print a song.NOTE: Each Song instance you create will store its own data, so you will use the methods of the Song class to get that data when you need it. Don’t use the temporary variables that you created for reading input from the user. For example, once you create a song, you may retrieve the title using song1.getTitle();Calculate the average play time.

Use the getPlayTime() method to retrieve the play time of each song and calculate the average play time in seconds.Print the average play time formatted to two decimal places. Format the output as shown in example below.Average play time: 260.67Use the DecimalFormat formatter to print the average. You may use thisFind the song with play time closest to 4 minutes

Determine which song has play time closest to 4 minutes.Print the title of the song formatted as shown in the output below.Song with play time closest to 240 secs is: Big Jet PlaneBuild a sorted play list

Build a play list of the songs from the shortest to the longest play time and print the songs in order.To print the formatted song data, use the toString() method in the Song class.Print the play list as shown in the output below.==============================================================================Title Artist File Name Play Time==============================================================================Where you end Moby sounds/classical.wav 198Big Jet Plane Julia Stone sounds/westernBeat.wav 234Last Tango in Paris Gotan Project sounds/newAgeRhythm.wav 350==============================================================================Extra Credit (5 points)

You may notice that you are repeating the same code to read in the song data from the user for each song (Yuck! This would get really messy if we had 10 songs).

Modify your main method to use a loop to read in the songs from the user. As you read and create new songs, you will need to store your songs in an ArrayList.

This can be quite challenging if you have never used ArrayLists before, so we recommend saving a backup of your original implementation before attempting the extra credit.

Getting Started

Create a new Eclipse project for this assignment and import Song.java into your project.Create a new Java class called PlayList and add a main method.Read the Song documentation and (if you are feeling adventurous) look through the Song.java file to familiarize yourself with what it contains and how it works before writing any code of your own.Start implementing your Song class according to the specifications.Test often! Run your program after each task so you can find and fix problems early. It is really hard for anyone to track down problems if the code was not tested along the way.Sample Input/Output

Make sure you at least test all of the following inputs.Last Tango in ParisGotan Project05:50sounds/newAgeRhythm.wavWhere you endMoby3:18sounds/classical.wavBig Jet PlaneJulia Stone3:54sounds/westernBeat.wavWhere you endMoby3:18sounds/classical.wavLast Tango in ParisGotan Project05:50sounds/newAgeRhythm.wavBig Jet PlaneJulia Stone3:54sounds/westernBeat.wavBig Jet PlaneJulia Stone3:54sounds/westernBeat.wavLast Tango in ParisGotan Project05:50sounds/newAgeRhythm.wavWhere you endMoby3:18sounds/classical.wavSubmitting Your Project

Testing

Once you have completed your program in Eclipse, copy your Song.java, PlayList.java and README files into a directory on the onyx server, with no other files (if you did the project on your computer). Test that you can compile and run your program from the console in the lab to make sure that it will run properly for the grader.

javac PlayList.javajava PlayListDocumentation

If you haven’t already, add a javadoc comment to your program. It should be located immediately before the class header. If you forgot how to do this, go look at the Documenting Your Program section from lab .

Have a class javadoc comment before the class (as you did in the first lab)Your class comment must include the @author tag at the end of the comment. This will list you as the author of your software when you create your documentation.Include a plain-text file called README that describes your program and how to use it. Expected formatting and content are described in README_TEMPLATE. See README_EXAMPLE for an example.

Submission

You will follow the same process for submitting each project.

Open a console and navigate to the project directory containing your source files,Remove all the .class files using the command, rm *.class.In the same directory, execute the submit command for your section as shown in the following table.Look for the success message and timestamp. If you don’t see a success message and timestamp, make sure the submit command you used is EXACTLY as shown.Required Source FilesRequired files (be sure the names match what is here exactly):PlayList.java (main class)Song.java (provided class)READMESection Instructor Submit Command1 Luke Hindman (TuTh 1:30 – 2:45) submit lhindman cs121-1 p22 Greg Andersen (TuTh 9:00 – 10:15) submit gandersen cs121-2 p23 Luke Hindman (TuTh 10:30 – 11:45) submit lhindman cs121-3 p24 Marissa Schmidt (TuTh 4:30 – 5:45) submit marissa cs121-4 p25 Jerry Fails (TuTh 1:30 – 2:45) submit jfails cs121-5 p2After submitting, you may check your submission using the “check” command. In the example below, replace

submit -check