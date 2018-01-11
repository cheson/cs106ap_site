#-- CS106J Spring 2017 Website
Our site's code base is pretty much a clone of Chris Piech's
CS106A website last quarter.  A full snapshot of that CS106A
website was uploaded to https://github.com/chrispiech/cs106a-winter-2017,
and our CS106J site was cloned and adapted from that.  

The master copy of everything you see here is maintained at
https://github.com/jerrycainjr/cs106j-spring-2017

#-- Code Base
In general, HTML files and file templates of interst reside in /templates and its
subdirectories.  PDFs, DOCs, DOCXs, and whatnot should be stored in the relevant
subdirectories of the root.  

+ To add announcements to the main page, modify `templates/index.html` directly.
+ To add lecture slides and PDFs, add a well-named subdirectory (e.g. 01-CS106J-Introduction)
  to the top-level lectures directory, and drop Powerpoint, PDF, and code files inside that
  new subdirectory.  Then update templates/parts/navBar.html to reference the new
  subdirectory.
+ To add handout PDFs, add the PDFS to the top level handouts directory and update
  templates/parts/navBar.html
+ To add announcements, prepend the relevant markup to the inner HTML of the
  announcements section within templates/index.html.  Modify the same
  templates/index.html file to add resources, new assignments, or update your
  office hours.

#-- Testing Locally Before Going Live
To compile all references and links to test locally, run the following command
from the root directory:

   ./compile.py -t

This compiles all templates and generates all HTML and resource files in the root directory.
You can view a staged version of the site by running:

   python -m SimpleHTTPServer

and then viewing localhost:8000 in your favorite browser.

#-- Pushing to Master Repository and Updating http://cs106j.stanford.edu
To compile all references and links for external hosting, run the following command
from the root directory:

    ./compile.py

This, too, compiles all templates and generates all HTML and resource files
in the root directory.  Locally commit everything and push all local commits
back to the master (i.e. git push should work unless you've created
local branches).  When you're ready to deploy these changes to the live site,
ssh into any myth machine, navigate to /usr/class/cs106j/WWW, and git pull everything
into place.
# cs106ap_site
