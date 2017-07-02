Day 1 & 2
---------

Accessibility- inclusive practises for allowing any users to access website (eg disabled).
WAI-ARIA - website accessibility standards.
Web Content Accessibility Guidelines (WCAG)


GIT WORKFLOW
•	git clone nameofrepo.git
•	git checkout -b newrepo OR ( git branch newrepo && git checkout newrepo )
Change things in Atom
•	git add . OR git add -A OR git add filename.ext
•	git commit -m “message message message” -m “message on new line” -m “message on third line”
•	git checkout master
•	git pull origin master (to make sure our local master branch is up to date)
•	git checkout newrepo
•	git merge master
•	Go to your text editor and resolve any conflicts if necessary
•	There might be untracked files at this point.
•	Solution git status - are there any untracked files?
•	If yes, git add -A OR git add .
•	git commit -m “message message message”
•	git push origin newrepo
•	Go onto GitHub and make a pull request. HEAD BRANCH: newrepo
•	Someone receives the pull request. Go onto it, check files changed and check the code. Comment and tag it as appropriate.
•	When ready, they can confirm the pull request to merge it to the master branch.
•	git pull origin master
•	When branch is finished, use git branch -d newrepo to delete the branch.
•	Before you do anything to git, make sure your files are saved .




**

Day 3
-----

**
•	Display block is default display for html images. Meaning each photo is displayed on one line, and nothing else.
•	Display flex. If you want something displayed flex. Display flex , some sets of rules need to apply to the parent containers, and some need to be displayed to the children. The rule, Display:flex , is applied to the parent containers. Always to the display flex on the parent containers.
•	Display inline – display in the same level . Display inline-block is the most compact display. So you can set width and height.
•	Whenever you have multiple lines of flex, use flex-wrap.
•	DOT / means from a certain file FORWARD SLASH – TO .

Day 4 – handwritten notes

**

Day 5 (Friday 30th June)
------------------------

**
•	In order to disable JavaScript, open the settings of chrome, click show advanced/more settings,  and under privacy, click content settings, and then click Javascript, do not disable.
•	<noscript> anything within this tag does not use javascript.
•	Text should have a contrast ratio of at least 4.5. In developer tools, under the 'elements' tab if you look at accessibility properties while the element is selected, it will recommend a similar colour which provides high enough contrast and let you easily try out the recommendation in chrome.
•	:focus pseudo elements and :hover elemtns in dev tool means what happens when that element is the focus or what happens on hover
•	cyvbercrab lets you view on different screen sizes.
•	When creating media qurieis, do the mobile first max width first. So max width 250px then media query after for the case of when the screen viewport is bigger than mobile. That way the standard is for the small mobile processccor, which means the site loads faster on desktops.
•	The commit message should be more consistent as if you should imagine the message to be “this commit” …
•	Vh and vw – viewport height and viewport width
•	Highlight whole thing and press sheft tab to do reverse tab index
•	Do on focus:  instead of on hover: as it makes the webtise accessible for someone who uses keyboard.
•	Fixes closes the issue when the issue is closed into master via a Pull request.  
•	Tab-index – only add it to the things that you need to reach with the keyboard. Screen readers don’t use tab to move through the interface, they have their own way of doing so.
•	Why , what, how fpr read,e/ In what description about each page.
•	Font awesome represents a script file.
•	Animate transform or opacity – doesn’t use a lot of processing power.  
•	Update your readme as you update your code. That helps rather than saving it all to last.
Animation
•	Add a class of shake. Then do shake , hover, and animation.
•	Atom plugin called Autoprefixer. Does all the pludings for you eg webkit.
•	Background-color: HSLA or opacity.  Hugh,color. RGBA .
•	<optgroup > tag – allows you to have a list heading within a list eg Nike(opt group) then air max, hurrache, ect.

Flexbox
•	Notice that when you set the direction to a reversed row or column, start and end are also reversed.
•	when the flex direction is a column, justify-content changes to the vertical and align-items to the horizontal.
