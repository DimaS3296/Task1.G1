[< to Table of Contents](./readme.md)

 An ignored file - a file which Git has been explicitly told to ignore. Ignored files are tracked in a special file named  _.gitignore_ that is checked in at the root of your repository.

 _.gitignore_ files contain patterns that are matched against file names in your repository to determine whether or not they should be ignored.

 
### Git ignore patterns

_.gitignore_ uses globbing patterns to match against file names. You can construct your patterns using various symbols:


1.   ****/logs** 
	


                logs/debug.log                 
                logs/monday/foo.bar
                build/logs/debug.log 

You can prepend a   pattern with a double asterisk to match directories anywhere 
in the repository. 



2.   ****/logs/debug.log** 
 

	

	           logs/debug.log
               build/logs/debug.log
             but not
               logs/build/debug.log 

You can also use a double asterisk to match files based on their name and the name of their parent directory.

3.    **.log** 
 
	 

            debug.log
            foo.log
            .log
            logs/debug.log
	

An asterisk is a wildcard that matches zero or more characters.

4.  ***.log**

    **!important.log**
	
 
             debug.log
          but not
             logs/debug.log
	

Prepending an exclamation mark to a pattern negates it. If a file matches a pattern, but also matches a negating pattern defined later in the file, it will not be ignored.

5. **/debug.log**
	

            debug.log
         but not
            logs/debug.log
	

Patterns defined after a negating pattern will re-ignore any previously negated files.


	

6. **debug.log** 

            debug.log  
            logs/debug.log
	

Prepending a slash matches files only in the repository root.


7. **debug?.log**
	

            debug0.log
            debugg.log
          but not
            debug10.log
	

A question mark matches exactly one character.

8. **debug[0-9].log**
	

            debug0.log
            debug1.log
          but not
            debug10.log
	

Square brackets can also be used to match a single character from a specified range.

9. **debug[01].log**
	

            debug0.log
            debug1.log
          but not
            debug2.log
            debug01.log
	

Square brackets match a single character form the specified set.

10. **debug[!01].log**
	

             debug2.log
           but not
             debug0.log
             debug1.log
             debug01.log
	

An exclamation mark can be used to match any character except one from the specified set.

11. **debug[a-z].log**
	

             debuga.log
             debugb.log
           but not
             debug1.log
	

Ranges can be numeric or alphabetic.

12. **logs**
	

             logs
             logs/debug.log
             logs/latest/foo.bar
             build/logs
             build/logs/debug.log
	

If you don't append a slash, the pattern will match both files and the contents of directories with that name. In the example matches on the left, both directories and files named logs are ignored

13. **logs/**
	

             logs/debug.log
             logs/latest/foo.bar
             build/logs/foo.bar
             build/logs/latest/debug.log
	

Appending a slash indicates the pattern is a directory. The entire contents of any directory in the repository matching that name – including all of its files and subdirectories – will be ignored



14. __logs/**/debug.log__ 

	

             logs/debug.log
             logs/monday/debug.log
             logs/monday/pm/debug.log
	

A double asterisk matches zero or more directories.

15. __logs/*day/debug.log__
	

             logs/monday/debug.log
             logs/tuesday/debug.log
           but not
             logs/latest/debug.log
	

Wildcards can be used in directory names as well.

16. **logs/debug.log**
	

             logs/debug.log
           but not
             debug.log
             build/logs/debug.log
	

Patterns specifying a file in a particular directory are relative to the repository root. (You can prepend a slash if you like, but it doesn't do anything special.) 



17.    **# ignore** 

In addition to these characters, you can use **#** to include comments in your .gitignore file:


             # ignore all logs

             <span style="color:red">*.log</span>