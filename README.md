# FileLockDemo
Demonstrate Java NIO FileLocks for multiple processes and auto-selecting whether to write to a file or a local array.

Inter-process communication in Java is limited. One option is a file lock using the nio.channels class and the tryLock method. 
Normally one wishes the critical section, or the portion of the program where the file is locked, to be as short as possible. 
However, this greatly limits testing. 

Since the purpose of this program is to demonstrate fileLocks, the file is purposely locked while user input is requested.  Something you'd never do normally. 

The program also gives the user more choice in waiting for a file to be unlocked, as well as displaying more detailed messages about why a file can't be read or written.  Finally, unlike a normal high-score processor, which gets its input from a queue (which was filled by an actual game result), this process simply gets its input from the user. 

Try it out, but be aware that you must have 2 copies running at the same time.  Also be aware that to be able to read and write to a file the program can't be executed directly from a jar file. 

Happy Locking!
