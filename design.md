---
layout: page
title: Design Documentation
permalink: /design/
---

#learnVCS Design Document

---

1. [Abstract](#abstract)
2. [Mission Objective](#mission-objective) 
3. [Constraints](#constraints)
4. [Target Audience](#target-audience)
5. [Resources](#resources)
    1. [Git Graph](#git-graph)
    2. [Why Use Version Control](#why-use-version-control)
    3. [Find Out More](#find-out-more)
    4. [About](#about)
6. [Style Guide](#style-guide)
    1. [Typography](#typography)
    2. [Colors](#colors)
    3. [Header](#header)
    4. [Commit Graph](#commit-graph)
    5. [Graph Nodes](#graph-nodes)
    6. [Commit Message View](#commit-message-view)
    7. [Repository Select Modal](#repository-select-modal)
    8. [Section](#section)
    9. [Image Group](#image-group)
    10. [Badge](#badge)
    11. [Profile](#profile)

---

##Abstract
This document describes the design of the [learnVCS](https://github.com/learnVCS/learnVCS.github.io/) project. It outlines the goal of the project, the target audience, and the constraints, and in doing so allows us to design the best project within those limitations.

##Mission Objective
Version Control is an important aspect of organized software development, but the concepts and various version control systems (VCS) can be difficult to grasp when you're first starting out. School is a great place to learn about this before entering the real world, but as of now it is not being given much focus in the [Interactive Games and Media (IGM)](https://www.rit.edu/gccis/igm/) program at the [Rochester Institute of Technology (RIT)](http://www.rit.edu/). The goal of this project is to __give students a resource they can use to understand version control concepts and give teachers a resource they can use to integrate version control lessons into their presentations.__

##Constraints
1. __The product should be easily integrate into professors existing lessons.__ Redesigning the IGM curriculum would be a major undertaking that is beyond the scope of this initial semester-long release cycle. We should focus on making a product that can be integrated into existing lessons, such as extra slides that can be integrated with existing presentations.

2. __The product should consist of a single page.__ If a person were to stumble on this site, we would want them to be able to find exactly what they are looking for with minimal effort. They should not have to click around the site to find something basic. As such, the site should present all information in a single, easy-to-navigate page.

##Target Audience
__Professors__ - Because learnVCS is intended to be integrated with the IGM curriculum, professors are crucial to delivering this information. It should be easy to demonstrate the learnVCS material in front of new students in the introductory program. Additional materials, such as supplementary slides to use in presentations, would also be beneficial.

__Newcomers to Version Control__ - learnVCS is designed to teach version control concepts to IGM students, but it should be accessible to anyone with some technical knowledge but no prior experience. It should present the concepts clearly and concisely, even without any prior experience with version control. 

##Resources

learnVCS will provide a curated collection of resources to convey version control concepts through multiple technologies. This section describes the resources we will provide. 

###Git Graph

####Dependencies:
 - [React](http://facebook.github.io/react/)
 - [react-commits-graph](https://github.com/jsdf/react-commits-graph)
 - A sample app to demonstrate a graph
 
####Purpose
The purpose of this section is to visually demonstrate principles of repository flow in version control. It will display an interactive graph of a Git repository hosted on GitHub.

####Initial State
Initially the graph displayed will be the commit history for a simple console application. The sample application is designed to effectively demonstrate version control principles through its branching model and quality commit messages. The sample application is hosted on GitHub, but the commit information will be stored locally as JSON for faster loading, and in the event that GitHub is down. __GitHub support must not be required in order to get the most out of this interaction.__ The sample application will be a simple CLI calculator program, written in C#, though the actual form of the application is incidental. 

####Loading a Graph
The user will be able to enter the user or organization name and repository name of a particular public project on GitHub. They will then be prompted to authenticate with GitHub using OAuth. After successful authentication, the commit information will be loaded in from GitHub's API, and passed through a React plugin to produce an SVG representation of the [Commit Graph](#commit-graph). The user will also be able to click or tap on commit nodes, represented as colored circles, to see details such as the commit message, author, date and hash.

###Why Use Version Control?

####Purpose
This section is intended to highlight primary motivators for using version control. Specifically, we want to highlight __version control's ability to track file changes over time__, __version control's ability to make collaborating among multiple people easier__, and __version control's ability to store a working backup of your project__.

###Learn Git

####Purpose
It is outside the scope of learnVCS to go in-depth on any particular version control system. As Git is the most popular VCS for publicly hosted code, this section will provide a small collection of hand-picked resources on learning and getting started with Git.

###Find Out More

####Purpose
While learnVCS focuses primarily on Git for the reasons outlined in the previous section, it's important to acknowledge other version control systems due to their applications and significance historically and in modern software development. In a similar manner to the previous section, this section will contain curated links to external resources that describe different version control systems and the concepts they bring to the table.

###About

####Purpose
There will be a low-key profiling of the team members and resources employed in the making of learnVCS. Each team member will have a small picture, their name, a description of their role and a small blurb about how cool they are. Below these profiles will be appropriate accreditation to the various open source projects and branding assets utilized in the making of learnVCS.

##Style Guide

The visual direction of learnVCS is constructed with the principles of atomic design in mind. Basic elements are developed first and are followed by more complex arrangements of basic elements. These elements are combined to create full pages.

###Typography

---

![Typography](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/Typography.png)

---

####Description
This covers the font styling of the site's text. It makes use of basic, sans-serif fonts to increase readability. The text for the header and the navigation is actually completely white, but it is displayed as having a black outline so that it will show up in this document. It is worth mentioning that the main title is actually smaller than the section titles. This is done so that the main header will still stand out, but won't overshadow the actual content.

####Style Notes

#####Main Title
- __font-size:__ 24px
- __font-family:__ Raleway Black
- __color:__ #FFFFFF

#####Section Header
- __font-size:__ 30px
- __font-family:__ Montserrat
- __color:__ #1C1208

#####Section Subheader
- __font-size:__ 24px
- __font-family:__ Montserrat
- __color:__ #1C1208

#####Badge Header
- __font-size:__ 24px
- __font-family:__ Montserrat
- __color:__ #1C1208

#####Navigation Link
- __font-size:__ 24px
- __font-family:__ Montserrat
- __font-color:__ #FFFFFF

#####Link (normal)
- __font-size:__ 24px
- __font-family:__ Roboto Bold
- __color:__ #1C1208

#####Link (hover)
- __font-size:__ 24px
- __font-family:__ Roboto Bold
- __text-decoration:__ underline
- __color:__ #1C1208

#####Body Text
- __font-size:__ 24px
- __font-family:__ Roboto Regular
- __color:__ #1C1208

###Colors

---

![Colors](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/Colors.png)

---

####Description
learnVCS aims to make use of bright and inviting colors, similar to the ones specified in [Google's Material Design guidelines](https://www.google.com/design/spec/material-design/). Text should make use of muted whites and blacks for legibility. All colors should have a light and dark variant. 

####Style Notes

#####Black
- __normal:__ #282822
- __light:__ #626260
- __dark:__ #1C1208

#####Blue
- __normal:__ #53B2BD
- __light:__ #80C7D2
- __dark:__ #3E888C

#####Red
- __normal:__ #E15E5F
- __light:__ #E8898D
- __dark:__ #B7413B

#####Yellow
- __normal:__ #FFAD22
- __light:__ #FFC360
- __dark:__ #D18308

#####Pink
- __normal:__ #FEE9DC
- __light:__ #FEF0E9
- __dark:__ #D0B7A6

#####White
- __normal:__ #FFFAF0
- __light:__ #FFFDF8
- __dark:__ #DICFB7

###Header

---

![Header](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/Header.png)

---

####Variants

---

![Header Large](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/HeaderLarge.png)

_A header on a large screen with the navigation list included._

---

![Header Expanded](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/HeaderExpanded.png)

_A header on a small screen with the navigation expanded._

---

####Description
The header appears at the top of the page and has two purposes:

1. Establish learnVCS's name and brand.
2. Allow the user to navigate the page.

####Behavior
The header fills the entire width of the screen. Clicking on a navigation item will quickly take the user to that location on the screen. On large screens, all of the navigation items are listed and floated to the right. On smaller screens, the navigation list is replaced with a hamburger menu icon. Clicking on this will cause a list of the navigation icons to expand downwards, where they can then click on them.


###Commit Graph

---

![Commit Graph](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/CommitGraph.png)

---

####Variants

---

![Commit Graph with Commit Message View](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/CommitGraphModal.png)

_A Commit Graph with the [Commit Message View](#commit-message-view) open._

---

![Commit Graph with Repository Select Modal](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/CommitGraphSelect.png)

_A Commit Graph with the [Repository Select Modal](#repository-select-modal) open_

---

####Description 
The Commit Graph is used to visualize the flow of commits in a single Git repository. It starts with a sample repository, but the user has the option to select another project from GitHub. Each node on the graph represents a single commit. Clicking on a node will allow the user to learn more about that commit. 

####Behavior
When the graph finishes loading the commits, the first node appears about a third of the way into the page. Additional nodes are added to the right. If there are more nodes than can be displayed on the screen, they will flow off the screen and the user can scroll to see more. 

#####Selecting a Node
When the user selects a node, the graph will automatically scroll until that node appears in the center of the screen. After that, it will load the Commit Message View. 

#####Changing the Repository
A magnifying glass icon will appear in the upper left corner of the screen, inviting the user to select a repository to display. If the user clicks or taps it, the [Repository Select Modal](#repository-select-modal) will appear above the graph. Loading a new repository will close this modal and change the structure of the graph.

###Graph Nodes

---

![Graph Nodes](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/Nodes.png)

---

####Description
This is the node styling that will appear on the commits graph. Each node describes a commit from the repository. Different colors are used to identify different branches. The colors are taken directly from [Google's Material Design guidelines](https://www.google.com/design/spec/material-design/).

####Behavior 
Each node color has two variants: a dark variant, and a white variant with a border. The bordered white variant is used to highlight the node that is currently selected. When the user clicks or taps on a regular node, it the white border animates outward. The dark variant is used when the graph is displayed in a dimmed state.

###Commit Message View

---

![Commit Message View](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/MessageView.png)

---

####Description
The Commit Message View is a part of the [Commits Graph](#commit-graph). It describes a commit by displaying the commit message, the author of the commit, the date, and the hash. It is above the commits graph but is slightly transparent so as not to obscure the content.

####Behavior
The Commit Message View has a fixed width and height. When the user clicks on a node from the commits graph, the Message View appears next to it and is populated by the information from that commit. Any content overflow is hidden, but the user can scroll through it. The Message View can be dismissed by clicking off of it, or by clicking on the "X" icon.

####Style Notes
- __Graph Node:__ The node from the graph that was clicked to display the Commit Message View.
- __Message Header:__ The first line of the commit message.
- __Message italic:__ The date and time of the commit
- __Message body:__ The remainder of the commit message.

###Repository Select Modal

---

![Repository Select Modal](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/SearchModal.png)

---

####Variants

---

![Repository Select Modal Help Screen](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/SearchModalHelp.png)

_A help screen that highlights what to look for when selecting a repository on GitHub._

---

![Repository Select Modal Loading](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/SearchModalLoading.png)

_The Repository Select Modal when a repository is being loaded._

---

![Repository Select Modal Loading](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/SearchModalError.png)

_The Repository Select Modal after a repository failed to be loaded._

---

####Description
The Repository Select Modal is used to specify a GitHub repository to display. The user is prompted to enter the name of the GitHub user and the name of the repository, which is used to look up the repository and get the commit information using GitHub's API.

####Behavior
The Repository Select Modal appears when the user clicks on the magnifying glass in the upper left corner of the commits graph. The User can enter the name of the GitHub user and the name of the repository in the text fields. Clicking off the modal or on the "X" button will dismiss it.

#####Submitting
When the user presses submit, they will be prompted to enter their GitHub credentials using OAuth. When they return to the graph, the text of the submit button will be replaced with a loading icon. If the repository loads, the modal will close and the graph will be displayed. Otherwise, an error message will appear on the bottom.

#####Help
It may not be immediately obvious what information the user needs to submit. A help screen is included to describe this. If the user clicks "Need help?", the content of the modal will be replaced by a brief description of the content they need and an image that highlights where they can find it on GitHub.


###Section

---

![Section](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/SectionWhite.png)

---

####Variants

---

![Red Section](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/SectionRed.png)

_A section using a red color scheme._

---

![Blue Section](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/SectionBlue.png)

_A section using a blue color scheme._

---

![Yellow Section](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/SectionYellow.png)

_A section using a yellow color scheme._

---

####Description 
A section is a generic container that is used to group content. It consists of a header that describes the content at the top, followed by the main section, which can contain sort of content. There are variations of sections for each of the main colors.


###Image Group

---

![Image Group](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/ImageGroup.png)

---

####Description
An image group is a combination of an approximately square image, a section subheader, and body text. The image will always be between 150px and 220px. This arrangement is used to quickly convey a concept by using imagery and a brief description. 

####Behavior
An image group sizes itself based on the current screen size. On a wide screen, up to three of these groupings can be displayed side-by-side horizontally. On smaller screens, each can be displayed on its own row.

####Style Notes
- __image:__ An image that illustrates the concept being described.
- __section subheader:__ The name of the concept being described.
- __body text:__ A brief description of the concept.


###Badge

---

![Badge](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/BadgeWhite.png)

---

####Variants
---

![Red Badge](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/BadgeRed.png)

_A badge using a red color scheme._

---

![Blue Badge](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/Badge.png)

_A badge using a blue color scheme._

---

![Yellow Badge](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/BadgeYellow.png)

_A badge using a yellow color scheme._

---

####Description
Badges are used to describe a subject and link to outside content. Badges appear to hover above the page, being surrounded by a text shadow. Inside the badge is an image related to the subject and a brief description of the content. 

####Behavior
The entire area of a badge is a link. Clicking anywhere within the bounds of the badge will open a link to outside content in a new page. Hovering over a badge will cause the background to lighten slightly.


###Profile

---

![Profile](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/Profile.png)

---

####Variants

---

![Profile Mobile](https://raw.githubusercontent.com/learnVCS/blog/gh-pages/images/mockups/ProfileMobile.png)

_The profile grouping resized to fit on a smaller screen._

---

####Description
A profile provides information about a person who worked on the project. It consists of an image of the person, their name, their role in developing learnVCS, and a fun description.

####Behavior
A profile sizes itself based on the current screen size. On a wide screen, up to three profiles can be displayed horizontally.

On smaller screens, the positioning of the profile elements is reordered. The profile image shrinks and moves to the left, while the text content moves to the right. Profiles are also arranged vertically. 

####Style Notes
- __image:__ A square photo of the person.
- __section subheader:__ The name of the person.
- __italic text:__ A brief description of the person's role on learnVCS.
- __body text:__ A brief biography of the person.