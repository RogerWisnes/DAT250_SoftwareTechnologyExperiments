Hand-in report

---------------------------------------------------------------------
---------------------------------------------------------------------
-   Technical problems that you encountered during installation of  -
- the software development environment and how you have solved them -
---------------------------------------------------------------------

The requirements were as follows:
* JDK
* IDE
* Maven
* Git
* GitHub

On this matter, the first three of the mentioned requirements were already 
installed. I chose to update both JDK and IDE (IntelliJ), using the 
technologies' providers, and I updated maven through Chocolatey in Powershell 
(Windows 10).

I already had Git and GitHub as well, so nothing more to do here.

Through the installation (/updating) process, I met no problems at all.


-----------------------------------------------
-----------------------------------------------
-  How you have validated (checked) that the  -
- software development environment is working -
-----------------------------------------------

As a validating process, I have booted up previous projects of mine, 
using IntelliJ, to see if these are working as they should. 


-------------------------------------------
-------------------------------------------
- Technical problems encountered with the -
- Heroku platform and how you solved them -
-------------------------------------------

For some some reason that I cannot explain at the top of my head, the 
path for "JAVA_HOME" was set to a JRE. This created some build-problems 
when I tried the "mvn clean install"-command in Powershell. 
* To fix this, I had to change the JAVA_HOME-path to a JDK instead. This 
  solved the problem.

Another problem I met was one of the last modules in the tutorial, about 
add-ons. Completely following the tutorial, I sould have added the 
provisions-add-on, but this required me to register my credit card to my 
account. 
* I did not see any reason as to why this should be necessary in a tutorial, 
  so I chose not to do this. To "make up" for this little rebellion, however, 
  I had a look at the database-add-on instead (since that add-on was already 
  included in the project). 
  As a result, I believe that I got the point from this module of the tutorial
  without adding my credit card information. So, In short: The way I see it - 
  Problem solved.


-------------------------------------------
-------------------------------------------
- Any pending issues with this assignment -
-    which you did not manage to solve    -
-------------------------------------------

One of the modules required me to add a dependency (together with some code). 
This dependency was marked as a "not found"-error by IntelliJ. Following that 
error, the codes that used this dependency also got an error (about missing 
dependency).
* I did not look too much into this, mainly because I did not notice until after 
  I had pushed the changes, and tested the program (which seemed to work just 
  fine). 

At last, I do not know if I have misunderstood something, here, 
but the exercise-description did not mention if the project itself 
should be included in the deliverance. I though that was a bit odd, 
so I chose to think that it should be included.
This, however, resulted in the more delicate task of pushing the repository 
to GitHub. I could not figure out how to do this in a good way.
* As a bit more awkward solution, I ended up forking the project to this repository.
