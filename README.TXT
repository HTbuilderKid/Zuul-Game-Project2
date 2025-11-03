
40. No, we don't need to make any changes to the game class. This is exactly why the enums version of the game is better than the original, and also why we're trying to improve the Zuul-bad. In the original version, commands like "go" and "quit" were hard-coded all over the Game class at the start (first commit of the project), which means that if we wanted to change "go" to "aller", like I did in the zuul-enums version, we'd have to search for every if(commandWord.equals("go")) and update it manually. 
In the enums version, the words that players type are isolated inside CommandWords, which means that the rest of the game just works with the internal enum values, like "CommandWord.GO/QUIT/etc, which never change. (The concept that we leaned in class, "loosely coupled", applies here. We can make changes to one class without affecting how another class works.)

44. The only other change to make is to the Game class (where we have to write the look method. Otherwise, everything works

45. The welcome message directly refrences CommandWord.HELP, whose toString() method returns the new text, which means that changing the "help" to "assist" will automatically update the welcome message.
