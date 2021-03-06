# **Holiday Planner** 
<img src="/assets/readmeAssets/holiday_planer_ami_image.jpg">

## Index

- [Version Control](#Version_Control)
- [Change Log](#Change_Log)
- [Introduction](#Introduction)
- [Project Motivation](#Project_Motivation)
- [UX](#UX) 
    - [User Stories](#User_Stories)
    - [Wireframes](#Wireframes)
- [Features](#Features)
    - [Existing Features](#Existing_Features)
    - [Future Enhancements](#Future_Enhancements)
- [Technologies Used](#Technologies_Used)
- [JavaScript Redevelopment & Validation](#JavaScript_Redevelopment_and_Validation)
- [Testing](#Testing)
- [Deployment](#Deployment)
- [Credits](#Credits)
    - [Content](#Content)
    - [Media](#Media)
    - [Acknowledgements](#Acknowledgements)

- - - -
## **<ins>Version_Control</ins>**

|Version|Date|Author|Comments|
| --- | --- | --- | --- |
| V1 | 5 Feb, 2021 | Mel Taylor | Initial Version |
| V2 | 2 Apr, 2021 | Mel Taylor | Revised project, failed grading. Updated UX & improved and tested JS more information on testing|

[Index](#Index)

- - - -
## **<ins>Change_Log</ins>**
The project was initially submitted on the 05th of Feb 2021, it received a failing grade with the following feedback
related to areas where the project did not meet the required criteria;

### Pass Criteria:

|Criterion|Meets Criterion|Reason|
| --- | --- | --- |
1.1|No|Principles of UX design no adhered to|
1.5|No|Inconsistent graphics colour in the layout|
2.1|No|JavaScript code fails validation|
3.1|No|Testing steps are missing / incom|prehensible against the user stories, leading to many open bugs.|
3.4|No|Missing documentation for manual and automated testing|

### Merit Criteria:

|Criterion|Meets Criterion|Reason|
| --- | --- | --- |
|1.1|No|Lacks a proper layout and ambiguous idea that is not put to proper implementation|
|1.3|No|Web application does not provides a good solution to the end user’s expectations|
|4.1|No|Commits are regular but description is not clear in some cases|
|5.3|No|Testing steps or guidelines are missing / incomprehensible|
|5.4|No|Missing or incomplete deployment instructions in the README file|

### Updates
To address the areas where the project failed, I had a review with my mentor to review the UX of the 
site and establish areas where it could be improved, following that I had an on-line chat with one of the 
code institute tutors to review the fails on JS testing and documentation of testing and other areas where it 
needed to be improved. This version of the readme file is now updated to document the updates, revised design 
elements and additional testing and validation that was done.

The overall theme of the site, the functionality and information largely remains the same, with an overhaul of the UX,
to improve the visual appeal of the site and improve responsiveness on mobile devices. This addresses the main UX issues raised. 
The site was redesigned in a clean Minimalist way, using white space and light back ground colours to create breaks. Background images 
were removed where text was overlaid and only used as accent pieces. Some elements are removed for viewing on mobile and expand / collapse
features are used on mobile to minimise scrolling. On the map section, the additional information presented when clicking on the map popup no longer 
adds additional sections to the page, it is all now simplified and displayed directly in the map pop-up. This has allowed us make the Map more prominent
on the site. As the map search function is the primary focus of the site, it has been moved up the page. A short intro followed by the interactive map. 
The addition information on destinations in Ireland has been moved to the bottom, background pictures removed and simplified cards
displaying the info. 

From a functional view, one main issue was the lack of testing and validation on the JS, to address this the main.js file 
was extensively rewritten to both remove duplicate functions and ones no longer needed after site redesign. The code was extensively tested and 
validated on JSHInt. Further details are explained in the testing section of the file.

[Index](#Index)

- - - -
## **<ins>Introduction</ins>**
As detailed above in the version control and change log, this is the second iteration of this project to be deployed. The project was my milestone 2 project for the 
Fullstack Web Developer course with the [Codeinistitute](https://codeinstitute.net/), the project originally received a failing mark  (for the reasons documented above).
The project, underwent a larger redevelopment in the last 10 days to address the areas raised and implement fixes and improvements. This is the new version 
that will be resubmitted for grading. The readme has been updated with details on what was changed and the additional development and testing that 
was carried out.

- - - -
## **<ins>Project_Motivation</ins>**
The main driver behind the development of this site was to create a holiday planner, that would become a trusted site for reviews and information on 
sites around Ireland for staycations. The site is limited to Ireland, but the scope could be expanded when Covid-19 travel restrictions are eased and 
travel abroad to complete reviews is again possible. The reviews are individual and only added by the site owners so all reviews can be stood over by the
site owner, with no anonymous review information included.

As part of the design and deployment, I wanted to include two important features, the first being the ability to quickly add new locations without the need to 
recode any of the page and the second was to make the interactive map section user friendly and intuitive to use. 
The ability to add new locations quickly was achieved by placing all the location data in one file, to add a new location the location.js file can be updated with thedata for the
new location, the site picks up the new location on the next load of the page. As all the information is dynamically pick up from this file no further updates are needed. 
To make the site easy to use, the user required inputs are presented sequentially to make it easy to follow and let the user know what information they need to provide. The menus are populated 
from the locations file so only contain options when there is supporting data in the locations file. 

- - - -
## **<ins>UX</ins>**
Once the concept of the site was developed, as part of the UX design phase I decided to make the site a one page site with distinctive containers for each 
section. The site would have 6 major components,

   - Header
   - Introduction
   - Interactive Map
   - Destinations Information. 
   - Footer

Bootstrap was chosen as the main library for the major design elements, it provides the responsiveness required to ensure the site looks good and works well 
across all device sizes. On top of bootstrap, custom CSS was used to provide a unique look and feel and set the site apart. 

**Header**
The navbar is now a standard Bootstrap navbar, with a drop down for mobile. Uses navbar dark bootstrap theme.

**Introduction**
A short intro section, intoducing the site and what is avaliable, the embeded video has been replaced with an image. The image only displays on larger devices,
while on mobiles to remove to much scrolling the picture is removed getting the user to the main section quicker.

**Interactive Map**
As the primary function and main user feature of the site, some extensive redesign has happened. In the previous version, the map was half the width (large screens) of the 
screen with additional information displayed in a table to the left or on a phone an additional section below the map. In the new design, the additional information has all been 
incorporated in the map pop-up, now making the map full width. The same information is presented to the user but in a more simplified way. 
The drop down selectors used were also updated, using bootstrap selector classes and removing some of the borders.
<img src="/assets/readmeAssets/menuView V1.jpg">

The overall functionality of the map remains the same, with some improvements on the rendering of the map. Discussed further in the JS & testing Section.

**Destination**
One of the main changes in the destination section, is it has been moved to the bottom of the page so it does not distract the user from the interactive map section
which is the main function of the site. 
This section still has the same information, providing information on Ireland's destinations. The section has been improved, by removing the background image and adding
the content to a bootstrap card with a small image on top of the card. For desktops the text is displayed in 3 cards and link to the external site. For mobile / tablets,
some of the information is hidden with JS driving a show / hide option for the user.

**Form**
Due to the fact that the form was not functional and feedback that it would be better to leave it out if not working, it has been removed from the site
for the time. It can be reintroduced once I have he time to add the functionality to the back end of the form.  

- - - -
## **<ins>User_Stories</ins>**

**Site User;**
- I want to find somewhere in Ireland, where I can go for my holidays. 
- I want to get additional review information on the accommodation location, outside the generic google review.
- I want to quickly link to the site of a selected accommodation if I want to book or find more information.
- A site where I can search on a wide variety of accommodation types and then narrow my search down.

**Site Owner;**
- As the site owner, I want to be able to add new locations quickly and easily without needing to update the code. 
- I want to get input from users, where do they suggest that we review and include in the site.
- Become a trusted source for reviews of accommodation

- - - -
## **<ins>Wireframes</ins>**
Once the site concept and userstories were worked out, a wireframe was built to use as a reference guide as elements were added.
Providing a quick reference for the construction of the site during development.

| Title | Link to Wireframe (pdf) |
| --- | --- |
| Title 1 | https://app.box.com/s/c8qnumxsedgjwzw54c3bqdmbvq5oc3qe |

**Note:** There was one element added to the site that was not included in the wireframe.
A covid banner was added to the site, as the site is dedicated to travel & staycations, the banner was added as reminder to follow all current restrictions and advice.
Outside the drafted wireframe but necessary in the current Covid-19 environment.

Update : The above link is to the original wireframe, the project has under gone redevelopment since. 
1. Removed the video and replaced it with an image
2. Moved the destination section below the map and removed the background image and added content to cards. 
3. Removed the non-functioning form section. 

[Index](#Index)
- - - -
## **<ins>Features</ins>**
The following section, details the existing features on the site, followed by a list of features to be added as enhacments or features that 
were not included due to time constraints.
### <ins>Existing_Features</ins>
- Standard boot strap nav bar with exapanding nav bar on mobile
- Interactine map driven by JS and populated with pre-reviwed destinations loaded from a locations.js file.
- Addtional information and links to some of Irelands destinations
- Reduced images and text over images, to make the map the primary feature. 

- Interactive Map;
    - The map is the main appeal and function of the site. 
    - It includes simple drop down menus that are populated using a locations file, this ensures only options with supporting data are presented.
    - The menus are intuitive and appear in sequence after selection to guide the user.
    - The map draws on the google maps api to populate the data based on the user selections. 
    - Pins are clickable and provide name & address data with a button for more info to click on.


[Index](#Index)
- - - -
## **<ins>Technologies_Used</ins>**
**Balsamiq**    https://balsamiq.com/wireframes/
- Basamiq was used in the design phase to create wireframes of the proposed web site.

**Github** https://github.com/
- Github is the repository used for version control & storage of the project.
- Github pages was used for the deployment of the site.

**Gitpod** https://www.gitpod.io/
- Gitpod was the IDE used for the development throughout the project.

**Bootstrap** https://getbootstrap.com/
- Bootstrap library was chosen for the initial layout & to provide responsiveness across devices sizes, layout was customised on top of bootstrap.

**Google Maps API** https://cloud.google.com/maps-platform/
- Google Maps API to create the map
- plotting the locations based on location data.

**Google Fonts** https://fonts.google.com/
- Google fonts provided fonts for the project (Roboto Condensed & Serrat)

**Font Awesome** https://fontawesome.com/
- Icons used through the web site are sourced from Font Awesome

**W3C Validation Service** https://validator.w3.org/
- HTML & CSS code was checked on W3C validator at the end of the project.

**JSHint Static Code Analysis Tool for JavaScript** https://jshint.com/
- Validation of JS code used in the project.

**HTML Formatter** https://webformatter.com/html
- HTML code was run through HTML formatter to fix any indentation issues.

**ami.responsivedesign** http://ami.responsivedesign.is/#
- The project was tested on ami.responsivedesign
- image used in readme file was taken from ami.responsivedesign site

**w3schools** https://www.w3schools.com
- For addtional code explanations & features to use.

[Index](#Index)
- - - -
## **<ins>JavaScript_Redevelopment_and_Validation</ins>**
As part of the project update, there was extensive rewrite and testing of the JavaScript. To help improve the performance of the site, 
the JS was reduced in size by removing some unused script and reducing the number of functions. For example, in the previous version the 
expand / collapse of text was driven by functions that were repeated (with a different name) each time they were used, in this Version the
six functions were reduced to one function that used parameters that came from the HTML file with if / else if statement to provide the same
level of functionality with the reduced number of functions. 

As part of the cycle of development, the JS was regularly passed through JSHint, where as last time it was not used which resulted in many errors, 
some very basic syntax errors and others more functional. 

<img src="/assets/readmeAssets/JSHint_Report.jpg">

Above is the report from JSHint on the current version of the JS file. There are two warnings, 
1. "eval can be harmful." eval is used in the script, to pull the list of counties and I needed to pull the value as the name of the counties. I could not find an alternate.
2. "Functions declared within loops referencing an outer scoped variable may lead to confusing semantics. (map, marker)", this part of the google maps API set-up.

Google did show as an undefined variable, this again was part of the google maps API set-up. 

The five functions, were listed as unused variables, these are used and called by the index.html file as required.


[Index](#Index)
- - - -

## **<ins>Testing</ins>**
One of the main drivers for the redevelopment of the project was failure to implement sufficent testing on the previous version. 
This time around, it has been addressed with more extensive testing of the site and the JS script driving the functionality of the site. 

### Automated Testing;
The HTML, CSS and JavaScript code were validate using the following on-line tools. 
| Code | Testing | Tool | Link |
| --- | --- | --- | --- |
|JS| Validate JS code| JSHint - Static Code Analysis Tool|https://jshint.com/|
|HTML| Validate HTML code|W3C - Markup Validation Service|https://validator.w3.org/|
|CSS| Validate CSS code| W3C - CSS Validation Service|https://jigsaw.w3.org/css-validator/|

***Further details on the results from the JSHint results are documented in the [JavaScript Redevelopment & Validation](#JavaScript_Redevelopment_and_Validation) section above.***

The CSS code passed with-out issue.

When the HTML code was validated, two issues were identified.
1. A p tag, within a span was flagged. Upon investigation the span was no longer required.
2. An out of sequence H tag (not in descending order), this was updated with an appropriate H tag.
Issues were resolved and updated code committed to the project. 

The final automated functional testing was carried out on Lighthouse (plugin on Firefox)
In the previous version of the site, the results achieved were;
- Performance > 33
- Accessibility > 89
- Best Practice > 93
- SEO > 83

In the current version, there have been some major improvements;

- Performance > 67 (+ 34pts)
- Accessibility > 97 (+ 8 pts)
- Best Practice > 93 (same)
- SEO > 83 (+ same)
<img src="/assets/readmeAssets/Lighthouse Test V1.jpg">

The improvements were down to the cleaning of the JS file and reduction in the number of functions (as described in the JS section).
In addition, the YouTube embedded video was causing a lot of issues with performance so I decided to replace with a 
static image.


### Manual Functional Testing;
The site was manualy tested to ensure that all the functionality was working and the site was responsive accross the device types.
Through the development cycle the site was tested on firefox using "Responsive Design Mode" to ensure that lay-out and features were responsive to different
device types. 

**Navbar:**

| Area |Bug | Resolution |
| --- | --- | --- |
| Nav Bar |The nav bar was a standard bootstrap navbar, when testing on desktop no issues were identified. When testing on a mobile devices, the expected function was once the user touched the three bar ICON the nav bar would pop out and then collapse once the link was selected. During testing, a bug was identified, where the nav bar on mobile functioned as far as it opened and took the user to the clicked anchor point, but it did not collapse after the link was clicked.  | The issue was missing classes, the data toggle class was missing from the navbar button. Once added the retest of the function passed. No other issues were found on the nav bar. |

**Interactive Map:**

Testing of the Map section was completed on both mobile and laptop.
The expected performance was, the initial "accommodation” menu loads as a default when the page loads. Upon making a selection in the first menu, the second “province” menu is populated and displayed, and a change to this menu will populate and display the final menu “county”. A selection of the third menu will show the “render map button”. The button has an on-click function in JS that will pull the data from all 3 menus, create an array from the locations.js file data with the relevant items, which will then be drawn on the map with a pin for each location. The pin on the map also has an on-click function that will display a pop-up with information for that location, including a link (as icon) that will launch a new tab with the locations website.

| Area |Bug | Resolution |
| --- | --- | --- |
|Map Popup| When clicking on the pin for a location, the pop-up always points to the last pin added to the map rather than the pin clicked. |Upon investigation, the issue was a result of using var in the loop to create the markers and in the marker section of this function. When the var (*2) was updated to let, which resolved the issue.|
|Map Popup Info|During testing, it was found that the URL for the locations was not opening. Clicking on the link icon opened a url with a Git web Url followed by the location address. | This issue was a legacy of the previous version of the page and the way the info was displayed in a table. The JS code to add the url to the popup, was updated and some urls in the locations file were missing http:// which was also added.|


**Page Layout & Responsiveness**

Testing of the lay-out was done on a large screen (21" widescreen), mobile device (Huawei P20 lite) and tablet Amazon Kindle. 
| Area |Bug | Resolution |
| --- | --- | --- |
| Intro Section | An issue was identified on the tablet size, the intro section shows text on the right and a picture on the left for larger devices, and on mobile the picture is hidden. However, when tested on a table the text was on the right column and the picture was hidden but the space block for the picture was still there. This caused the text to be on the right column with white space on the left. | To fix the issue, I changed the media query controlling the picture display and reduced it to show on tablet devices as there was sufficient space for it, This issue only happened on tablets in portrait. |
| Footer | On mobile devices, the footer was too small and hard to read and click on the social icons. | I implemented a media query in the CSS file to allow me to apply sizing of the footer to have a proper scale on all devices.  | 
| Selector menus for map |When testing the drop down menus, on tablet devices the menus were not spaced and some went over their column. The render map button was wrapping the text in the button causing the row to expand.  | To resolve, I added SM columns in the html file and applied an max with 100% to prevent them from going out of their designated column.|
| Selector menus on mobile | during testing, I found that on mobile if the user starts to use the menu when close to the bottom of the screen, the next menu displayed off the screen and the user had to scroll down to find it. This was a poor user experience.  | To resolve the issue, I added some JS; 1. When the user changes the first menu, there was already JS to populate and unhide the second menu, I added some JS to move the menu to the top of the screen. This was also implemented for larger devices as it gives a better user experience. 2. I also added the JS to the render map button to move the map to the top of the screen. This was not implemented for larger screens as there was sufficient place to as is.|



[Index](#Index)
- - - -

## **<ins>Deployment</ins>**
The project was developed using GitHub as the repository and I choose to deploy the live project on GitHub Pages,
The live site can be accessed at https://meltaylor78.github.io/holiday_planner/

**Important Note**
The main data for the locations and data that drives the interactive map are contained in the location.js file.
This file drives the menus for the map. Ensure this file remains correctly linked if you deploy the site or make a local copy of the repo.

**To complete the deployment;**
- From the Github repository 
- Navigate to the settings tab on the top of the repository page
- Scroll down to the section GitHub Pages. 
- In this GitHub Pages section, complete the deployment selection;
- Select the Branch to deploy from the first menu
    -	Select the folder from the second menu
    -	Save the settings
Further updates can be made, such as custom domain and enforce HTTPS. I did not opt for a custom domain but did select to enforce HTTPS 
for the additional security it offers. 

GitHub also provides the option to clone the repository, cloning allows you to make a local copy of the repository on your machine. 
You can complete this using the code drop down menu to get details to clone the repositor. You can find more information on how to clone a 
repository on GitHub Docs [Cloning a repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)

[Index](#Index)
- - - -
## **<ins>Credits</ins>**
The developers of the Holiday Planner site would like to thank all those who contributed directly or indirectly to the development of the site, or 
through providing media and content for the site.

- - - -

| Details | Site | Link |
| --- | --- | --- |
| Discover Ireland images & video | Discover Ireland | https://www.discoverireland.ie/ |

In addtion to the list aboved, see the [Technologies Used](#Technologies_Used) and the [Acknowledgements](#Acknowledgements) section for others that we would like 
to extend our thanks and apperication to.

[Index](#Index)
- - - -

## **<ins>Media</ins>**

| Details | Site | Link |
| --- | --- | --- |
| Google Maps | Google Maps API | https://cloud.google.com/maps-platform/ |
| Video - Ireland – a luxury destination |  Discover Ireland - YouTube | https://www.youtube.com/watch?v=rvSdyIhpdrM&feature=youtu.be |
| Images | Discover Ireland | https://www.discoverireland.ie/ |

[Index](#Index)
- - - -

## **<ins>Acknowledgements</ins>**
| Name | Acknowledgement | Acknowledgement |
| --- | --- | --- |
| Rahul Lakhanpal | Project Mentor | Rahul provided the advice & input needed to develop the site. He also guided me with the layout and ascetics to ensure a modern look and feel. |
| Caroline Taylor | Content Provider | Helped to source images and content for the site. Reviewed included text|
| Caroline Taylor | User Acceptance Testing | Provided user functional testing and user acceptance testing |
| Discover Ireland | Content | For images and video content included |

[Index](#Index)
- - - -